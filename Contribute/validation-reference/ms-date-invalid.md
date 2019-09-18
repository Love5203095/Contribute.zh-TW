---
title: ms-date-invalid
description: ms-date-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 46cd047253fc7fbfdf92b0c5a6d690e041262b02
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895451"
---
# <a name="ms-date-invalid"></a>ms-date-invalid

## <a name="warning"></a>警告

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY, no more than five days from today.`

## <a name="resolution"></a>解決方式

確認文章為最新狀態，其中沒有任何損毀的內容，然後以 MM/DD/YYYY 格式新增有效日期：

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
