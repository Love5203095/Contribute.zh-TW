---
title: ms-prod-service-mismatch
description: ms-prod-service-mismatch 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987607"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**即將推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

使用 `ms.prod` 來指定內部部署產品；`ms.service` 則用於雲端服務。 若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`。 若要指定有關 `ms.service` 的更詳細資訊，您可以指定 `ms.subservice`。 您無法將 `ms.prod` 與 `ms.subservice` 搭配使用，或將 `ms.service` 與 `ms.technology`搭配使用。

## <a name="resolution"></a>解決方式

首先，確認您已為文章選取正確的父屬性 (`ms.prod` 或 `ms.service`)。 接著，新增具有有效配對值的適當子欄位。 移除任何額外的欄位。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
