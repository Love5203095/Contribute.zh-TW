---
title: author-missing
description: author-missing 文件組建問題的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791526"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: author. Add the current author's GitHub ID.`

`author` 屬性會依 GitHub 識別碼來識別文章的作者。 

## <a name="resolution"></a>解決方式

將目前作者的 GitHub 識別碼新增到 YML 標頭：

```yml
---
author: meganbradley
ms.author: mbradley
---
```

請注意，如果擁有權曾經變更，這應該要是文章的「目前」  擁有者，而不是原始作者。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
