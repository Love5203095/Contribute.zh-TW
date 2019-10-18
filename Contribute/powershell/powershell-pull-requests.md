---
title: 提交提取要求
description: 本文描述 PR 流程和確保您的貢獻可供合併的最佳做法。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 09b9fd1057a32c8d2755e07cac564eca417bd357
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290073"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="8c905-103">提取要求的最佳做法</span><span class="sxs-lookup"><span data-stu-id="8c905-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="8c905-104">若要將變更發行到內容，您必須從您的分叉提交提取要求。</span><span class="sxs-lookup"><span data-stu-id="8c905-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="8c905-105">每個提取要求都必須在合併前經過檢閱。</span><span class="sxs-lookup"><span data-stu-id="8c905-105">Every pull request has to be reviewed before it can merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="8c905-106">以正確的分支為目標</span><span class="sxs-lookup"><span data-stu-id="8c905-106">Target the correct branch</span></span>

<span data-ttu-id="8c905-107">所有變更都應在 `staging` 分支進行。</span><span class="sxs-lookup"><span data-stu-id="8c905-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="8c905-108">變更永遠都不應該以 `live` 分支為目標。</span><span class="sxs-lookup"><span data-stu-id="8c905-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="8c905-109">在 `staging` 分支中進行的變更會合併到 `live`，因此任何對 `live` 進行的變更都會遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="8c905-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="8c905-110">若您正在提交對文件進行的變更，且該變更僅適用於尚未發行的 PowerShell 版本，請檢查是否有該版本的發行分支。</span><span class="sxs-lookup"><span data-stu-id="8c905-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="8c905-111">任何適用於未來特定版本的變更都應以發行分支為目標。</span><span class="sxs-lookup"><span data-stu-id="8c905-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="8c905-112">發行分支具有下列名稱模式：`release-<version>`。</span><span class="sxs-lookup"><span data-stu-id="8c905-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="8c905-113">使提取要求佇列更利於每個人處理</span><span class="sxs-lookup"><span data-stu-id="8c905-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="8c905-114">提取要求佇列中有兩項基本的事實：</span><span class="sxs-lookup"><span data-stu-id="8c905-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="8c905-115">小範圍和包含相關變更的提取要求所需檢閱時間較少。</span><span class="sxs-lookup"><span data-stu-id="8c905-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="8c905-116">大範圍或包含不相關變更的提取要求所需檢閱時間較多。</span><span class="sxs-lookup"><span data-stu-id="8c905-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="8c905-117">避免會更新大量檔案的分支</span><span class="sxs-lookup"><span data-stu-id="8c905-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="8c905-118">分隔現有文章的次要更新與新文章或重大重寫。</span><span class="sxs-lookup"><span data-stu-id="8c905-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="8c905-119">在個別的工作分支中處理這些變更。</span><span class="sxs-lookup"><span data-stu-id="8c905-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="8c905-120">大量變更會造成具有大量變更檔案的 PR。</span><span class="sxs-lookup"><span data-stu-id="8c905-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="8c905-121">請將您的 PR 限制在最多 50 個變更檔案。</span><span class="sxs-lookup"><span data-stu-id="8c905-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="8c905-122">大型的 PR 不僅難以檢閱，也可能較會包含錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c905-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="8c905-123">重新命名或刪除檔案</span><span class="sxs-lookup"><span data-stu-id="8c905-123">Renaming or deleting files</span></span>

<span data-ttu-id="8c905-124">當您重新命名或刪除檔案時，請避免將這些變更與新增或更新的內容混合。</span><span class="sxs-lookup"><span data-stu-id="8c905-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="8c905-125">請在個別的 PR 中處理這些變更，使其合併順序晚於針對相關更新的 PR。</span><span class="sxs-lookup"><span data-stu-id="8c905-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="8c905-126">例如，請先更新重新導向檔案，並確認重新導向能正常運作，然後再刪除某篇文章。</span><span class="sxs-lookup"><span data-stu-id="8c905-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="8c905-127">您必須更新所有連結到重新命名檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="8c905-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="8c905-128">這包含任何 TOC 檔案。</span><span class="sxs-lookup"><span data-stu-id="8c905-128">This includes any TOC files.</span></span> <span data-ttu-id="8c905-129">您也必須在存放庫根的主要重新導向檔案 (`.openpublishing.redirection.json`) 中新增重新導向項目。</span><span class="sxs-lookup"><span data-stu-id="8c905-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="8c905-130">Docs PR 驗證服務</span><span class="sxs-lookup"><span data-stu-id="8c905-130">Docs PR validation service</span></span>

<span data-ttu-id="8c905-131">Docs PR 驗證服務是一項 GitHub 應用程式，可在 PR 中於檔案上執行驗證規則。</span><span class="sxs-lookup"><span data-stu-id="8c905-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="8c905-132">您會看見下列行為：</span><span class="sxs-lookup"><span data-stu-id="8c905-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="8c905-133">您提交 PR。</span><span class="sxs-lookup"><span data-stu-id="8c905-133">You submit a PR.</span></span>
1. <span data-ttu-id="8c905-134">在指出您 PR 狀態的 GitHub 註解中，您會看到存放庫上已啟用的「檢查」狀態。</span><span class="sxs-lookup"><span data-stu-id="8c905-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="8c905-135">請注意，在此範例中，有兩項已啟用的檢查：「認可驗證」和「OpenPublishing.Build」：</span><span class="sxs-lookup"><span data-stu-id="8c905-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![有些檢查失敗](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="8c905-137">即使認可驗證失敗，建置也可能會通過。</span><span class="sxs-lookup"><span data-stu-id="8c905-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="8c905-138">按一下 [詳細資料]  以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8c905-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="8c905-139">在 [詳細資料] 頁面上，您會看到所有失敗的驗證檢查，其中包含如何修正問題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c905-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="8c905-140">驗證成功時，會將下列註解新增至 PR：</span><span class="sxs-lookup"><span data-stu-id="8c905-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![組建驗證](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="8c905-142">若您是外部 (非 Microsoft) 參與者，您將無法存取詳細的組建報告或預覽連結。</span><span class="sxs-lookup"><span data-stu-id="8c905-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="8c905-143">組建警告</span><span class="sxs-lookup"><span data-stu-id="8c905-143">Build warnings</span></span>

<span data-ttu-id="8c905-144">一般而言，您應修正所有建置錯誤、警告和建議。</span><span class="sxs-lookup"><span data-stu-id="8c905-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="8c905-145">但是，您可以忽略部分警告。</span><span class="sxs-lookup"><span data-stu-id="8c905-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="8c905-146">您可以忽略下列警告：</span><span class="sxs-lookup"><span data-stu-id="8c905-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="8c905-147">找不到 `<version>/<modulepath>/About/About.md` 的服務名稱</span><span class="sxs-lookup"><span data-stu-id="8c905-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="8c905-148">包含下列名稱的中繼資料不允許在 YAML 標頭中設定，或是設為 docfx.json 中的檔案層級中繼資料，或是 docfx.json 中的全域中繼資料：`locale`。</span><span class="sxs-lookup"><span data-stu-id="8c905-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="8c905-149">它們會由 Docs 平台產生，因此在這 3 處設定的值會遭到忽略。</span><span class="sxs-lookup"><span data-stu-id="8c905-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="8c905-150">請從這 3 個位置移除它們以解決警告。</span><span class="sxs-lookup"><span data-stu-id="8c905-150">Please remove them from all 3 places to resolve the warning.</span></span>
