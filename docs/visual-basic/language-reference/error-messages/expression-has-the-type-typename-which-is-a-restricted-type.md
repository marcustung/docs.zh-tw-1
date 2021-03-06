---
title: 運算式包含類型 '<typename>'，其為受限制的類型且不可用來存取繼承自 'Object' 或 'ValueType' 的成員
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: 017a2458562068727674bd3fd9cda8c33d989e8b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59314616"
---
# <a name="expression-has-the-type-typename-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-object-or-valuetype"></a>運算式包含類型 '\<類型名稱 >' 其為受限制的類型，且不能用來存取繼承自 'Object' 或 'ValueType' 的成員
運算式評估為 common language runtime (CLR) 無法 box 處理的類型，但是會存取需要 boxing 處理的成員。  
  
 *Boxing* 是指將類型轉換為 `Object` 或者，在某些情況下，轉換為 <xref:System.ValueType>時所需的處理。 Common language runtime 無法 box 處理某些結構類型，例如<xref:System.ArgIterator>， <xref:System.RuntimeArgumentHandle>，和<xref:System.TypedReference>。  
  
 這個運算式會嘗試使用受限制的型別呼叫方法，繼承自<xref:System.Object>或是<xref:System.ValueType>，例如<xref:System.Object.GetHashCode%2A>或<xref:System.Object.ToString%2A>。 若要存取此方法，Visual Basic 嘗試會導致此錯誤的隱含 boxing 轉換。  
  
 **錯誤 ID:** BC31393  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1. 找出評估至所指出類型的運算式。  
  
2. 找出您嘗試呼叫的方法繼承自的陳述式的一部分<xref:System.Object>或<xref:System.ValueType>。  
  
3. 請重寫陳述式，以避免在方法呼叫。  
  
## <a name="see-also"></a>另請參閱

- [隱含和明確轉換](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
