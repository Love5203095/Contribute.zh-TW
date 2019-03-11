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
# <a name="yaml-header-invalid"></a><span data-ttu-id="ae3d5-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="ae3d5-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="ae3d5-104">警告</span><span class="sxs-lookup"><span data-stu-id="ae3d5-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="ae3d5-105">這通常表示 YAML 標頭中不具引號的中繼資料值包含冒號或其他特殊字元。</span><span class="sxs-lookup"><span data-stu-id="ae3d5-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="ae3d5-106">也可能表示索引鍵/值組中的冒號後面遺漏空格。</span><span class="sxs-lookup"><span data-stu-id="ae3d5-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="ae3d5-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="ae3d5-107">Resolution</span></span>

<span data-ttu-id="ae3d5-108">檢閱您的 YAML 標頭。</span><span class="sxs-lookup"><span data-stu-id="ae3d5-108">Review your YAML header.</span></span> <span data-ttu-id="ae3d5-109">尋找下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="ae3d5-109">Look for the following mistakes.</span></span>

<span data-ttu-id="ae3d5-110">不具引號值中的冒號：</span><span class="sxs-lookup"><span data-stu-id="ae3d5-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="ae3d5-111">變更為：</span><span class="sxs-lookup"><span data-stu-id="ae3d5-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="ae3d5-112">索引鍵/值組中的冒號後面沒有空格：</span><span class="sxs-lookup"><span data-stu-id="ae3d5-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="ae3d5-113">變更為：</span><span class="sxs-lookup"><span data-stu-id="ae3d5-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
