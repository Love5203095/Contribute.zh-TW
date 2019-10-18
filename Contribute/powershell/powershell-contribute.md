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
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="5a15b-103">參與 PowerShell 文件</span><span class="sxs-lookup"><span data-stu-id="5a15b-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="5a15b-104">感謝您對於 PowerShell 文件感到興趣！</span><span class="sxs-lookup"><span data-stu-id="5a15b-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="5a15b-105">本文件涵蓋參與 PowerShell 文件網站上所託管文章和程式碼範例的流程。</span><span class="sxs-lookup"><span data-stu-id="5a15b-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="5a15b-106">這些參與可以是簡單的錯字校正，也可以是複雜的新文章。</span><span class="sxs-lookup"><span data-stu-id="5a15b-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="5a15b-107">PowerShell 文件網站是從包含一或多個 docset 的多個存放庫所建置：</span><span class="sxs-lookup"><span data-stu-id="5a15b-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="5a15b-108">[PowerShell 概念與 Cmdlet 參考][psdocs]</span><span class="sxs-lookup"><span data-stu-id="5a15b-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="5a15b-109">PowerShell SDK 程式碼範例 - 包含 SDK 文章中所使用範例的私人存放庫</span><span class="sxs-lookup"><span data-stu-id="5a15b-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="5a15b-110">[PowerShell .NET SDK 參考](/dotnet/api/?view=pscore-6.2.0) - 從 PowerShell 原始程式碼產生的私人存放庫內容</span><span class="sxs-lookup"><span data-stu-id="5a15b-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="5a15b-111">所有此內容的問題都會在 [PowerShell-Docs][docsrepo] 存放庫進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="5a15b-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="5a15b-112">存放庫結構</span><span class="sxs-lookup"><span data-stu-id="5a15b-112">Repository Structure</span></span>

<span data-ttu-id="5a15b-113">PowerShell-Docs 存放庫由三個發佈至 [Microsoft Docs][psdocs] 的 docset 組成。Docset 包含在下列資料夾中：</span><span class="sxs-lookup"><span data-stu-id="5a15b-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="5a15b-114">[/reference/][ref]：包含 PowerShell 所隨附 Cmdlet 的 PowerShell Cmdlet 參考。</span><span class="sxs-lookup"><span data-stu-id="5a15b-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="5a15b-115">會在版本資料夾 (3.0、4.0、5.0、5.1、6 和 7) 中收集參考。</span><span class="sxs-lookup"><span data-stu-id="5a15b-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="5a15b-116">此 docset 不包含隨附於 Windows 或其他 Microsoft 產品中的模組參考。</span><span class="sxs-lookup"><span data-stu-id="5a15b-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="5a15b-117">[/reference/docs-conceptual][conceptual] - 包含 PowerShell 概念文件。</span><span class="sxs-lookup"><span data-stu-id="5a15b-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="5a15b-118">這包含安裝指示、範例指令碼、做法主題等。</span><span class="sxs-lookup"><span data-stu-id="5a15b-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="5a15b-119">[/developer/][SDK] - 包含 PowerShell SDK 概念文件。</span><span class="sxs-lookup"><span data-stu-id="5a15b-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
