---
title: 快速入門：從 Azure Key Vault 設定及擷取祕密 | Microsoft Docs
description: 快速入門：從 Azure Key Vault 設定及擷取祕密
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805726"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>快速入門：從 Azure Key Vault 設定及擷取祕密

此快速入門說明如何將祕密儲存在 Key Vault 中，以及如何使用 Web 應用程式擷取它。 若要查看祕密值，您必須在 Azure 上執行此作業。 本快速入門會使用 Node.js 和受控服務識別 (MSI)。

> [!div class="checklist"]
> * 建立 Key Vault。
> * 將秘密儲存至金鑰保存庫。
> * 從 Key Vault 擷取祕密。
> * 建立 Azure Web 應用程式。
> * [啟用受控服務身分識別](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)。
> * 授與 Web 應用程式從 Key Vault 讀取資料所需的權限。

繼續之前，請先確定您已熟悉[基本概念](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts)。

> [!NOTE]
> 為了解以下教學課程為何是最佳做法，我們需要了解一些概念。 Key Vault 是一個中央存放庫，可透過程式設計方式儲存祕密。 但若要這樣做，應用程式/使用者必須要先向 Key Vault 進行驗證，也就是出示祕密。 為了遵循安全性最佳做法，第一個祕密也必須定期輪替。 但透過[受控服務識別](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)，在 Azure 中執行的應用程式將會獲得一個由 Azure 自動管理的身分識別。 這有助於解決**祕密導入問題**，如此，使用者/應用程式即可遵循最佳做法，且不需要擔心輪替第一個祕密的問題

## <a name="prerequisites"></a>必要條件

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* 具有下列工作負載的[Visual Studio 2017 15.7.3 版或更新版本](https://www.microsoft.com/net/download/windows)：
  * ASP.NET 與 Web 開發
  * .NET Core 跨平台開發
* [.NET Core 2.1 SDK 或更新版本](https://www.microsoft.com/net/download/windows)
::: zone-end
* Git ([下載](https://git-scm.com/downloads))。
* Azure 訂用帳戶。 如果您沒有 Azure 訂用帳戶，請在開始前建立 [免費帳戶](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)。
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 版或更新版本。 此工具適用於 Windows、Mac 與 Linux。

## <a name="login-to-azure"></a>登入 Azure

若要使用 CLI 登入 Azure，您可以輸入：

```azurecli
az login
```

## <a name="create-resource-group"></a>建立資源群組

使用 [az group create](/cli/azure/group#az-group-create) 命令建立資源群組。 Azure 資源群組是可供在其中部署及管理 Azure 資源的邏輯容器。

請選取資源群組名稱，並填入預留位置。
下列範例會在 *eastus* 位置建立名為 <YourResourceGroupName> 的資源群組。

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

此教學課程中會使用您剛建立的資源群組。

## <a name="create-an-azure-key-vault"></a>建立 Azure Key Vault

接下來，您會使用在上一個步驟中建立的資源群組建立 Key Vault。 雖然 “ContosoKeyVault” 是作為本文中的 Key Vault 名稱使用，但您必須使用唯一名稱。 請提供下列資訊：

* Vault 名稱 - **在這裡選取 Key Vault 名稱**。
* 資源群組名稱 - **在這裡選取資源群組名稱**。
* 位置 - **美國東部**。

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

此時，您的 Azure 帳戶是唯一獲得授權在此新保存庫上執行任何作業的帳戶。

## <a name="add-a-secret-to-key-vault"></a>將祕密新增至 Key Vault

我們將新增祕密，以協助說明其運作方式。 您可能正在儲存 SQL 連接字串，或任何您必須安全保存但可供您的應用程式使用的其他資訊。 在本教學課程中，密碼會稱為 **AppSecret**，並將在其中儲存 **MySecret** 的值。

輸入下列命令，以在 Key Vault 中建立稱為 **AppSecret** 並將儲存 **MySecret** 值的祕密：

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

以純文字檢視包含在祕密中的值：

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

此命令會顯示祕密資訊，包括 URI。 完成這些步驟之後，您的 Azure Key Vault 中應該會有祕密的 URI。 寫下此資訊。 您在稍後的步驟中需要此資訊。

## <a name="clone-the-repo"></a>複製存放庫

複製存放庫以便製作本機複本，讓您可以透過執行下列命令以編輯來源：

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>安裝相依性

我們在此安裝相依性。 執行下列命令：

    cd key-vault-node-quickstart
    npm install

此專案使用了 2 個節點模組：

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>將 Web 應用程式發佈至 Azure

下面是將應用程式發行至 Azure 所需執行的一些步驟。

* 第 1 個步驟是建立 [Azure App Service](https://azure.microsoft.com/services/app-service/) 方案。 您可以在此方案中儲存多個 Web 應用程式。

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* 我們會接著建立 Web 應用程式。 在下列範例中，使用全域唯一應用程式名稱 (有效的字元為 a-z、0-9 與 -) 取代 <app_name>。 執行階段是設定為 NODE|6.9。 若要查看所有支援的執行階段，請執行 `az webapp list-runtimes`

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    建立 Web 應用程式後，Azure CLI 會顯示類似下列範例的輸出：

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    瀏覽至新建立的 Web 應用程式，您應會看到正常運作的 Web 應用程式。 以唯一應用程式名稱取代 <app_name>。

    ```text
    http://<app name>.azurewebsites.net
    ```
    上述命令也會建立具有 Git 功能的應用程式，讓您從本機 Git 部署至 Azure。 
    本機 Git 已設定為使用 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git' 的 url

* 在前一個命令完成後，建立部署使用者，您可以將 Azure 遠端新增至您的本機 Git 存放庫。 使用從「為應用程式啟用 Git」取得的 Git 遠端 URL 取代 <url>。

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>開啟及編輯方案

編輯 program.cs 檔案，以使用您的特定金鑰保存庫名稱來執行範例：

1. 瀏覽至 key-vault-dotnet-core-quickstart 資料夾。
2. 在 Visual Studio 2017 中開啟 key-vault-dotnet-core-quickstart.sln 檔案。
3. 開啟 Program.cs 檔案，並使用您先前建立的金鑰保存庫名稱更新預留位置 *YourKeyVaultName*。

這個方案會使用 [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) 與 [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet 程式庫。

## <a name="run-the-app"></a>執行應用程式

在 Visual Studio 2017 的主功能表中，選取 [偵錯] > [啟動但不偵錯]。 在瀏覽器出現時，移至 [關於] 頁面。 **AppSecret** 的值隨即顯示。

## <a name="publish-the-web-application-to-azure"></a>將 Web 應用程式發佈至 Azure

將此應用程式發佈至 Azure，以 Web 應用程式的形式即時查看，並確認您可以擷取祕密值：

1. 在 Visual Studio 中，選取 **key-vault-dotnet-core-quickstart** 專案。
2. 選取 [發佈] > [開始]。
3. 建立新的 **App Service**，然後選取 [發佈]。
4. 將應用程式名稱變更為 **keyvaultdotnetcorequickstart**。
5. 選取 [建立]。

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>啟用受控服務身分識別

Azure Key Vault 可安全地儲存認證和其他金鑰及祕密，但是您的程式碼必須向 Azure Key Vault 進行驗證，才能擷取這些項目。 「受控服務識別」可以輕易地解決此問題，因為 MSI 可在 Azure Active Directory (Azure AD) 中將自動受控身分識別提供給 Azure 服務。 您可以使用此身分識別來完成任何支援 Azure AD 驗證的服務驗證 (包括 Key Vault)，不需要任何您程式碼中的認證。

1. 返回 Azure CLI。
2. 執行 assign-identity 命令來建立此應用程式的身分識別：

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>此程序中的命令等同於前往入口網站，並在 Web 應用程式屬性中將 [受控服務識別] 切換為 [開啟]。

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>將權限指派給您的應用程式，以便從 Key Vault 讀取秘密

當您將應用程式發佈至 Azure 時，請記下輸出。 其格式應為：

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

然後，使用金鑰保存庫的名稱和 **PrincipalId** 的值來執行此命令：

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>將 Node 應用程式部署至 Azure 並擷取祕密值

現在一切都已設定。 執行下列命令以將應用程式部署到 Azure

```bash
git push azure master
```

在此之後，當您瀏覽 https://<app_name>.azurewebsites.net 時，您可以看見祕密值。
確定您已用保存庫的名稱取代了名稱 <YourKeyVaultName>

::: zone-end

::: zone pivot="dotnet"
現在，當您執行應用程式時，應該會看到擷取的秘密值。
::: zone-end

## <a name="next-steps"></a>後續步驟

::: zone pivot="nodejs"
* [Azure Key Vault 首頁](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault 文件](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK For Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Azure REST API 參考](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [Azure Key Vault 首頁](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault 文件](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK For .NET](https://github.com/Azure/azure-sdk-for-net)
* [Azure REST API 參考](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
