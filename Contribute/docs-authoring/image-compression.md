---
title: 影像壓縮 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來進行影像壓縮。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336650"
---
# <a name="image-compression"></a><span data-ttu-id="3e104-103">影像壓縮</span><span class="sxs-lookup"><span data-stu-id="3e104-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="3e104-104">摘要</span><span class="sxs-lookup"><span data-stu-id="3e104-104">Summary</span></span>

<span data-ttu-id="3e104-105">所有的文件都是透過網路提供，只有 PDF 版本的文件除外。提供靜態內容時，最好能將透過網路傳送的位元組數目降至最低。</span><span class="sxs-lookup"><span data-stu-id="3e104-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="3e104-106">其中一種方法是壓縮待用影像。</span><span class="sxs-lookup"><span data-stu-id="3e104-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="3e104-107">Docs 編寫套件延伸模組包含影像壓縮操作功能表項目。</span><span class="sxs-lookup"><span data-stu-id="3e104-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="3e104-108">支援下列的影像類型/副檔名：</span><span class="sxs-lookup"><span data-stu-id="3e104-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="3e104-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="3e104-109">*\*.png*</span></span>
* <span data-ttu-id="3e104-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="3e104-110">*\*.jpg*</span></span>
* <span data-ttu-id="3e104-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="3e104-111">*\*.jpeg*</span></span>
* <span data-ttu-id="3e104-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="3e104-112">*\*.gif*</span></span>
* <span data-ttu-id="3e104-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="3e104-113">*\*.svg*</span></span>
* <span data-ttu-id="3e104-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="3e104-114">*\*.webp*</span></span>

<span data-ttu-id="3e104-115">在適用的情況下，會使用不失真的影像壓縮演算法。</span><span class="sxs-lookup"><span data-stu-id="3e104-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="3e104-116">壓縮影像</span><span class="sxs-lookup"><span data-stu-id="3e104-116">Compress image</span></span>

<span data-ttu-id="3e104-117">在 [Explorer]  導覽窗格中，以滑鼠右鍵按一下影像檔，然後選取 [壓縮影像]  選項。</span><span class="sxs-lookup"><span data-stu-id="3e104-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="3e104-118">便可壓縮影像。</span><span class="sxs-lookup"><span data-stu-id="3e104-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="3e104-119">壓縮資料夾中的影像</span><span class="sxs-lookup"><span data-stu-id="3e104-119">Compress images in folder</span></span>

<span data-ttu-id="3e104-120">在 [Explorer]  導覽窗格中，以滑鼠右鍵按一下包含影像的資料夾，然後選取 [壓縮資料夾中的影像]  選項。</span><span class="sxs-lookup"><span data-stu-id="3e104-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="3e104-121">便可壓縮資料夾中的所有影像。</span><span class="sxs-lookup"><span data-stu-id="3e104-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="3e104-122">考量</span><span class="sxs-lookup"><span data-stu-id="3e104-122">Considerations</span></span>

<span data-ttu-id="3e104-123">解析度大的影像會默默的調整大小。</span><span class="sxs-lookup"><span data-stu-id="3e104-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="3e104-124">最大尺寸是根據平台建議的最大寬度 `1,200px`。</span><span class="sxs-lookup"><span data-stu-id="3e104-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="3e104-125">只有在影像大於建議的大小時才會使用最大尺寸，而且會在自動調整大小時維持外觀比例。</span><span class="sxs-lookup"><span data-stu-id="3e104-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="3e104-126">喜好設定</span><span class="sxs-lookup"><span data-stu-id="3e104-126">Preferences</span></span>

<span data-ttu-id="3e104-127">您可設定最大尺寸，但預設的最大寬度為 `1200` 像素。</span><span class="sxs-lookup"><span data-stu-id="3e104-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="3e104-128">若要設定最大尺寸，選取 [檔案-> 喜好設定-> 設定]  ，並依 `"Docs Image Extension"` 篩選。</span><span class="sxs-lookup"><span data-stu-id="3e104-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="設定影像壓縮":::

> [!NOTE]
> <span data-ttu-id="3e104-130">[最大寬度]  或 [最大高度]  的值若為 `0`，會直接忽略解析度差異。</span><span class="sxs-lookup"><span data-stu-id="3e104-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="3e104-131">操作實況</span><span class="sxs-lookup"><span data-stu-id="3e104-131">In action</span></span>

<span data-ttu-id="3e104-132">以下是這項功能的簡短示範。</span><span class="sxs-lookup"><span data-stu-id="3e104-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="3e104-133">[![壓縮影像示範](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="3e104-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
