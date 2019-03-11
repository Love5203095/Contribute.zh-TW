---
title: included-file-redirected
description: Docs 組建問題 included-file-redirected 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459065"
---
# <a name="included-file-redirected"></a><span data-ttu-id="e61ca-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="e61ca-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="e61ca-104">警告</span><span class="sxs-lookup"><span data-stu-id="e61ca-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="e61ca-105">解決方式</span><span class="sxs-lookup"><span data-stu-id="e61ca-105">Resolution</span></span>

<span data-ttu-id="e61ca-106">重新建構您的內容，讓您不包括重新導向的檔案。</span><span class="sxs-lookup"><span data-stu-id="e61ca-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="e61ca-107">例如，建立新的檔案以包含或移除包含的內容參考和連結，或是將它內嵌寫入。</span><span class="sxs-lookup"><span data-stu-id="e61ca-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
