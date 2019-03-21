---
title: ms-prod-missing
description: ms-prod-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987690"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**即將推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

使用 `ms.prod` 來指定內部部署產品。 若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`，但如果您指定 `ms.technology`，則必須一併指定 `ms.prod`。 `ms.prod` 與 `ms.technology` 的值必須是有效的配對。

## <a name="resolution"></a>解決方式

確認您所指定的 `ms.technology` 值對您的文章而言是正確的值。 然後新增是 `ms.technology` 之有效父系的適當 `ms.prod` 值。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
