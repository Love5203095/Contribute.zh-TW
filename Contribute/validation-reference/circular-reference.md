---
title: circular-reference
description: Docs 組建問題 circular-reference 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459203"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>錯誤

`Files '{file name 1}' and '{file name 2}' reference each other.`

例如，這可能是連結到目前檔案的包含檔案，或已重新導向到目前檔案的檔案連結。

## <a name="resolution"></a>解決方式

檢閱檔案中的連結，並進行必要的編輯，以防任何檔案連結到或包含其本身。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
