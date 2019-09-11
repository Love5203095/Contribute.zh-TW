---
title: author-missing
description: author-missing 文件組建問題的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848577"
---
# <a name="author-missing"></a><span data-ttu-id="4d37a-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="4d37a-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="4d37a-104">警告</span><span class="sxs-lookup"><span data-stu-id="4d37a-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="4d37a-105">`author` 屬性會依 GitHub 識別碼來識別文章的作者。</span><span class="sxs-lookup"><span data-stu-id="4d37a-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="4d37a-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="4d37a-106">Resolution</span></span>

<span data-ttu-id="4d37a-107">將目前作者的 GitHub 識別碼新增到 YML 標頭：</span><span class="sxs-lookup"><span data-stu-id="4d37a-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="4d37a-108">請注意，如果擁有權曾經變更，這應該要是文章的「目前」  擁有者，而不是原始作者。</span><span class="sxs-lookup"><span data-stu-id="4d37a-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
