---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084438"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="787bf-101">Docs PR 驗證服務</span><span class="sxs-lookup"><span data-stu-id="787bf-101">Docs PR validation service</span></span>

<span data-ttu-id="787bf-102">Docs PR 驗證服務是一項 GitHub 應用程式，可在 PR 中於檔案上執行驗證規則。</span><span class="sxs-lookup"><span data-stu-id="787bf-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="787bf-103">在存放庫上啟用時驗證服務時，您會看到下列行為：</span><span class="sxs-lookup"><span data-stu-id="787bf-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="787bf-104">您提交 PR。</span><span class="sxs-lookup"><span data-stu-id="787bf-104">You submit a PR.</span></span>
1. <span data-ttu-id="787bf-105">在指出您 PR 狀態的 GitHub 註解中，您會看到存放庫上已啟用的「檢查」狀態。</span><span class="sxs-lookup"><span data-stu-id="787bf-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="787bf-106">請注意，在此範例中，有兩項已啟用的檢查：「認可驗證」和「OpenPublishing.Build」：</span><span class="sxs-lookup"><span data-stu-id="787bf-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![有些檢查失敗](media/validation-failed.png)

   <span data-ttu-id="787bf-108">即使認可驗證失敗，建置也可能會通過。</span><span class="sxs-lookup"><span data-stu-id="787bf-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="787bf-109">按一下 [詳細資料] 以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="787bf-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="787bf-110">在 [詳細資料] 頁面上，您會看到所有失敗的驗證檢查，其中包含如何修正問題的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="787bf-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![驗證訊息](media/validation-details.png)

<span data-ttu-id="787bf-112">請參閱本文左側的 TOC，以取得目前服務中的驗證清單。</span><span class="sxs-lookup"><span data-stu-id="787bf-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>