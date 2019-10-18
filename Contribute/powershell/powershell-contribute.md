---
title: 參與 PowerShell 文件存放庫
description: 本文與組成 PowerShell 文件的存放庫相關。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290165"
---
# <a name="contributing-to-powershell-documentation"></a>參與 PowerShell 文件

感謝您對於 PowerShell 文件感到興趣！

本文件涵蓋參與 PowerShell 文件網站上所託管文章和程式碼範例的流程。 這些參與可以是簡單的錯字校正，也可以是複雜的新文章。

PowerShell 文件網站是從包含一或多個 docset 的多個存放庫所建置：

- [PowerShell 概念與 Cmdlet 參考][psdocs]
- PowerShell SDK 程式碼範例 - 包含 SDK 文章中所使用範例的私人存放庫
- [PowerShell .NET SDK 參考](/dotnet/api/?view=pscore-6.2.0) - 從 PowerShell 原始程式碼產生的私人存放庫內容

所有此內容的問題都會在 [PowerShell-Docs][docsrepo] 存放庫進行追蹤。

## <a name="repository-structure"></a>存放庫結構

PowerShell-Docs 存放庫由三個發佈至 [Microsoft Docs][psdocs] 的 docset 組成。Docset 包含在下列資料夾中：

- [/reference/][ref]：包含 PowerShell 所隨附 Cmdlet 的 PowerShell Cmdlet 參考。 會在版本資料夾 (3.0、4.0、5.0、5.1、6 和 7) 中收集參考。 此 docset 不包含隨附於 Windows 或其他 Microsoft 產品中的模組參考。
- [/reference/docs-conceptual][conceptual] - 包含 PowerShell 概念文件。 這包含安裝指示、範例指令碼、做法主題等。
- [/developer/][SDK] - 包含 PowerShell SDK 概念文件。

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
