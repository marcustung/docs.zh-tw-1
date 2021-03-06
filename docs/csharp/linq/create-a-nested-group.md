---
title: 建立巢狀群組 (C# 中的 LINQ)
description: 了解如何在 C# 之 LINQ 查詢運算式中建立巢狀群組。
ms.date: 12/01/2016
ms.assetid: e9f00708-362e-4d13-98c5-d77549347ba0
ms.openlocfilehash: 7d056c9e215ccc7ca24d621b64e2328bed79f22e
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857667"
---
# <a name="create-a-nested-group"></a>建立巢狀群組

下列範例示範如何在 LINQ 查詢運算式中建立巢狀群組。 每個根據學年或年級層級建立的群組，接著會根據每個人的姓名進一步細分為群組。

## <a name="example"></a>範例

> [!NOTE]
> 這個範例包含[查詢物件的集合](query-a-collection-of-objects.md)中範例程式碼中定義的物件參考。

[!code-csharp[csProgGuideLINQ#24](~/samples/snippets/csharp/concepts/linq/how-to-create-a-nested-group_1.cs)]

請注意，需要有三個巢狀 `foreach` 迴圈，才能逐一查看巢狀群組的內部項目。

## <a name="see-also"></a>另請參閱

- [Language-Integrated Query (LINQ)](index.md)
