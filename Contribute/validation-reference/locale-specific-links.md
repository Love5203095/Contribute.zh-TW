---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: 地區設定限定連結
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841262"
---
# <a name="locale-specific-links"></a>地區設定限定連結

地區設定代碼 (例如 `en-us`) 不應包含在前往特定 Microsoft 網站的連結中。 若您在英文內容中的連結內包含地區設定代碼，它也會包含在當地語系化連結中，導致不良的當地語系化體驗。 例如，若德文當地語系化內容中的連結包含 `en-us`，則德國客戶會發現連結將他們導向英文文章 (即使有可用的德文版本)。

請從前往 Microsoft 網站的連結移除地區設定代碼。 下列為範例。

之前：

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

之後：

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

下列網站皆位於此驗證的範圍中：

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com