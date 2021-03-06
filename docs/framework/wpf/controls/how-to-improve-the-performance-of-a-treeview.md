---
title: HOW TO：改善 TreeView 的效能
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], improving the performance
ms.assetid: b792c740-cf2b-4da8-8ba8-3d2e5a821874
ms.openlocfilehash: de1b46da2a7c6c3db0c0c19cdbb654fcf2fbbd6c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153435"
---
# <a name="how-to-improve-the-performance-of-a-treeview"></a>HOW TO：改善 TreeView 的效能
如果<xref:System.Windows.Controls.TreeView>包含許多項目，載入所花費的時間長度可能在使用者介面項目會造成明顯的延遲。 您可以藉由設定改善載入時間`VirtualizingStackPanel.IsVirtualizing`附加屬性`true`。  UI 也可能會變慢，以回應使用者捲動時<xref:System.Windows.Controls.TreeView>藉由使用滑鼠滾輪，或拖曳捲軸捲動方塊。 您可以改善效能<xref:System.Windows.Controls.TreeView>當使用者捲動藉由設定`VirtualizingStackPanel.VirtualizationMode`; 附加屬性<xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>。  
  
## <a name="example"></a>範例  
  
## <a name="description"></a>描述  
下列範例會建立<xref:System.Windows.Controls.TreeView>，設定`VirtualizingStackPanel.IsVirtualizing`附加屬性設定為 true 並`VirtualizingStackPanel.VirtualizationMode`; 附加屬性<xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>最佳化其效能。  
  
## <a name="code"></a>程式碼  
 [!code-xaml[RecycleItemContainerShippets#VirtualizingTreeView](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizingtreeview)]  
  
 下列範例會顯示先前的範例使用的資料。  
  
 [!code-csharp[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#treeviewdata)]
 [!code-vb[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#treeviewdata)]  
  
## <a name="see-also"></a>另請參閱

- [控制項](../advanced/optimizing-performance-controls.md)
