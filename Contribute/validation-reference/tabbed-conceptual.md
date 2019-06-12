---
ms.date: 03/29/2019
title: 索引標籤式概念
ms.openlocfilehash: 3d6f38c1659297182a8bd50bf52b9853bd21b2c8
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841290"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="1e51a-102">索引標籤式概念</span><span class="sxs-lookup"><span data-stu-id="1e51a-102">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e51a-103">索引標籤式概念語法已淘汰，不應新增索引標籤。</span><span class="sxs-lookup"><span data-stu-id="1e51a-103">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="1e51a-104">本文所描述的驗證適用於經過核准，可在替代功能推出前使用索引標籤式概念的內容集合。</span><span class="sxs-lookup"><span data-stu-id="1e51a-104">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="1e51a-105">索引標籤語法</span><span class="sxs-lookup"><span data-stu-id="1e51a-105">Tab syntax</span></span>

<span data-ttu-id="1e51a-106">索引標籤的語法如下：</span><span class="sxs-lookup"><span data-stu-id="1e51a-106">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="1e51a-107">單一層級索引標籤：</span><span class="sxs-lookup"><span data-stu-id="1e51a-107">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="1e51a-108">選擇性相依性索引標籤：</span><span class="sxs-lookup"><span data-stu-id="1e51a-108">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="1e51a-109">範例：具有兩個索引標籤和索引標籤群組結束字元 (---) 的單一層級索引標籤區段：</span><span class="sxs-lookup"><span data-stu-id="1e51a-109">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="1e51a-110">索引標籤可另外包含次要索引標籤或相依性索引標籤。</span><span class="sxs-lookup"><span data-stu-id="1e51a-110">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="1e51a-111">這會讓索引標籤相依於另一組索引標籤上的選取項目。</span><span class="sxs-lookup"><span data-stu-id="1e51a-111">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="1e51a-112">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="1e51a-112">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="1e51a-113">下列驗證適用於索引標籤語法：</span><span class="sxs-lookup"><span data-stu-id="1e51a-113">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="1e51a-114">索引標籤語法必須正確。</span><span class="sxs-lookup"><span data-stu-id="1e51a-114">Tab syntax must be correct.</span></span>
- <span data-ttu-id="1e51a-115">相依索引標籤必須已於上一個索引標籤群組中受定義。</span><span class="sxs-lookup"><span data-stu-id="1e51a-115">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="1e51a-116">僅允許一個層級的相依性。</span><span class="sxs-lookup"><span data-stu-id="1e51a-116">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="1e51a-117">索引標籤數不得少於兩個。</span><span class="sxs-lookup"><span data-stu-id="1e51a-117">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="1e51a-118">索引標籤數不得多於四個。</span><span class="sxs-lookup"><span data-stu-id="1e51a-118">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="1e51a-119">索引標籤必須經過核准。</span><span class="sxs-lookup"><span data-stu-id="1e51a-119">Tabs must be approved.</span></span>
- <span data-ttu-id="1e51a-120">索引標籤/識別碼對必須有效。</span><span class="sxs-lookup"><span data-stu-id="1e51a-120">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="1e51a-121">在同一個索引標籤群組中，不得多次具有相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e51a-121">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="1e51a-122">核准的索引標籤</span><span class="sxs-lookup"><span data-stu-id="1e51a-122">Approved tabs</span></span>

<span data-ttu-id="1e51a-123">下列索引標籤名稱/索引標籤識別碼組合已經過核准。</span><span class="sxs-lookup"><span data-stu-id="1e51a-123">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="1e51a-124">相依性索引標籤識別碼不會成對，但在索引標籤識別碼欄位中必須有效。</span><span class="sxs-lookup"><span data-stu-id="1e51a-124">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="1e51a-125">值會區分大小寫</span><span class="sxs-lookup"><span data-stu-id="1e51a-125">The values are case-sensitive</span></span>

|<span data-ttu-id="1e51a-126">索引標籤名稱</span><span class="sxs-lookup"><span data-stu-id="1e51a-126">Tab name</span></span>              |<span data-ttu-id="1e51a-127">索引標籤識別碼</span><span class="sxs-lookup"><span data-stu-id="1e51a-127">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |