---
title: ms-author-invalid
description: Docs 組建問題 ms-author-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246296"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>警告

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>解決方式

將 `ms.author` 值更新為目前建立者的有效 Microsoft 別名。 建議使用全職員工或小組通訊群組清單 (DL) 而非短期廠商作為指定的作者。 如果別名為 DL，它必須也在 `ms.author` 允許清單上。

如需 `ms.author` DL 的有效值，請參閱[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
