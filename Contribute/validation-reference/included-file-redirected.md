---
title: included-file-redirected
description: Docs 組建問題 included-file-redirected 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459065"
---
# <a name="included-file-redirected"></a>included-file-redirected

## <a name="warning"></a>警告

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a>解決方式

重新建構您的內容，讓您不包括重新導向的檔案。 例如，建立新的檔案以包含或移除包含的內容參考和連結，或是將它內嵌寫入。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
