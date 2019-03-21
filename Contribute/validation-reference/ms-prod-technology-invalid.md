---
title: ms-prod-and-technology-invalid
description: ms-prod-and-technology-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987575"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**即將推出！**

## <a name="warning"></a>警告

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

使用 `ms.prod` 來指定內部部署產品。 若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`。 `ms.prod` 與 `ms.technology` 的值必須是有效的配對。 您的 `ms.prod` 值無效，或您的 `ms.technology` 值不是 `ms.prod` 的有效配對。

## <a name="resolution"></a>解決方式

確認 `ms.prod` 值對您的文章而言是正確的值。 然後選擇一個有效的 `ms.technology` 值。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
