---
ms.openlocfilehash: de73145273ad5aa5c19de55525417cfc3305b86d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803477"
---
### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>在已選取項目的 WPF ListBox、ListView 或 DataGrid 上呼叫 Items.Refresh 會導致在項目中出現重複的項目

|   |   |
|---|---|
|詳細資料|在 .NET Framework 4.5 中，如果 <xref:System.Windows.Controls.ListBox?displayProperty=name> 中已選取項目，從程式碼呼叫 ListBox.Items.Refresh 可能會導致選取的項目在清單中重複出現。 <xref:System.Windows.Controls.ListView?displayProperty=name> 和 <xref:System.Windows.Controls.DataGrid?displayProperty=name> 會發生類似的問題。 這在 .NET Framework 4.6 中已修正。|
|建議|您可以在呼叫 <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> 之前以程式設計方式取消選取項目，然後在呼叫完成之後重新選取項目來解決此問題。 此外，此問題在 .NET Framework 4.6 中已修正，因此可藉由升級至該版 .NET Framework 來解決。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|
