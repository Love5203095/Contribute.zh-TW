---
title: author-missing
description: author-missing 文件組建問題的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6c7306cf674a345b25d3e05c4e00662623c44469
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637429"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: author. Add a valid GitHub ID.`

`author` 屬性會依 GitHub 識別碼來識別文章的作者。 

## <a name="resolution"></a>解決方式

將作者的 GitHub 識別碼新增至 YML 標頭：

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]