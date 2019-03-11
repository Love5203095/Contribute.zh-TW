---
title: hard-coded-locale
description: Docs 組建問題 hard-coded-locale 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427204"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="1496f-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="1496f-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="1496f-104">警告</span><span class="sxs-lookup"><span data-stu-id="1496f-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="1496f-105">地區設定代碼 (例如 `en-us`) 不應包含在前往特定 Microsoft 網站的連結中。</span><span class="sxs-lookup"><span data-stu-id="1496f-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="1496f-106">若您在英文內容中的連結內包含地區設定代碼，它也會包含在當地語系化連結中，導致不良的當地語系化體驗。</span><span class="sxs-lookup"><span data-stu-id="1496f-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="1496f-107">例如，若德文當地語系化內容中的連結包含 `en-us`，則德國客戶會發現連結將他們導向英文文章 (即使有可用的德文版本)。</span><span class="sxs-lookup"><span data-stu-id="1496f-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="1496f-108">下列網站皆位於此驗證的範圍中：</span><span class="sxs-lookup"><span data-stu-id="1496f-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="1496f-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1496f-109">azure.microsoft.com</span></span>
- <span data-ttu-id="1496f-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1496f-110">docs.microsoft.com</span></span>
- <span data-ttu-id="1496f-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1496f-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="1496f-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1496f-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="1496f-113">解決方式</span><span class="sxs-lookup"><span data-stu-id="1496f-113">Resolution</span></span>

<span data-ttu-id="1496f-114">請從前往 Microsoft 網站的連結移除地區設定代碼。</span><span class="sxs-lookup"><span data-stu-id="1496f-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="1496f-115">下列為範例。</span><span class="sxs-lookup"><span data-stu-id="1496f-115">The following is an example.</span></span>

<span data-ttu-id="1496f-116">之前：</span><span class="sxs-lookup"><span data-stu-id="1496f-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="1496f-117">之後：</span><span class="sxs-lookup"><span data-stu-id="1496f-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]