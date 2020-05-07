---
ms.openlocfilehash: 9cb0ba651d40d2834081d32443a8fd2b1152003d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "53286093"
---
## <a name="pull-request-processing"></a>提取要求會處理

上一節引導您完成提交建議變更的程序，方法是將它們繫結在新的提取要求 (PR) 中，此 PR 會新增到目的地存放庫的 PR 佇列。 提取要求會要求提取您工作分支的變更，合併到其他分支，以啟用 GitHub 的共同作業模型。 在大部分的案例中，其他分支是主要存放庫的預設/主分支。

### <a name="validation"></a>驗證

您的提取要求可能要先通過一或多項 PR 驗證程序，才能合併到其目的地分支。 驗證程序因建議變更範圍及目的地存放庫規則而異。 提交提取要求之後，您可以期待出現下列一或多種情況：

- **可合併性**：基準 GitHub 可合併性測試會先出現，確認您分支與目的地分支中的建議變更是否衝突。 如果提取要求指出此測試失敗，您即必須先協調造成合併衝突的內容，處理程序才能繼續。
- **CLA**：如果您要向公共存放庫發表貢獻，但不是 Microsoft 員工，視建議變更的範圍而定，第一次向該存放庫提交提取要求時，系統可能會要求您先完成簡短的貢獻授權合約 (CLA)。 完成 CLA 步驟之後，就會處理您的提取要求。
- **標記**：標籤會自動套用至您的提取要求，當提取要求通過驗證工作流程時指示其狀態。 例如，新的提取要求會自動接收 "do-not-merge" 標籤，指出提取要求尚未完成驗證、檢閱及登出步驟。
- **驗證和建置**：自動檢查會驗證變更是否通過驗證測試。 驗證測試可能會發出警告或錯誤，要求您先對提取要求中的一或多個檔案進行變更，再執行合併。 驗證測試結果會新增為提取要求中的註解供您檢閱，也可能以電子郵件傳送給您。
- **預備**:受變更影響的文章頁面會自動部署到預備環境，於驗證及建置成功時檢閱。 PR 註解會顯示預覽 URL。
- **自動合併**：如果提取要求通過驗證測試及特定條件，可能會自動合併。 如果是這種情況，您不需要採取任何進一步的動作。

### <a name="review-and-sign-off"></a>檢閱與登出

完成所有 PR 處理程序之後，您應該檢閱結果 (PR 註解、預覽 URL 等等) 以決定是否需要對其檔案進行額外變更，再登出進行合併。 如果 PR 檢閱者已檢閱過您的提取要求，如有未處理的問題/疑問需要在合併前解決，他們也可以透過註解提供意見反應。

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

當提取要求沒有問題且已登出後，您的變更即會合併回父分支並關閉提取要求。

### <a name="publishing"></a>發佈

請記住，提取要求必須先由 PR 檢閱者合併，下次排程的發佈回合才能納入變更。 通常是依提交順序檢閱/合併提取要求。 如果您的提取要求需要針對特定的發佈回合進行合併，您就需要提前與 PR 檢閱者合作，以確保先合併再發佈。

投稿經核准與合併後，就交由 docs.microsoft.com 發佈程序挑選。 發佈時間會因您投稿的存放庫管理小組而異。 經由下列路徑發佈的文章通常約在太平洋時間週一至週五上午 10:30 和下午 3:30 部署：

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

文章發佈上線最多約需 45 分鐘。 文章發佈後，您可在正確的 URL 驗證變更：`https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`。
