---
title: author-missing
description: author-missing 文件組建問題的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288512"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>警告

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
