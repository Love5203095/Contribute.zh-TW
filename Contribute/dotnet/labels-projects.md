---
title: 標籤和專案藍圖
description: 本文說明 dotnet/docs 存放庫中標籤和專案的使用方式。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760368"
---
# <a name="labels-and-projects-roadmap"></a>標籤和專案藍圖

.NET 文件小組廣泛使用 [GitHub 標籤](https://github.com/dotnet/docs/labels)來管理工作。 藉由篩選標籤組合，即可快速專注於 [.NET 文件網站](https://docs.microsoft.com/dotnet)上感興趣的章節。

我們也使用 [GitHub 專案](https://github.com/dotnet/docs/projects) 來管理短期衝刺及其他目標導向的 Epic。

此藍圖說明如何使用這些管理工具，並包含便利的篩選連結，以便用來尋找感興趣的區域。

## <a name="labels"></a>標籤

如果這是第一次參與 [dotnet/docs](https://github.com/dotnet/docs)，建議您從 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 問題開始。 這些是範圍較集中的問題。 也是您第一次參與的絕佳方式。 從 up-for-grabs 檢視，您可根據區域和優先順序進一步篩選問題。 如果想要在第一次參與時嘗試較不嚴重的問題，我們在 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 中列出了適合初學者的不錯問題。

我們使用標籤，以許多不同的方式來分類問題：

- [.NET 指南](#find-a-single-net-guide)和[指南的章節](#search-one-section-of-a-guide)。
- [目標版本](#releases)
- [優先順序](#priority)

您可從每個集合 (指南、版本、優先順序) 合併成一個標籤來建立範圍較窄的焦點，以尋找想要解決的問題。

### <a name="find-a-single-net-guide"></a>尋找單一 .NET 指南

我們針對每個架構電子書和每個 .NET 指南使用標籤。

![淺綠色背景上的 :book: guide](./media/labels-projects/guide.png "架構指南標籤的前置詞")

架構電子書會以 `:book: guide` 前置詞來註明，並具有淺綠色背景。 這些是涵蓋建議架構的完整格式區域。 以下是針對每個 .NET 架構指南篩選的目前問題。

- [ASP.NET Core Web 應用程式](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [雲端原生](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker 生命週期](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [使用 Windows 容器進行現代化](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET 微服務](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [無伺服器應用程式](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

此標籤樣式也適用於 [Framework 設計方針](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。 此區域具有相同的標籤設計，但不建議社群公關部門使用。 這是需要許可才能轉載的內容，且不可編輯。

![深藍色背景上的 :books:區域](./media/labels-projects/area.png ".NET 指南區域標籤的前置詞")

每個 .NET 指南會以 `:books: Area` 前置詞來註明，並具有深藍色背景。 以下是針對每個 .NET 指南篩選的目前問題。

- [API 參照](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [桌面指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET 架構指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 可移除
- [.NET Core 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [適用於 Apache Spark 的 .NET 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API 參照](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 可移除。
- [Visual Basic 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>搜尋指南的某個章節

![中藍色背景上的 :card_file_box:區域](./media/labels-projects/technology.png ".NET 指南子區域標籤的前置詞")

.NET 指南很大，因此這些標籤會依指南章節進一步限制範圍。 每個 .NET 指南子區域會以 `:card_file_box: Technology` 前置詞來註明，並具有中藍色背景。 這些標籤中有許多適用於多個指南，而其他標籤則只適用於一個指南。 依區域篩選之後，請新增下列其中一個標籤，以進一步限制問題的範圍。

- AppCompat
- 非同步工作
- C# 進階概念
- C# 編譯器
- C# 基礎
- C# 入門
- C# 語言參考
- C# Null 安全
- C# 的新功能
- CLI
- 資料存取
- Docker
- 安裝程式
- LINQ
- NCL
- .NET Standard
- Roslyn API
- 安全性
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>版本

![深黃色上的 :checkered_flag:Release:](./media/labels-projects/release.png "版本標籤的前置詞")

針對特定版本標記的問題會以 `:checkered_flag: Release:` 前置詞來註明，並具有深黃色背景。

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>優先順序

所有優先順序標籤都是 `P` 後面接著一位數。 數字越低則表示優先順序越高：

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>其他標籤如何？

內容小組使用許多其他標籤來管理不同分類的問題。 如果您不在內容小組上，則可以忽略這些其他標籤。

## <a name="projects"></a>專案

我們透過兩種方式來使用專案：

- Month YYYY 專案類型：這些是每月工作計畫的 Scrum 面板。
- 長時間執行的 Epic：這些會在工作持續數個月時，用來管理工作達成目標的進度。
