---
title: 溢位 (Visual Basic 執行階段錯誤)
ms.date: 07/20/2015
f1_keywords:
- vbrERRID_Overflow
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
ms.openlocfilehash: 63223a815e1c4ff8d4e0afbb6c732fff90aad465
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59345543"
---
# <a name="overflow-visual-basic-run-time-error"></a>溢位 (Visual Basic 執行階段錯誤)
當您嘗試超過限制的指派目標的指派時，就會造成溢位。  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1. 請確定指派、 計算和資料類型轉換不會太大而無法表示變數的值，該類型所允許的範圍內，並將值指派給類型的變數的結果可以保存較大範圍的值如有必要。  
  
2. 請確定指派屬性符合的屬性會將所做的範圍。  
  
3. 請確定會強制轉型成整數的計算中使用的數字，並沒有比整數較大的結果。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Int32.MaxValue?displayProperty=nameWithType>
- <xref:System.Double.MaxValue?displayProperty=nameWithType>
- [資料類型](../../../visual-basic/language-reference/data-types/index.md)
- [錯誤類型](../../../visual-basic/programming-guide/language-features/error-types.md)
