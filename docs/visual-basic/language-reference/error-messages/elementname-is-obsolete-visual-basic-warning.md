---
title: "'<elementname>' 已經過時 (Visual Basic 警告)"
ms.date: 07/20/2015
f1_keywords:
- vbc40008
- bc40008
helpviewer_keywords:
- BC40008
ms.assetid: 729e3eb5-76ac-4c55-9fdd-78350e0de55e
ms.openlocfilehash: 545f0f4a56e72e32d2225217225d441a10f0e52e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "58836359"
---
# <a name="elementname-is-obsolete-visual-basic-warning"></a>'\<項目名稱 >' 已經過時 （Visual Basic 警告）
陳述式嘗試存取已使用 <xref:System.ObsoleteAttribute> 屬性和指示詞標記以視為警告的程式設計項目。  
  
 您可以將任何程式設計項目標記為不再使用，方法是對其套用 <xref:System.ObsoleteAttribute> 。 如果您這麼做，則可以將屬性 (attribute) 的 <xref:System.ObsoleteAttribute.IsError%2A> 屬性 (property) 設定為 `True` 或 `False`。 如果您將它設定為 `True`，則編譯器會將使用這個項目的嘗試視為錯誤。 如果您將它設定為 `False`，或讓它預設為 `False`，則在嘗試使用該項目時，編譯器會發出警告。  
  
 根據預設，這個訊息是一個警告，因為 <xref:System.ObsoleteAttribute.IsError%2A> 的 <xref:System.ObsoleteAttribute> 屬性是 `False`。 如需隱藏警告或將警告視為錯誤的詳細資訊，請參閱 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。  
  
 **錯誤 ID:** BC40008  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
-   確定原始程式碼參考正確拼寫項目名稱。  
  
## <a name="see-also"></a>另請參閱

- [屬性概觀](../../../visual-basic/programming-guide/concepts/attributes/index.md)
