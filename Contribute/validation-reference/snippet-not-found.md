---
title: snippet-not-found
description: Docs 組建問題 snippet-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 82fc2926f5bc2ec01577670b066b88fb59d7ea11
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459088"
---
# <a name="snippet-not-found"></a>snippet-not-found

## <a name="warning"></a>警告

`Code snippet '{snippet path}' not found.`

指定路徑中不存在程式碼片段參考，或目前檔案中沒有該路徑可用。

## <a name="resolution"></a>解決方式

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

確定您的程式碼片段路徑正確。 如果程式碼片段儲存在目前存放庫外部，請務必將存放庫設定為相依存放庫。 如需詳細資訊，請參閱 Microsoft 內部[程式碼片段文章](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
