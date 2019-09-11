---
title: block-section-invalid
description: Docs 組建問題 block-section-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 500527c7371dd9d4966460b3eafe0a44874fc4eb
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848524"
---
# <a name="block-section-invalid"></a>block-section-invalid

## <a name="warning"></a>警告

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

數個 Docs Markdown 延伸模組以字串 `> [!` 開頭。 `>` 與 `[` 之間必須有一個空格，而且必須有右 `]`。 如果語法不正確，文字會轉譯為區塊引述。

## <a name="resolution"></a>解決方式

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

確定您使用的延伸模組語法正確：

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
