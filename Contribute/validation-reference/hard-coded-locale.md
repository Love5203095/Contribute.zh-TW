---
title: hard-coded-locale
description: Docs 組建問題 hard-coded-locale 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310339"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>警告

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

地區設定代碼 (例如 `en-us`) 不應包含在前往特定 Microsoft 網站的連結中。 若您在英文內容中的連結內包含地區設定代碼，它也會包含在當地語系化連結中，導致不良的當地語系化體驗。 例如，若德文當地語系化內容中的連結包含 `en-us`，則德國客戶會發現連結將他們導向英文文章 (即使有可用的德文版本)。

下列網站皆位於此驗證的範圍中：

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>解決方式

請從前往 Microsoft 網站的連結移除地區設定代碼。 下列為範例。

之前：

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

之後：

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> VS Code 的 Docs Markdown 延伸模組包含適用於 Microsoft 連結的清除指令碼。 指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。 執行指令碼：
>
> 1. 安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。
> 1. 按一下 alt + M 來開啟 Markdown 功能表。
> 1. 選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]