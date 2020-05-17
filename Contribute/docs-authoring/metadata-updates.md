---
title: 中繼資料更新 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來更新中繼資料。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336627"
---
# <a name="update-metadata"></a><span data-ttu-id="0a59c-103">更新中繼資料</span><span class="sxs-lookup"><span data-stu-id="0a59c-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="0a59c-104">摘要</span><span class="sxs-lookup"><span data-stu-id="0a59c-104">Summary</span></span>

<span data-ttu-id="0a59c-105">在 Markdown (.md *\** ) 檔案中，有兩個中繼資料專用的操作功能表項目。</span><span class="sxs-lookup"><span data-stu-id="0a59c-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="0a59c-106">當您以滑鼠右鍵按一下文字編輯器中的任何位置，會看到類似以下的功能表項目：</span><span class="sxs-lookup"><span data-stu-id="0a59c-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="更新中繼資料操作功能表":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="0a59c-108">更新 `ms.date` 中繼資料值</span><span class="sxs-lookup"><span data-stu-id="0a59c-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="0a59c-109">選取 [更新 `ms.date` 中繼資料值]  選項會將目前的 Markdown 檔案 `ms.date` 值設定為今天的日期。</span><span class="sxs-lookup"><span data-stu-id="0a59c-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="0a59c-110">如果文件中沒有 `ms.date` 中繼資料欄位，就不會有任何動作。</span><span class="sxs-lookup"><span data-stu-id="0a59c-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="0a59c-111">更新隱含的中繼資料值</span><span class="sxs-lookup"><span data-stu-id="0a59c-111">Update implicit metadata values</span></span>

<span data-ttu-id="0a59c-112">選取 更新隱含中繼資料值  選項將會尋找並取代所有可能隱含指定的中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="0a59c-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="0a59c-113">隱含的中繼資料值是在 `build/fileMetadata` 節點下的 docfx.json  檔案中指定。</span><span class="sxs-lookup"><span data-stu-id="0a59c-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="0a59c-114">`fileMetadata` 節點中的每個索引鍵值組都代表中繼資料預設值。</span><span class="sxs-lookup"><span data-stu-id="0a59c-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="0a59c-115">例如，在省略 `ms.author` 中繼資料值的 top-level/sub-folder  目錄之中的 Markdown 檔案，可以隱含地指定要在 `fileMetadata` 節點中使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="0a59c-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="0a59c-116">在此案例中，所有 Markdown 檔案都會隱含地採用 `ms.author: dapine` 中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="0a59c-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="0a59c-117">此功能會作用在 docfx.json  檔案中找到的這些隱含設定。</span><span class="sxs-lookup"><span data-stu-id="0a59c-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="0a59c-118">如果 Markdown 檔案包含的中繼資料和值明確設定為隱含值以外的值，便會覆寫隱含值。</span><span class="sxs-lookup"><span data-stu-id="0a59c-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="0a59c-119">請看以下 Markdown 檔案中繼資料 (Markdown 檔案位於 **top-level/sub-folder/includes/example.md**)：</span><span class="sxs-lookup"><span data-stu-id="0a59c-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="0a59c-120">如果已在這個檔案上執行 [更新隱含的中繼資料值]  選項，再加上前述指定的 docfx.json  內容，則中繼資料值會更新為 `ms.author: dapine`。</span><span class="sxs-lookup"><span data-stu-id="0a59c-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="0a59c-121">操作實況</span><span class="sxs-lookup"><span data-stu-id="0a59c-121">In action</span></span>

<span data-ttu-id="0a59c-122">以下是這項功能的簡短示範。</span><span class="sxs-lookup"><span data-stu-id="0a59c-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="0a59c-123">[![更新中繼資料示範](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0a59c-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
