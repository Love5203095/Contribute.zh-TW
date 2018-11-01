---
title: Markdown 標題
description: 描述 Markdown 標題的需求。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084428"
---
# <a name="markdown-headings"></a><span data-ttu-id="04122-103">Markdown 標題</span><span class="sxs-lookup"><span data-stu-id="04122-103">Markdown headings</span></span>

<span data-ttu-id="04122-104">下列驗證需求適用於 OPS Markdown 檔案中的標題。</span><span class="sxs-lookup"><span data-stu-id="04122-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="04122-105">H1</span><span class="sxs-lookup"><span data-stu-id="04122-105">H1</span></span>

<span data-ttu-id="04122-106">`H1` 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="04122-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="04122-107">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="04122-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="04122-108">H1 的建立方式為以單一井字 (`#`) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="04122-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="04122-109">例如，本文的 H1 為：</span><span class="sxs-lookup"><span data-stu-id="04122-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="04122-110">下列規則適用於 H1 標題：</span><span class="sxs-lookup"><span data-stu-id="04122-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="04122-111">檔案中必須存在 H1。</span><span class="sxs-lookup"><span data-stu-id="04122-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="04122-112">只能有一個 H1。</span><span class="sxs-lookup"><span data-stu-id="04122-112">There can only be one H1.</span></span>
- <span data-ttu-id="04122-113">H1 必須包含內容。</span><span class="sxs-lookup"><span data-stu-id="04122-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="04122-114">`#` 和 H1 內容間必須有一個空格。</span><span class="sxs-lookup"><span data-stu-id="04122-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="04122-115">不具空格的 H1 將不會在發佈頁面中轉譯為標題。</span><span class="sxs-lookup"><span data-stu-id="04122-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="04122-116">H1 必須是檔案中 YML 中繼資料標頭後的第一個內容。</span><span class="sxs-lookup"><span data-stu-id="04122-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="04122-117">YML 標頭的結尾和 H1 間不允許任何內容 (例如文字或影像)。</span><span class="sxs-lookup"><span data-stu-id="04122-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="04122-118">不應使用第一層標題的 HTML 元素 (`<h1>`)。</span><span class="sxs-lookup"><span data-stu-id="04122-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="04122-119">使用 Markdown 語法 (`# `)。</span><span class="sxs-lookup"><span data-stu-id="04122-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="04122-120">H1 的長度不應超過 100 個字元。</span><span class="sxs-lookup"><span data-stu-id="04122-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="04122-121">此為樣式方針。</span><span class="sxs-lookup"><span data-stu-id="04122-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="04122-122">H2 到 H6</span><span class="sxs-lookup"><span data-stu-id="04122-122">H2 - H6</span></span>

<span data-ttu-id="04122-123">OPS 中允許 H2 (`## `) 到 H6 (`###### `)。</span><span class="sxs-lookup"><span data-stu-id="04122-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="04122-124">請使用 Markdown 標頭，而非 HTML (`<h2>` - `<h6>`) 來建立標題。</span><span class="sxs-lookup"><span data-stu-id="04122-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
