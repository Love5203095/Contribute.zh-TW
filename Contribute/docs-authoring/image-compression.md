---
title: 影像壓縮 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來進行影像壓縮。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336650"
---
# <a name="image-compression"></a>影像壓縮

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>摘要

所有的文件都是透過網路提供，只有 PDF 版本的文件除外。提供靜態內容時，最好能將透過網路傳送的位元組數目降至最低。 其中一種方法是壓縮待用影像。

Docs 編寫套件延伸模組包含影像壓縮操作功能表項目。 支援下列的影像類型/副檔名：

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

在適用的情況下，會使用不失真的影像壓縮演算法。

## <a name="compress-image"></a>壓縮影像

在 [Explorer]  導覽窗格中，以滑鼠右鍵按一下影像檔，然後選取 [壓縮影像]  選項。 便可壓縮影像。

## <a name="compress-images-in-folder"></a>壓縮資料夾中的影像

在 [Explorer]  導覽窗格中，以滑鼠右鍵按一下包含影像的資料夾，然後選取 [壓縮資料夾中的影像]  選項。 便可壓縮資料夾中的所有影像。

## <a name="considerations"></a>考量

解析度大的影像會默默的調整大小。 最大尺寸是根據平台建議的最大寬度 `1,200px`。 只有在影像大於建議的大小時才會使用最大尺寸，而且會在自動調整大小時維持外觀比例。

## <a name="preferences"></a>喜好設定

您可設定最大尺寸，但預設的最大寬度為 `1200` 像素。 若要設定最大尺寸，選取 [檔案-> 喜好設定-> 設定]  ，並依 `"Docs Image Extension"` 篩選。

:::image type="content" source="media/configure-image-compression.png" alt-text="設定影像壓縮":::

> [!NOTE]
> [最大寬度]  或 [最大高度]  的值若為 `0`，會直接忽略解析度差異。

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範。

[![壓縮影像示範](media/compress-image.gif)](media/compress-image.gif#lightbox)
