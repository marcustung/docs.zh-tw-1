---
title: ByVal (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ByVal
- ByVal
helpviewer_keywords:
- ByVal keyword [Visual Basic], contexts
- ByVal keyword [Visual Basic]
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
ms.openlocfilehash: 5e534eac2300327d4c54c5ce93d8b2c6c538e794
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "58832488"
---
# <a name="byval-visual-basic"></a>ByVal (Visual Basic)
指定呼叫的程序或屬性無法變更基礎呼叫程式碼中的引數的變數值的方式傳遞引數。  
  
## <a name="remarks"></a>備註  
 `ByVal` 修飾詞可用於以下內容：  
  
 [Declare 陳述式](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function 陳述式](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Operator 陳述式](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [Property 陳述式](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub 陳述式](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="example"></a>範例  
 下列範例示範如何使用`ByVal`參數傳遞參考型別引數的機制。 在此範例中，引數是`c1`，類別的執行個體`Class1`。 `ByVal` 防止程序中的程式碼變更基礎值的參考引數`c1`，但不會保護的可存取的欄位和屬性`c1`。  
  
 [!code-vb[VbVbalrKeywords#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class5.vb#10)]  
  
## <a name="see-also"></a>另請參閱

- [關鍵字](../../../visual-basic/language-reference/keywords/index.md)
- [以傳值和傳址方式傳遞引數](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
