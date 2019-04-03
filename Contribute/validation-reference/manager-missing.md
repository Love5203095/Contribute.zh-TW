---
title: manager-missing
description: Docs 組建問題 manager-missing 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637245"
---
# <a name="manager-missing"></a>manager-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

某些內容群組需要 `manager` 屬性以識別作者的經理。

## <a name="resolution"></a>解決方式

為 `manager` 新增有效的 Microsoft 別名：

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
