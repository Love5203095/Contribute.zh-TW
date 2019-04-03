---
title: deprecated-attribute
description: deprecated-attribute 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636877"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Deprecated attribute: ms.component. Use ms.subservice instead.`

使用 `ms.service`來指定雲端服務。 若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。 請勿使用 `ms.component`；這對此內容來說已淘汰。

## <a name="resolution"></a>解決方式

確認 `ms.service` 值對您的文章而言是正確的值。 然後選擇一個有效的 `ms.subservice` 值。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
