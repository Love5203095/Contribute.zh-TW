---
title: manager-invalid
description: Docs 組建問題 manager-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637222"
---
# <a name="manager-invalid"></a>manager-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

某些內容群組需要 `manager` 屬性以識別作者的經理。

## <a name="resolution"></a>解決方式

`manager` 的值必須是個別 Microsoft 員工的有效別名。 確認作者的經理別名，並更新該值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
