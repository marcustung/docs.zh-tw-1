---
title: HOW TO：清除繫結
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
ms.openlocfilehash: 8140928d44555e399ddf4ebd73407a251ad3cffe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59101415"
---
# <a name="how-to-clear-bindings"></a>HOW TO：清除繫結
這個範例顯示如何清除物件的繫結。  
  
## <a name="example"></a>範例  
 若要清除物件個別屬性的繫結，請呼叫<xref:System.Windows.Data.BindingOperations.ClearBinding%2A>如下列範例所示。 下列範例會移除從繫結<xref:System.Windows.Controls.TextBlock.TextProperty>的*mytext*、<xref:System.Windows.Controls.TextBlock>物件。  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 清除繫結會移除繫結，讓相依性屬性的值還原為沒有繫結時應該有的值。 這個值可以是預設值、繼承值或是資料範本繫結的值。  
  
 若要清除的物件上的所有可能屬性的繫結，請使用<xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Windows.Data.BindingOperations>
- [資料繫結概觀](data-binding-overview.md)
- [HOW-TO 主題](data-binding-how-to-topics.md)
