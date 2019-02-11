---
title: author-missing
description: author-missing 文件組建問題的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: cba9788c113101fc93bffa674702b2bed95afbcb
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713031"
---
# <a name="author-missing"></a>author-missing

**即將推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: author. Add a valid GitHub ID.`

`author` 屬性會依 GitHub 識別碼來識別文章的作者。 

## <a name="resolution"></a>解決方式

將作者的 GitHub 識別碼新增至 YML 標頭：

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]