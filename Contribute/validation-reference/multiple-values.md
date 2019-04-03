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
# <a name="multiple-values"></a><span data-ttu-id="41114-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="41114-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="41114-104">建議</span><span class="sxs-lookup"><span data-stu-id="41114-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="41114-105">您為只允許一個值的屬性指定多個值。</span><span class="sxs-lookup"><span data-stu-id="41114-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="41114-106">必須以單一值 (scalar) YML 格式指定不允許有多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="41114-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="41114-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="41114-107">Resolution</span></span>

<span data-ttu-id="41114-108">當多值陣列用於單一值屬性 (不論是單一值屬性具有多個值或陣列中有單一值) 時，您就會收到此建議。</span><span class="sxs-lookup"><span data-stu-id="41114-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="41114-109">YML 針對多值屬性支援下列陣列格式，例如 `ms.custom`：</span><span class="sxs-lookup"><span data-stu-id="41114-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="41114-110">這些格式對單一值屬性而言無效，例如 `author`。</span><span class="sxs-lookup"><span data-stu-id="41114-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="41114-111">若您指定多個值，請檢閱指定的值並判斷哪一個是正確的。</span><span class="sxs-lookup"><span data-stu-id="41114-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="41114-112">移除其他值並在與屬性相同的行上指定單一值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="41114-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="41114-113">若您有單一值陣列，請將它變更為上面的純量格式。</span><span class="sxs-lookup"><span data-stu-id="41114-113">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
