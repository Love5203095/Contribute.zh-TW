---
title: ms-prod-and-service
description: ms-prod-and-service 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 77c0dd71cf526ee837799bcd01e21290ce7d6058
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636739"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>解決方式

需要 `ms.prod` 或 `ms.service` 其中之一，不可同時存在：`ms.prod` 用於內部部署產品；`ms.service` 則用於雲端服務。 請判斷哪一個適合您的文章，確認值正確，然後移除另一個欄位。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
