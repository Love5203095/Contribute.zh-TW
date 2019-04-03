---
title: ms-service-and-subservice-invalid
description: ms-service-and-subservice-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637291"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

使用 `ms.service`來指定雲端服務。 若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。 `ms.service` 與 `ms.subservice` 的值必須是有效的配對。 您的 `ms.service` 值無效，或您的 `ms.subservice` 值不是 `ms.service` 的有效配對。

## <a name="resolution"></a>解決方式

確認 `ms.service` 值對您的文章而言是正確的值。 然後選擇一個有效的 `ms.subservice` 值。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
