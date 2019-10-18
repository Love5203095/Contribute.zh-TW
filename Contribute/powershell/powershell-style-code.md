---
title: 撰寫指令碼範例的特定指導
description: 本文提供格式化 PowerShell 程式碼範例的特定規則。 這適用於包含範例的概念文章，以及 Cmdlet 參考。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290257"
---
# <a name="formatting-code-samples"></a><span data-ttu-id="b0b7b-104">格式化程式碼範例</span><span class="sxs-lookup"><span data-stu-id="b0b7b-104">Formatting code samples</span></span>

<span data-ttu-id="b0b7b-105">現有文件已使用了多個樣式，且隨著時間經過，格式化規則也已多次進行變更。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="b0b7b-106">我們嘗試為文件中 PowerShell 程式碼區塊和輸出建立一致的樣式。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="b0b7b-107">Markdown 支援兩種不同的程式碼樣式：</span><span class="sxs-lookup"><span data-stu-id="b0b7b-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="b0b7b-108">程式碼範圍 (內嵌) - 以單一反引號 (`` ` ``) 字元標記。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="b0b7b-109">用於在段落中進行內嵌，而非獨立區塊。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="b0b7b-110">最常用在 Cmdlet 名稱周圍。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="b0b7b-111">請參閱[格式化命令語法項目](powershell-style-basic-markdown.md#formatting-command-syntax-elements)。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="b0b7b-112">程式碼區塊 - 以三個反引號 (`` ``` ``) 包圍的多行區塊字串。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="b0b7b-113">使用程式碼區塊</span><span class="sxs-lookup"><span data-stu-id="b0b7b-113">Using code blocks</span></span>

<span data-ttu-id="b0b7b-114">Markdown 允許使用縮排來表示程式碼區塊，但這種模式可能會產生問題，因此應盡量避免。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="b0b7b-115">所有程式碼區塊都應包含在程式碼柵欄內。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="b0b7b-116">程式碼柵欄是由三個反引號 (`` ``` ``) 包圍的程式碼區塊字串。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="b0b7b-117">程式碼柵欄標記在程式碼範例之前和之後都必須位於獨立的一行。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="b0b7b-118">程式碼區塊開頭的標記可以包含選擇性語言標籤。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="b0b7b-119">Microsoft 的開放式發行系統 (OPS) 會使用語言標籤來支援語法醒目提示功能。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="b0b7b-120">OPS 也會新增一個 [複製]  按鈕，可將程式碼區塊的內容複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="b0b7b-121">這可以讓您快速地將程式碼貼入指令碼以測試程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="b0b7b-122">但是，並非所有我們文件中的範例都旨在透過這種方式執行。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="b0b7b-123">某些程式碼區塊可能只是 PowerShell 概念的簡易插畫或語法抽象表示法。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="b0b7b-124">我們的文件中使用了兩種程式碼區塊：</span><span class="sxs-lookup"><span data-stu-id="b0b7b-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="b0b7b-125">說明範例</span><span class="sxs-lookup"><span data-stu-id="b0b7b-125">Illustrative examples</span></span>
2. <span data-ttu-id="b0b7b-126">可執行檔範例</span><span class="sxs-lookup"><span data-stu-id="b0b7b-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="b0b7b-127">格式化說明範例</span><span class="sxs-lookup"><span data-stu-id="b0b7b-127">Formatting illustrative examples</span></span>

<span data-ttu-id="b0b7b-128">說明範例會用來解釋 PowerShell 概念。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="b0b7b-129">它們並非用來複製到剪貼簿並用於執行。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="b0b7b-130">這些最常用於容易鍵入的簡易範例。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="b0b7b-131">它們也會用於說明命令語法的語法範例。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="b0b7b-132">說明範例會使用「裸」程式碼柵欄來標記程式碼區塊的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="b0b7b-133">程式碼區塊可能會包含所說明命令的範例輸出。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="b0b7b-134">語法區塊</span><span class="sxs-lookup"><span data-stu-id="b0b7b-134">Syntax block</span></span>

<span data-ttu-id="b0b7b-135">此範例會說明 `Get-Command` Cmdlet 所有可能的參數。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="b0b7b-136">此範例會以通用字詞描述 `for` 陳述式：</span><span class="sxs-lookup"><span data-stu-id="b0b7b-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="b0b7b-137">簡易插畫範例</span><span class="sxs-lookup"><span data-stu-id="b0b7b-137">Simple illustration example</span></span>

<span data-ttu-id="b0b7b-138">以下是說明 PowerShell 比較運算子的範例：</span><span class="sxs-lookup"><span data-stu-id="b0b7b-138">Here is an example illustrating PowerShell comparison operators:</span></span>

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

<span data-ttu-id="b0b7b-139">請注意，此範例包含經簡化的 PowerShell 提示，並會顯示結果輸出。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="b0b7b-140">在此情況下，我們並不意圖讓讀者複製和執行此範例。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="b0b7b-141">格式化可執行檔範例</span><span class="sxs-lookup"><span data-stu-id="b0b7b-141">Formatting executable examples</span></span>

<span data-ttu-id="b0b7b-142">更複雜的範例或是在複製和執行後會更為有用範例，則應使用下列區塊樣式標記：</span><span class="sxs-lookup"><span data-stu-id="b0b7b-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="b0b7b-143">PowerShell 命令顯示的輸出應括在 **Output** 程式碼區塊中，以防止語法醒目提示。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="b0b7b-144">例如：</span><span class="sxs-lookup"><span data-stu-id="b0b7b-144">For example:</span></span>

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

<span data-ttu-id="b0b7b-145">**Output** 程式碼標籤並非語法醒目提示系統支援的正式「語言」。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="b0b7b-146">但是，由於 OPS 會將「輸出」標籤新增到網頁上的程式碼方塊，因此這個標籤相當有用。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="b0b7b-147">且此「輸出」程式碼方塊將不會包含語法醒目提示。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="b0b7b-148">樣式規則編碼</span><span class="sxs-lookup"><span data-stu-id="b0b7b-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="b0b7b-149">在程式碼範例中避免行接續</span><span class="sxs-lookup"><span data-stu-id="b0b7b-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="b0b7b-150">避免在 PowerShell 程式碼範例中使用行接續字元 (`` ` ``)。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="b0b7b-151">這些項目難以查看，且可能會在行的結尾包含額外空格時造成問題。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="b0b7b-152">使用 PowerShell 展開來減少包含許多參數 Cmdlet 的行長度。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="b0b7b-153">利用 PowerShell 的自然斷行機會，例如在直立線 (`|`) 符號、左括弧、括弧和中括弧之後。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="b0b7b-154">避免在範例中使用 PowerShell 提示</span><span class="sxs-lookup"><span data-stu-id="b0b7b-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="b0b7b-155">不建議使用提示字串，且應該將使用範圍限制在用於說明命令列的使用方式。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="b0b7b-156">針對說明會改變提示命令的範例，或是所顯示路徑對所說明案例相當重要時，提示為必要項目。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="b0b7b-157">PowerShell 提示應僅用於說明範例。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="b0b7b-158">針對大多數的這些範例，提示字串應為 "`PS>`"。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="b0b7b-159">此提示與 OS 特定的指標無關。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="b0b7b-160">提示「不應」  用於可執行檔範例。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="b0b7b-161">下列範例會說明在使用登錄提供者時提示的變更方式。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="b0b7b-162">請不要在範例中使用別名</span><span class="sxs-lookup"><span data-stu-id="b0b7b-162">Do not use aliases in examples</span></span>

<span data-ttu-id="b0b7b-163">除非您正在討論別名，否則請一律使用所有 Cmdlet 和參數的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="b0b7b-164">Cmdlet 和參數名稱必須使用程式碼中所定義適當的 Pascal 命名法拼字。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="b0b7b-165">在範例中使用參數</span><span class="sxs-lookup"><span data-stu-id="b0b7b-165">Using parameters in examples</span></span>

<span data-ttu-id="b0b7b-166">避免使用位置參數。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-166">Avoid using positional parameters.</span></span> <span data-ttu-id="b0b7b-167">一般而言，您應在範例中一律包含參數名稱，即使參數是位置參數也一樣。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="b0b7b-168">這會減少您範例中造成混淆的機會。</span><span class="sxs-lookup"><span data-stu-id="b0b7b-168">This reduces the chance of confusion in your examples.</span></span>
