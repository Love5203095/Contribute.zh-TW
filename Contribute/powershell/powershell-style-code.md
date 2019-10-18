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
# <a name="formatting-code-samples"></a>格式化程式碼範例

現有文件已使用了多個樣式，且隨著時間經過，格式化規則也已多次進行變更。 我們嘗試為文件中 PowerShell 程式碼區塊和輸出建立一致的樣式。

Markdown 支援兩種不同的程式碼樣式：

- 程式碼範圍 (內嵌) - 以單一反引號 (`` ` ``) 字元標記。 用於在段落中進行內嵌，而非獨立區塊。 最常用在 Cmdlet 名稱周圍。 請參閱[格式化命令語法項目](powershell-style-basic-markdown.md#formatting-command-syntax-elements)。
- 程式碼區塊 - 以三個反引號 (`` ``` ``) 包圍的多行區塊字串。

## <a name="using-code-blocks"></a>使用程式碼區塊

Markdown 允許使用縮排來表示程式碼區塊，但這種模式可能會產生問題，因此應盡量避免。 所有程式碼區塊都應包含在程式碼柵欄內。 程式碼柵欄是由三個反引號 (`` ``` ``) 包圍的程式碼區塊字串。 程式碼柵欄標記在程式碼範例之前和之後都必須位於獨立的一行。 程式碼區塊開頭的標記可以包含選擇性語言標籤。 Microsoft 的開放式發行系統 (OPS) 會使用語言標籤來支援語法醒目提示功能。

OPS 也會新增一個 [複製]  按鈕，可將程式碼區塊的內容複製到剪貼簿。 這可以讓您快速地將程式碼貼入指令碼以測試程式碼範例。 但是，並非所有我們文件中的範例都旨在透過這種方式執行。 某些程式碼區塊可能只是 PowerShell 概念的簡易插畫或語法抽象表示法。

我們的文件中使用了兩種程式碼區塊：

1. 說明範例
2. 可執行檔範例

## <a name="formatting-illustrative-examples"></a>格式化說明範例

說明範例會用來解釋 PowerShell 概念。 它們並非用來複製到剪貼簿並用於執行。 這些最常用於容易鍵入的簡易範例。
它們也會用於說明命令語法的語法範例。

說明範例會使用「裸」程式碼柵欄來標記程式碼區塊的開頭和結尾。 程式碼區塊可能會包含所說明命令的範例輸出。

### <a name="syntax-block"></a>語法區塊

此範例會說明 `Get-Command` Cmdlet 所有可能的參數。

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

此範例會以通用字詞描述 `for` 陳述式：

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>簡易插畫範例

以下是說明 PowerShell 比較運算子的範例：

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

請注意，此範例包含經簡化的 PowerShell 提示，並會顯示結果輸出。 在此情況下，我們並不意圖讓讀者複製和執行此範例。

## <a name="formatting-executable-examples"></a>格式化可執行檔範例

更複雜的範例或是在複製和執行後會更為有用範例，則應使用下列區塊樣式標記：

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

PowerShell 命令顯示的輸出應括在 **Output** 程式碼區塊中，以防止語法醒目提示。 例如：

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

**Output** 程式碼標籤並非語法醒目提示系統支援的正式「語言」。
但是，由於 OPS 會將「輸出」標籤新增到網頁上的程式碼方塊，因此這個標籤相當有用。
且此「輸出」程式碼方塊將不會包含語法醒目提示。

## <a name="coding-style-rules"></a>樣式規則編碼

### <a name="avoid-line-continuation-in-code-samples"></a>在程式碼範例中避免行接續

避免在 PowerShell 程式碼範例中使用行接續字元 (`` ` ``)。 這些項目難以查看，且可能會在行的結尾包含額外空格時造成問題。

- 使用 PowerShell 展開來減少包含許多參數 Cmdlet 的行長度。
- 利用 PowerShell 的自然斷行機會，例如在直立線 (`|`) 符號、左括弧、括弧和中括弧之後。

### <a name="avoid-using-powershell-prompts-in-examples"></a>避免在範例中使用 PowerShell 提示

不建議使用提示字串，且應該將使用範圍限制在用於說明命令列的使用方式。 針對說明會改變提示命令的範例，或是所顯示路徑對所說明案例相當重要時，提示為必要項目。

- PowerShell 提示應僅用於說明範例。 針對大多數的這些範例，提示字串應為 "`PS>`"。 此提示與 OS 特定的指標無關。
- 提示「不應」  用於可執行檔範例。

下列範例會說明在使用登錄提供者時提示的變更方式。

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

### <a name="do-not-use-aliases-in-examples"></a>請不要在範例中使用別名

除非您正在討論別名，否則請一律使用所有 Cmdlet 和參數的完整名稱。 Cmdlet 和參數名稱必須使用程式碼中所定義適當的 Pascal 命名法拼字。

### <a name="using-parameters-in-examples"></a>在範例中使用參數

避免使用位置參數。 一般而言，您應在範例中一律包含參數名稱，即使參數是位置參數也一樣。 這會減少您範例中造成混淆的機會。
