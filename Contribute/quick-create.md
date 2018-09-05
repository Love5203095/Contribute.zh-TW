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
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308816"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="79f51-103">快速入門：從 Azure Key Vault 設定及擷取祕密</span><span class="sxs-lookup"><span data-stu-id="79f51-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="79f51-104">此快速入門說明如何將祕密儲存在 Key Vault 中，以及如何使用 Web 應用程式擷取它。</span><span class="sxs-lookup"><span data-stu-id="79f51-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="79f51-105">若要查看祕密值，您必須在 Azure 上執行此作業。</span><span class="sxs-lookup"><span data-stu-id="79f51-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="79f51-106">此快速入門會使用 Node.js 和受控服務識別 (MSI)</span><span class="sxs-lookup"><span data-stu-id="79f51-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="79f51-107">建立 Key Vault。</span><span class="sxs-lookup"><span data-stu-id="79f51-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="79f51-108">將祕密儲存在 Key Vault 中。</span><span class="sxs-lookup"><span data-stu-id="79f51-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="79f51-109">從 Key Vault 擷取祕密。</span><span class="sxs-lookup"><span data-stu-id="79f51-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="79f51-110">建立 Azure Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="79f51-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="79f51-111">[啟用受控服務身分識別](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)。</span><span class="sxs-lookup"><span data-stu-id="79f51-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="79f51-112">授與 Web 應用程式從 Key Vault 讀取資料所需的權限。</span><span class="sxs-lookup"><span data-stu-id="79f51-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="79f51-113">繼續之前，請先確定您已熟悉[基本概念](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts)。</span><span class="sxs-lookup"><span data-stu-id="79f51-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="79f51-114">為了解以下教學課程為何是最佳做法，我們需要了解一些概念。</span><span class="sxs-lookup"><span data-stu-id="79f51-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="79f51-115">Key Vault 是一個中央存放庫，可透過程式設計方式儲存祕密。</span><span class="sxs-lookup"><span data-stu-id="79f51-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="79f51-116">但若要這樣做，應用程式/使用者必須要先向 Key Vault 進行驗證，也就是出示祕密。</span><span class="sxs-lookup"><span data-stu-id="79f51-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="79f51-117">為了遵循安全性最佳做法，第一個祕密也必須定期輪替。</span><span class="sxs-lookup"><span data-stu-id="79f51-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="79f51-118">但透過[受控服務識別](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)，在 Azure 中執行的應用程式將會獲得一個由 Azure 自動管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="79f51-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="79f51-119">這有助於解決**祕密導入問題**，如此，使用者/應用程式即可遵循最佳做法，且不需要擔心輪替第一個祕密的問題</span><span class="sxs-lookup"><span data-stu-id="79f51-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="79f51-120">必要條件</span><span class="sxs-lookup"><span data-stu-id="79f51-120">Prerequisites</span></span>

<span data-ttu-id="79f51-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="79f51-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="79f51-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="79f51-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span></span>
* <span data-ttu-id="79f51-123">具有下列工作負載的[Visual Studio 2017 15.7.3 版或更新版本](https://www.microsoft.com/net/download/windows)：</span><span class="sxs-lookup"><span data-stu-id="79f51-123">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="79f51-124">ASP.NET 與 Web 開發</span><span class="sxs-lookup"><span data-stu-id="79f51-124">ASP.NET and web development</span></span>
  * <span data-ttu-id="79f51-125">.NET Core 跨平台開發</span><span class="sxs-lookup"><span data-stu-id="79f51-125">.NET Core cross-platform development</span></span>
* <span data-ttu-id="79f51-126">[.NET Core 2.1 SDK 或更新的版本](https://www.microsoft.com/net/download/windows) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-126">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) ::: zone-end</span></span>
* <span data-ttu-id="79f51-127">Git ([下載](https://git-scm.com/downloads))。</span><span class="sxs-lookup"><span data-stu-id="79f51-127">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="79f51-128">Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="79f51-128">An Azure subscription.</span></span> <span data-ttu-id="79f51-129">如果您沒有 Azure 訂用帳戶，請在開始前建立 [免費帳戶](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)。</span><span class="sxs-lookup"><span data-stu-id="79f51-129">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="79f51-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 2.0.4 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="79f51-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="79f51-131">此工具適用於 Windows、Mac 與 Linux。</span><span class="sxs-lookup"><span data-stu-id="79f51-131">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="79f51-132">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="79f51-132">Login to Azure</span></span>

<span data-ttu-id="79f51-133">若要使用 CLI 登入 Azure，您可以輸入：</span><span class="sxs-lookup"><span data-stu-id="79f51-133">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="79f51-134">建立資源群組</span><span class="sxs-lookup"><span data-stu-id="79f51-134">Create resource group</span></span>

<span data-ttu-id="79f51-135">使用 [az group create](/cli/azure/group#az-group-create) 命令建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="79f51-135">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="79f51-136">Azure 資源群組是可供在其中部署及管理 Azure 資源的邏輯容器。</span><span class="sxs-lookup"><span data-stu-id="79f51-136">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="79f51-137">請選取資源群組名稱，並填入預留位置。</span><span class="sxs-lookup"><span data-stu-id="79f51-137">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="79f51-138">下列範例會在 *eastus* 位置建立名為 <YourResourceGroupName> 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="79f51-138">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="79f51-139">此教學課程中會使用您剛建立的資源群組。</span><span class="sxs-lookup"><span data-stu-id="79f51-139">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="79f51-140">建立 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="79f51-140">Create an Azure Key Vault</span></span>

<span data-ttu-id="79f51-141">接下來，您會使用在上一個步驟中建立的資源群組建立 Key Vault。</span><span class="sxs-lookup"><span data-stu-id="79f51-141">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="79f51-142">雖然 “ContosoKeyVault” 是作為本文中的 Key Vault 名稱使用，但您必須使用唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="79f51-142">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="79f51-143">請提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="79f51-143">Provide the following information:</span></span>

* <span data-ttu-id="79f51-144">Vault 名稱 - **在這裡選取 Key Vault 名稱**。</span><span class="sxs-lookup"><span data-stu-id="79f51-144">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="79f51-145">資源群組名稱 - **在這裡選取資源群組名稱**。</span><span class="sxs-lookup"><span data-stu-id="79f51-145">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="79f51-146">位置 - **美國東部**。</span><span class="sxs-lookup"><span data-stu-id="79f51-146">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="79f51-147">此時，您的 Azure 帳戶是唯一獲得授權在此新保存庫上執行任何作業的帳戶。</span><span class="sxs-lookup"><span data-stu-id="79f51-147">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="79f51-148">將祕密新增至 Key Vault</span><span class="sxs-lookup"><span data-stu-id="79f51-148">Add a secret to key vault</span></span>

<span data-ttu-id="79f51-149">我們將新增祕密，以協助說明其運作方式。</span><span class="sxs-lookup"><span data-stu-id="79f51-149">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="79f51-150">您可能正在儲存 SQL 連接字串，或任何您必須安全保存但可供您的應用程式使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="79f51-150">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="79f51-151">在本教學課程中，密碼會稱為 **AppSecret**，並將在其中儲存 **MySecret** 的值。</span><span class="sxs-lookup"><span data-stu-id="79f51-151">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="79f51-152">輸入下列命令，以在 Key Vault 中建立稱為 **AppSecret** 並將儲存 **MySecret** 值的祕密：</span><span class="sxs-lookup"><span data-stu-id="79f51-152">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="79f51-153">以純文字檢視包含在祕密中的值：</span><span class="sxs-lookup"><span data-stu-id="79f51-153">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="79f51-154">此命令會顯示祕密資訊，包括 URI。</span><span class="sxs-lookup"><span data-stu-id="79f51-154">This command shows the secret information including the URI.</span></span> <span data-ttu-id="79f51-155">完成這些步驟之後，您的 Azure Key Vault 中應該會有祕密的 URI。</span><span class="sxs-lookup"><span data-stu-id="79f51-155">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="79f51-156">寫下此資訊。</span><span class="sxs-lookup"><span data-stu-id="79f51-156">Write this information down.</span></span> <span data-ttu-id="79f51-157">您在稍後的步驟中需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="79f51-157">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="79f51-158">複製存放庫</span><span class="sxs-lookup"><span data-stu-id="79f51-158">Clone the Repo</span></span>

<span data-ttu-id="79f51-159">複製存放庫以便製作本機複本，讓您可以透過執行下列命令以編輯來源：</span><span class="sxs-lookup"><span data-stu-id="79f51-159">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="79f51-160">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="79f51-160">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="79f51-161">安裝相依性</span><span class="sxs-lookup"><span data-stu-id="79f51-161">Install dependencies</span></span>

<span data-ttu-id="79f51-162">我們在此安裝相依性。</span><span class="sxs-lookup"><span data-stu-id="79f51-162">Here we install the dependencies.</span></span> <span data-ttu-id="79f51-163">執行下列命令 cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="79f51-163">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="79f51-164">此專案使用了 2 個節點模組：</span><span class="sxs-lookup"><span data-stu-id="79f51-164">This project used 2 node modules:</span></span>

* [<span data-ttu-id="79f51-165">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="79f51-165">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="79f51-166">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="79f51-166">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="79f51-167">將 Web 應用程式發佈至 Azure</span><span class="sxs-lookup"><span data-stu-id="79f51-167">Publish the web application to Azure</span></span>

<span data-ttu-id="79f51-168">以下是我們必須執行的幾個步驟</span><span class="sxs-lookup"><span data-stu-id="79f51-168">Below are the few steps we need to do</span></span>

* <span data-ttu-id="79f51-169">第 1 個步驟是建立 [Azure App Service](https://azure.microsoft.com/services/app-service/) 方案。</span><span class="sxs-lookup"><span data-stu-id="79f51-169">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="79f51-170">您可以在此方案中儲存多個 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="79f51-170">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="79f51-171">我們會接著建立 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="79f51-171">Next we create a web app.</span></span> <span data-ttu-id="79f51-172">在下列範例中，使用全域唯一應用程式名稱 (有效的字元為 a-z、0-9 與 -) 取代 <app_name>。</span><span class="sxs-lookup"><span data-stu-id="79f51-172">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="79f51-173">執行階段是設定為 NODE|6.9。</span><span class="sxs-lookup"><span data-stu-id="79f51-173">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="79f51-174">若要查看所有支援的執行階段，請執行 az webapp list-runtimes</span><span class="sxs-lookup"><span data-stu-id="79f51-174">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="79f51-175">建立 Web 應用程式後，Azure CLI 會顯示類似下列範例的輸出：</span><span class="sxs-lookup"><span data-stu-id="79f51-175">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="79f51-176">瀏覽至新建立的 Web 應用程式，您應會看到正常運作的 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="79f51-176">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="79f51-177">以唯一應用程式名稱取代 <app_name>。</span><span class="sxs-lookup"><span data-stu-id="79f51-177">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="79f51-178">上述命令也會建立具有 Git 功能的應用程式，讓您從本機 Git 部署至 Azure。</span><span class="sxs-lookup"><span data-stu-id="79f51-178">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="79f51-179">本機 Git 已設定為使用 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git' 的 url</span><span class="sxs-lookup"><span data-stu-id="79f51-179">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="79f51-180">在前一個命令完成後，建立部署使用者，您可以將 Azure 遠端新增至您的本機 Git 存放庫。</span><span class="sxs-lookup"><span data-stu-id="79f51-180">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="79f51-181">使用從「為應用程式啟用 Git」取得的 Git 遠端 URL 取代 <url>。</span><span class="sxs-lookup"><span data-stu-id="79f51-181">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
<span data-ttu-id="79f51-182">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-182">::: zone-end</span></span>

<span data-ttu-id="79f51-183">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="79f51-183">::: zone pivot="dotnet"</span></span>
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="79f51-184">開啟及編輯方案</span><span class="sxs-lookup"><span data-stu-id="79f51-184">Open and edit the solution</span></span>

<span data-ttu-id="79f51-185">編輯 program.cs 檔案，以使用您的特定金鑰保存庫名稱來執行範例：</span><span class="sxs-lookup"><span data-stu-id="79f51-185">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="79f51-186">瀏覽至 key-vault-dotnet-core-quickstart 資料夾。</span><span class="sxs-lookup"><span data-stu-id="79f51-186">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="79f51-187">在 Visual Studio 2017 中開啟 key-vault-dotnet-core-quickstart.sln 檔案。</span><span class="sxs-lookup"><span data-stu-id="79f51-187">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="79f51-188">開啟 Program.cs 檔案，並使用您先前建立的金鑰保存庫名稱更新預留位置 *YourKeyVaultName*。</span><span class="sxs-lookup"><span data-stu-id="79f51-188">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="79f51-189">這個方案會使用 [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) 與 [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet 程式庫。</span><span class="sxs-lookup"><span data-stu-id="79f51-189">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="79f51-190">執行應用程式</span><span class="sxs-lookup"><span data-stu-id="79f51-190">Run the app</span></span>

<span data-ttu-id="79f51-191">在 Visual Studio 2017 的主功能表中，選取 [偵錯] > [啟動但不偵錯]。</span><span class="sxs-lookup"><span data-stu-id="79f51-191">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="79f51-192">在瀏覽器出現時，移至 [關於] 頁面。</span><span class="sxs-lookup"><span data-stu-id="79f51-192">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="79f51-193">**AppSecret** 的值隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="79f51-193">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="79f51-194">將 Web 應用程式發佈至 Azure</span><span class="sxs-lookup"><span data-stu-id="79f51-194">Publish the web application to Azure</span></span>

<span data-ttu-id="79f51-195">將此應用程式發佈至 Azure，以 Web 應用程式的形式即時查看，並確認您可以擷取祕密值：</span><span class="sxs-lookup"><span data-stu-id="79f51-195">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="79f51-196">在 Visual Studio 中，選取 **key-vault-dotnet-core-quickstart** 專案。</span><span class="sxs-lookup"><span data-stu-id="79f51-196">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="79f51-197">選取 [發佈] > [開始]。</span><span class="sxs-lookup"><span data-stu-id="79f51-197">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="79f51-198">建立新的 **App Service**，然後選取 [發佈]。</span><span class="sxs-lookup"><span data-stu-id="79f51-198">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="79f51-199">將應用程式名稱變更為 **keyvaultdotnetcorequickstart**。</span><span class="sxs-lookup"><span data-stu-id="79f51-199">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="79f51-200">選取 [建立]。</span><span class="sxs-lookup"><span data-stu-id="79f51-200">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
<span data-ttu-id="79f51-201">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-201">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="79f51-202">啟用受控服務身分識別</span><span class="sxs-lookup"><span data-stu-id="79f51-202">Enable managed service identities</span></span>

<span data-ttu-id="79f51-203">Azure Key Vault 可安全地儲存認證和其他金鑰及祕密，但是您的程式碼必須向 Azure Key Vault 進行驗證，才能擷取這些項目。</span><span class="sxs-lookup"><span data-stu-id="79f51-203">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="79f51-204">「受控服務識別」可以輕易地解決此問題，因為 MSI 可在 Azure Active Directory (Azure AD) 中將自動受控身分識別提供給 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="79f51-204">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="79f51-205">您可以使用此身分識別來完成任何支援 Azure AD 驗證的服務驗證 (包括 Key Vault)，不需要任何您程式碼中的認證。</span><span class="sxs-lookup"><span data-stu-id="79f51-205">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="79f51-206">返回 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="79f51-206">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="79f51-207">執行 assign-identity 命令來建立此應用程式的身分識別：</span><span class="sxs-lookup"><span data-stu-id="79f51-207">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="79f51-208">此程序中的命令等同於前往入口網站，並在 Web 應用程式屬性中將 [受控服務識別] 切換為 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="79f51-208">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="79f51-209">將權限指派給您的應用程式，以便從 Key Vault 讀取秘密</span><span class="sxs-lookup"><span data-stu-id="79f51-209">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="79f51-210">當您將應用程式發佈至 Azure 時，請記下輸出。</span><span class="sxs-lookup"><span data-stu-id="79f51-210">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="79f51-211">其格式應為：</span><span class="sxs-lookup"><span data-stu-id="79f51-211">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="79f51-212">然後，使用金鑰保存庫的名稱和 **PrincipalId** 的值來執行此命令：</span><span class="sxs-lookup"><span data-stu-id="79f51-212">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="79f51-213">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="79f51-213">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="79f51-214">將 Node 應用程式部署至 Azure 並擷取祕密值</span><span class="sxs-lookup"><span data-stu-id="79f51-214">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="79f51-215">現在一切都已設定。</span><span class="sxs-lookup"><span data-stu-id="79f51-215">Now that everything is set.</span></span> <span data-ttu-id="79f51-216">執行下列命令以將應用程式部署到 Azure</span><span class="sxs-lookup"><span data-stu-id="79f51-216">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="79f51-217">在此之後，當您瀏覽 https://<app_name>.azurewebsites.net 時，您可以看見祕密值。</span><span class="sxs-lookup"><span data-stu-id="79f51-217">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="79f51-218">確定您已用保存庫的名稱取代了名稱 <YourKeyVaultName></span><span class="sxs-lookup"><span data-stu-id="79f51-218">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

<span data-ttu-id="79f51-219">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-219">::: zone-end</span></span>

<span data-ttu-id="79f51-220">現在當您執行應用程式時，您應該會看到擷取的秘密值。</span><span class="sxs-lookup"><span data-stu-id="79f51-220">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="79f51-221">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-221">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="79f51-222">後續步驟</span><span class="sxs-lookup"><span data-stu-id="79f51-222">Next steps</span></span>

<span data-ttu-id="79f51-223">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="79f51-223">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="79f51-224">Azure Key Vault 首頁</span><span class="sxs-lookup"><span data-stu-id="79f51-224">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="79f51-225">Azure Key Vault 文件</span><span class="sxs-lookup"><span data-stu-id="79f51-225">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="79f51-226">Azure SDK For Node</span><span class="sxs-lookup"><span data-stu-id="79f51-226">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="79f51-227">[Azure REST API 參考](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="79f51-228">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="79f51-228">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="79f51-229">Azure Key Vault 首頁</span><span class="sxs-lookup"><span data-stu-id="79f51-229">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="79f51-230">Azure Key Vault 文件</span><span class="sxs-lookup"><span data-stu-id="79f51-230">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="79f51-231">Azure SDK For .NET</span><span class="sxs-lookup"><span data-stu-id="79f51-231">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="79f51-232">[Azure REST API 參考](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="79f51-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>
