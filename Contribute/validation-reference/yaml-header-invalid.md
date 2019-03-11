---
title: yaml-header-invalid
description: Docs 組建問題 yaml-header-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459019"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>警告

`Invalid YAML header: Improper use of a colon in a metadata entry.`

這通常表示 YAML 標頭中不具引號的中繼資料值包含冒號或其他特殊字元。 也可能表示索引鍵/值組中的冒號後面遺漏空格。

## <a name="resolution"></a>解決方式

檢閱您的 YAML 標頭。 尋找下列錯誤。

不具引號值中的冒號：

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

變更為：

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

索引鍵/值組中的冒號後面沒有空格：

```yml
---
title:I omitted a space.
---
```

變更為：

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
