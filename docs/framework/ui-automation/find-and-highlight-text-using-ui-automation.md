---
title: 利用 UI 自動化尋找和反白顯示文字
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text, highlighting
- finding text
- text, finding
- UI automation, highlighting text
- UI automation, finding text
- highlighting text
ms.assetid: b77693f5-87bb-4b29-a297-05ff882e2044
ms.openlocfilehash: fafd3fc7345f94d3907163ff9dcf0ab293f85f3f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59157153"
---
# <a name="find-and-highlight-text-using-ui-automation"></a>利用 UI 自動化尋找和反白顯示文字
> [!NOTE]
>  這份文件適用於想要使用 <xref:System.Windows.Automation> 命名空間中定義之 Managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 類別的 .NET Framework 開發人員。 如需最新資訊[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]，請參閱[Windows Automation API:使用者介面自動化](https://go.microsoft.com/fwlink/?LinkID=156746)。  
  
 本主題示範如何依序搜尋，並反白顯示文字的控制項使用的內容中之字串的每個出現[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]。  
  
## <a name="example"></a>範例  
 下列範例會取得<xref:System.Windows.Automation.TextPattern>從文字控制項的物件。 A<xref:System.Windows.Automation.Text.TextPatternRange>物件，表示文字內容的整份文件，然後會建立使用<xref:System.Windows.Automation.TextPattern.DocumentRange%2A>屬性的<xref:System.Windows.Automation.TextPattern>。 兩個額外<xref:System.Windows.Automation.Text.TextPatternRange>物件建立，然後進行循序搜尋，並反白顯示功能。  
  
[!code-csharp[FindText#StartApp](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#startapp)]
[!code-vb[FindText#StartApp](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#startapp)]  
[!code-csharp[FindText#FindTextProvider](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#findtextprovider)]
[!code-vb[FindText#FindTextProvider](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#findtextprovider)]  
[!code-csharp[FindText#SearchTarget](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#searchtarget)]
[!code-vb[FindText#SearchTarget](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#searchtarget)]  
  
## <a name="see-also"></a>另請參閱

- [使用 UI 自動化尋找和反白顯示文字](../../../docs/framework/ui-automation/find-and-highlight-text-using-ui-automation.md)
