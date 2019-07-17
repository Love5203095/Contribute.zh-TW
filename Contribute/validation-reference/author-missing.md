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
# <a name="author-missing"></a><span data-ttu-id="bc0bb-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="bc0bb-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bc0bb-104">建議</span><span class="sxs-lookup"><span data-stu-id="bc0bb-104">Suggestion</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="bc0bb-105">`author` 屬性會依 GitHub 識別碼來識別文章的作者。</span><span class="sxs-lookup"><span data-stu-id="bc0bb-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="bc0bb-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="bc0bb-106">Resolution</span></span>

<span data-ttu-id="bc0bb-107">將目前作者的 GitHub 識別碼新增到 YML 標頭：</span><span class="sxs-lookup"><span data-stu-id="bc0bb-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="bc0bb-108">請注意，如果擁有權曾經變更，這應該要是文章的「目前」  擁有者，而不是原始作者。</span><span class="sxs-lookup"><span data-stu-id="bc0bb-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
