---
title: multiple-values
description: multiple-values 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637314"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

您為只允許一個值的屬性指定多個值。

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

必須以單一值 (scalar) YML 格式指定不允許有多個值的屬性。

## <a name="resolution"></a>解決方式

當多值陣列用於單一值屬性 (不論是單一值屬性具有多個值或陣列中有單一值) 時，您就會收到此建議。

YML 針對多值屬性支援下列陣列格式，例如 `ms.custom`：

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

這些格式對單一值屬性而言無效，例如 `author`。

若您指定多個值，請檢閱指定的值並判斷哪一個是正確的。 移除其他值並在與屬性相同的行上指定單一值，如下所示：

```yml
---
author: meganbradley
---
```

若您有單一值陣列，請將它變更為上面的純量格式。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
