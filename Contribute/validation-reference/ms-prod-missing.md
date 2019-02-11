---
title: ms-prod-missing
description: ms-prod-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713215"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**即將推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

使用 `ms.prod` 來指定內部部署產品。 若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`，但如果您指定 `ms.technology`，則必須一併指定 `ms.prod`。 `ms.prod` 與 `ms.technology` 的值必須是有效的配對。

## <a name="resolution"></a>解決方式

確認您所指定的 `ms.technology` 值對您的文章而言是正確的值。 然後新增是 `ms.technology` 之有效父系的適當 `ms.prod` 值。

您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
