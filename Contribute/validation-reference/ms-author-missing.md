---
title: ms-author-missing
description: ms-author-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246244"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>警告

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>解決方式

在 `ms.author` 新增目前作者的 Microsoft 別名。 請注意，如果擁有權曾經變更，這應該要是文章的「目前」  擁有者，而不是原始作者。 建議使用全職員工或小組通訊群組清單 (DL) 而非短期廠商作為指定的作者。 

如果別名為 DL，它必須也在 `ms.author` 允許清單上。

如需 `ms.author` DL 的有效值，請參閱[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
