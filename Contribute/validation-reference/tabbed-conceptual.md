# <a name="tabbed-conceptual"></a><span data-ttu-id="47eb6-101">索引標籤式概念</span><span class="sxs-lookup"><span data-stu-id="47eb6-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47eb6-102">索引標籤式概念語法已淘汰，不應新增索引標籤。</span><span class="sxs-lookup"><span data-stu-id="47eb6-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="47eb6-103">本文所描述的驗證適用於經過核准，可在替代功能推出前使用索引標籤式概念的內容集合。</span><span class="sxs-lookup"><span data-stu-id="47eb6-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="47eb6-104">索引標籤語法</span><span class="sxs-lookup"><span data-stu-id="47eb6-104">Tab syntax</span></span>

<span data-ttu-id="47eb6-105">索引標籤的語法如下：</span><span class="sxs-lookup"><span data-stu-id="47eb6-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="47eb6-106">單一層級索引標籤：</span><span class="sxs-lookup"><span data-stu-id="47eb6-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="47eb6-107">選擇性相依性索引標籤：</span><span class="sxs-lookup"><span data-stu-id="47eb6-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="47eb6-108">範例：具有兩個索引標籤和索引標籤群組結束字元 (---) 的單一層級索引標籤區段：</span><span class="sxs-lookup"><span data-stu-id="47eb6-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="47eb6-109">索引標籤可另外包含次要索引標籤或相依性索引標籤。</span><span class="sxs-lookup"><span data-stu-id="47eb6-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="47eb6-110">這會讓索引標籤相依於另一組索引標籤上的選取項目。</span><span class="sxs-lookup"><span data-stu-id="47eb6-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="47eb6-111">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="47eb6-111">Here's an example:</span></span>

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

<span data-ttu-id="47eb6-112">下列驗證適用於索引標籤語法：</span><span class="sxs-lookup"><span data-stu-id="47eb6-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="47eb6-113">索引標籤語法必須正確。</span><span class="sxs-lookup"><span data-stu-id="47eb6-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="47eb6-114">相依索引標籤必須已於上一個索引標籤群組中受定義。</span><span class="sxs-lookup"><span data-stu-id="47eb6-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="47eb6-115">僅允許一個層級的相依性。</span><span class="sxs-lookup"><span data-stu-id="47eb6-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="47eb6-116">索引標籤數不得少於兩個。</span><span class="sxs-lookup"><span data-stu-id="47eb6-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="47eb6-117">索引標籤數不得多於四個。</span><span class="sxs-lookup"><span data-stu-id="47eb6-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="47eb6-118">索引標籤必須在允許清單內。</span><span class="sxs-lookup"><span data-stu-id="47eb6-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="47eb6-119">索引標籤/識別碼對必須有效。</span><span class="sxs-lookup"><span data-stu-id="47eb6-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="47eb6-120">在同一個索引標籤群組中，不得多次具有相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="47eb6-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="47eb6-121">索引標籤允許清單</span><span class="sxs-lookup"><span data-stu-id="47eb6-121">Tab whitelist</span></span>

<span data-ttu-id="47eb6-122">以下索引標籤/索引標籤識別碼對均已在允許清單內。</span><span class="sxs-lookup"><span data-stu-id="47eb6-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="47eb6-123">相依性索引標籤識別碼不會成對，但在索引標籤識別碼欄位中必須有效。</span><span class="sxs-lookup"><span data-stu-id="47eb6-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="47eb6-124">值會區分大小寫</span><span class="sxs-lookup"><span data-stu-id="47eb6-124">The values are case-sensitive</span></span>

|<span data-ttu-id="47eb6-125">索引標籤名稱</span><span class="sxs-lookup"><span data-stu-id="47eb6-125">Tab name</span></span>              |<span data-ttu-id="47eb6-126">索引標籤識別碼</span><span class="sxs-lookup"><span data-stu-id="47eb6-126">Tab ID</span></span>            |
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