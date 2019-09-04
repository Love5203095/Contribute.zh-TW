---
title: title-missing
description: title-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
ms.openlocfilehash: cfe942be4285bb22f5fa08fa882077ea790fd2c4
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236560"
---
# <a name="title-missing"></a>title-missing

## <a name="warning"></a>警告

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a>解決方式

新增要在搜尋結果中顯示的標題字串。 一般來說，標題應該介於 19 到 59 個字元之間，應和文章的 H1 區隔，且應包含相關的品牌文字。 您不應在標題中包含 " | Microsoft Docs"，此項目會由 Docs 自動新增，如果明確新增將會受到忽略。 如果希望在內容集的所有標題中新增其他品牌 (如 " - Azure")，請於全域或單一資料夾設定 `titleSuffix` 中繼資料值。

您可以在 [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag) 上預覽標題在 Google 中看起來的樣子。

如果您是 Microsoft 員工，請參閱內部《參與者指南》中的 [SEO 基本知識](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master)，以了解有關良好標題和搜尋引擎最佳化 (SEO) 的詳細資訊。

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
