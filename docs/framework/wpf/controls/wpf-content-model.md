---
title: WPF 內容模型
ms.date: 03/30/2017
helpviewer_keywords:
- UIElement class [WPF], displaying content
- content model [WPF], controls
- controls [WPF], displaying text
- content display [WPF], controls
- controls [WPF], formatting text
- displaying content [WPF]
- arbitrary content classes [WPF], content model
- ContentControl class [WPF], displaying content
ms.assetid: 214da5ef-547a-4cf8-9b07-4aa8a0e52cdd
ms.openlocfilehash: 4f866e0366a7781c287b3ebae7b668c2b296a5cc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59134585"
---
# <a name="wpf-content-model"></a>WPF 內容模型
[!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] 是展示平台，提供許多以顯示不同類型內容為主要目的的控制項和類控制項類型。 為了判斷要使用哪一種控制項或從哪一種控制項衍生，您應該了解特定控制項顯示哪些物件的效果最佳。  
  
 本主題摘要說明 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 控制項和類控制項類型所適用的內容模型。 內容模型描述控制項中可使用的內容。 本主題同時列出每一個內容模型的內容屬性。 內容屬性是一種用於儲存物件內容的屬性。  

<a name="classes_that_contain_arbitrary_content"></a>   
## <a name="classes-that-contain-arbitrary-content"></a>包含任意內容的類別  
 有些控制項可能包含任何類型，例如字串、 物件<xref:System.DateTime>物件，或<xref:System.Windows.UIElement>也就是其他項目的容器。 例如，<xref:System.Windows.Controls.Button>可以包含影像和某些文字; 或<xref:System.Windows.Controls.CheckBox>可包含的值<xref:System.DateTime.Now%2A?displayProperty=nameWithType>。  
  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 有四種可包含任意內容的類別。 下表列出的類別，繼承自<xref:System.Windows.Controls.Control>。  
  
|包含任意內容的類別|內容|  
|-------------------------------------------|-------------|  
|<xref:System.Windows.Controls.ContentControl>|單一任意物件。|  
|<xref:System.Windows.Controls.HeaderedContentControl>|標頭和單一項目，兩者都是任意物件。|  
|<xref:System.Windows.Controls.ItemsControl>|任意物件的集合。|  
|<xref:System.Windows.Controls.HeaderedItemsControl>|標頭和項目集合，這些全部都是任意物件。|  
  
 繼承自這些類別的控制項可以包含相同類型的內容，並且以相同方式處理內容。 下圖顯示一個控制項，從每個內容的模型，包含影像和某些文字：  
  
 ![如果螢幕擷取畫面顯示四個不同的控制項，從每個內容的模型。](./media/wpf-content-model/control-content-model-image-text.png)  
  
### <a name="controls-that-contain-a-single-arbitrary-object"></a>包含單一任意物件的控制項  
 <xref:System.Windows.Controls.ContentControl>類別包含單一任意內容。 其內容的屬性是<xref:System.Windows.Controls.ContentControl.Content%2A>。 下列控制項繼承自<xref:System.Windows.Controls.ContentControl>並且使用其內容模型：  
  
-   <xref:System.Windows.Controls.Button>  
  
-   <xref:System.Windows.Controls.Primitives.ButtonBase>  
  
-   <xref:System.Windows.Controls.CheckBox>  
  
-   <xref:System.Windows.Controls.ComboBoxItem>  
  
-   <xref:System.Windows.Controls.ContentControl>  
  
-   <xref:System.Windows.Controls.Frame>  
  
-   <xref:System.Windows.Controls.GridViewColumnHeader>  
  
-   <xref:System.Windows.Controls.GroupItem>  
  
-   <xref:System.Windows.Controls.Label>  
  
-   <xref:System.Windows.Controls.ListBoxItem>  
  
-   <xref:System.Windows.Controls.ListViewItem>  
  
-   <xref:System.Windows.Navigation.NavigationWindow>  
  
-   <xref:System.Windows.Controls.RadioButton>  
  
-   <xref:System.Windows.Controls.Primitives.RepeatButton>  
  
-   <xref:System.Windows.Controls.ScrollViewer>  
  
-   <xref:System.Windows.Controls.Primitives.StatusBarItem>  
  
-   <xref:System.Windows.Controls.Primitives.ToggleButton>  
  
-   <xref:System.Windows.Controls.ToolTip>  
  
-   <xref:System.Windows.Controls.UserControl>  
  
-   <xref:System.Windows.Window>  
  
 下圖顯示四個按鈕，其<xref:System.Windows.Controls.ContentControl.Content%2A>設定為字串，<xref:System.DateTime>物件， <xref:System.Windows.Shapes.Rectangle>，和<xref:System.Windows.Controls.Panel>，其中包含<xref:System.Windows.Shapes.Ellipse>和<xref:System.Windows.Controls.TextBlock>:  
  
 ![如果螢幕擷取畫面顯示使用不同的內容類型的四個按鈕。](./media/wpf-content-model/control-content-model-buttons.png)  
  
 如需如何設定的範例<xref:System.Windows.Controls.ContentControl.Content%2A>屬性，請參閱<xref:System.Windows.Controls.ContentControl>。  
  
### <a name="controls-that-contain-a-header-and-a-single-arbitrary-object"></a>包含標頭和單一任意物件的控制項  
 <xref:System.Windows.Controls.HeaderedContentControl>類別繼承自<xref:System.Windows.Controls.ContentControl>並顯示具有標頭的內容。 它所繼承之內容的屬性<xref:System.Windows.Controls.ContentControl.Content%2A>，從<xref:System.Windows.Controls.ContentControl>，並定義<xref:System.Windows.Controls.HeaderedContentControl.Header%2A>類型的屬性<xref:System.Object>; 因此，兩者都可以是任意物件。  
  
 下列控制項繼承自<xref:System.Windows.Controls.HeaderedContentControl>並且使用其內容模型：  
  
-   <xref:System.Windows.Controls.Expander>  
  
-   <xref:System.Windows.Controls.GroupBox>  
  
-   <xref:System.Windows.Controls.TabItem>  
  
 下圖顯示兩個<xref:System.Windows.Controls.TabItem>物件。 第一個<xref:System.Windows.Controls.TabItem>已經<xref:System.Windows.UIElement>物件當做<xref:System.Windows.Controls.HeaderedContentControl.Header%2A>而<xref:System.Windows.Controls.ContentControl.Content%2A>。 <xref:System.Windows.Controls.HeaderedContentControl.Header%2A>設定為<xref:System.Windows.Controls.StackPanel>，其中包含<xref:System.Windows.Shapes.Ellipse>和<xref:System.Windows.Controls.TextBlock>。 <xref:System.Windows.Controls.ContentControl.Content%2A>設定為<xref:System.Windows.Controls.StackPanel>，其中包含<xref:System.Windows.Controls.TextBlock>和<xref:System.Windows.Controls.Label>。 第二個<xref:System.Windows.Controls.TabItem>中包含字串<xref:System.Windows.Controls.HeaderedContentControl.Header%2A>並<xref:System.Windows.Controls.TextBlock>在<xref:System.Windows.Controls.ContentControl.Content%2A>。  
  
 ![標頭屬性中使用不同類型的 TabControl。](./media/wpf-content-model/control-content-model-tab.png)  
  
 如需如何建立的範例<xref:System.Windows.Controls.TabItem>物件，請參閱<xref:System.Windows.Controls.HeaderedContentControl>。  
  
### <a name="controls-that-contain-a-collection-of-arbitrary-objects"></a>包含任意物件集合的控制項  
 <xref:System.Windows.Controls.ItemsControl>類別繼承自<xref:System.Windows.Controls.Control>，而且可以包含多個項目，例如字串、 物件或其他項目。 其內容屬性為<xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>和<xref:System.Windows.Controls.ItemsControl.Items%2A>。 <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> 通常用來填入<xref:System.Windows.Controls.ItemsControl>資料收集。 如果您不想使用集合來填入<xref:System.Windows.Controls.ItemsControl>，您可以新增項目使用<xref:System.Windows.Controls.ItemsControl.Items%2A>屬性。  
  
 下列控制項繼承自<xref:System.Windows.Controls.ItemsControl>並且使用其內容模型：  
  
-   <xref:System.Windows.Controls.Menu>  
  
-   <xref:System.Windows.Controls.Primitives.MenuBase>  
  
-   <xref:System.Windows.Controls.ContextMenu>  
  
-   <xref:System.Windows.Controls.ComboBox>  
  
-   <xref:System.Windows.Controls.ItemsControl>  
  
-   <xref:System.Windows.Controls.ListBox>  
  
-   <xref:System.Windows.Controls.ListView>  
  
-   <xref:System.Windows.Controls.TabControl>  
  
-   <xref:System.Windows.Controls.TreeView>  
  
-   <xref:System.Windows.Controls.Primitives.Selector>  
  
-   <xref:System.Windows.Controls.Primitives.StatusBar>  
  
 下圖顯示<xref:System.Windows.Controls.ListBox>包含這些類型的項目：  
  
-   字串。  
  
-   <xref:System.DateTime> 物件。  
  
-   <xref:System.Windows.UIElement>。  
  
-   A <xref:System.Windows.Controls.Panel> ，其中包含<xref:System.Windows.Shapes.Ellipse>和<xref:System.Windows.Controls.TextBlock>。  
  
 ![如果螢幕擷取畫面顯示具有四種內容的 ListBox。](./media/wpf-content-model/control-content-model-listbox.png)  
  
### <a name="controls-that-contain-a-header-and-a-collection-of-arbitrary-objects"></a>包含標頭和任意物件集合的控制項  
 <xref:System.Windows.Controls.HeaderedItemsControl>類別繼承自<xref:System.Windows.Controls.ItemsControl>，而且可以包含多個項目，例如字串、 物件或其他項目和標頭。 它會繼承<xref:System.Windows.Controls.ItemsControl>內容屬性， <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>，並<xref:System.Windows.Controls.ItemsControl.Items%2A>，也會定義<xref:System.Windows.Controls.HeaderedItemsControl.Header%2A>可以是任意物件的屬性。  
  
 下列控制項繼承自<xref:System.Windows.Controls.HeaderedItemsControl>並且使用其內容模型：  
  
-   <xref:System.Windows.Controls.MenuItem>  
  
-   <xref:System.Windows.Controls.ToolBar>  
  
-   <xref:System.Windows.Controls.TreeViewItem>  
  
<a name="classes_that_contain_a_collection_of_uielement_objects"></a>   
## <a name="classes-that-contain-a-collection-of-uielement-objects"></a>包含 UIElement 物件集合的類別  
 <xref:System.Windows.Controls.Panel>類別會定位和排列子<xref:System.Windows.UIElement>物件。 其內容的屬性是<xref:System.Windows.Controls.Panel.Children%2A>。  
  
 下列類別繼承自<xref:System.Windows.Controls.Panel>類別，並且使用其內容模型：  
  
-   <xref:System.Windows.Controls.Canvas>  
  
-   <xref:System.Windows.Controls.DockPanel>  
  
-   <xref:System.Windows.Controls.Grid>  
  
-   <xref:System.Windows.Controls.Primitives.TabPanel>  
  
-   <xref:System.Windows.Controls.Primitives.ToolBarOverflowPanel>  
  
-   <xref:System.Windows.Controls.Primitives.ToolBarPanel>  
  
-   <xref:System.Windows.Controls.Primitives.UniformGrid>  
  
-   <xref:System.Windows.Controls.StackPanel>  
  
-   <xref:System.Windows.Controls.VirtualizingPanel>  
  
-   <xref:System.Windows.Controls.VirtualizingStackPanel>  
  
-   <xref:System.Windows.Controls.WrapPanel>  
  
 如需詳細資訊，請參閱[面板概觀](panels-overview.md)。  
  
<a name="classes_that_affects_the_appearance_of_a_uielement"></a>   
## <a name="classes-that-affect-the-appearance-of-a-uielement"></a>影響 UIElement 外觀的類別  
 <xref:System.Windows.Controls.Decorator>類別適用於視覺效果，或其周圍單一子系<xref:System.Windows.UIElement>。 其內容的屬性是<xref:System.Windows.Controls.Decorator.Child%2A>。 下列類別繼承自<xref:System.Windows.Controls.Decorator>並且使用其內容模型：  
  
-   <xref:System.Windows.Documents.AdornerDecorator>  
  
-   <xref:System.Windows.Controls.Border>  
  
-   <xref:System.Windows.Controls.Primitives.BulletDecorator>  
  
-   <xref:Microsoft.Windows.Themes.ButtonChrome>  
  
-   <xref:Microsoft.Windows.Themes.ClassicBorderDecorator>  
  
-   <xref:System.Windows.Controls.InkPresenter>  
  
-   <xref:Microsoft.Windows.Themes.ListBoxChrome>  
  
-   <xref:Microsoft.Windows.Themes.SystemDropShadowChrome>  
  
-   <xref:System.Windows.Controls.Viewbox>  
  
 如下圖所示<xref:System.Windows.Controls.TextBox>具有 （做為裝飾）<xref:System.Windows.Controls.Border>其周圍。  
  
 ![具有黑色框線的 TextBox](./media/layout-border-around-textbox.png "Layout_Border_around_TextBox")  
具有框線的 TextBlock  
  
<a name="classes_that_provides_visual_feedback_about_a_uielement"></a>   
## <a name="classes-that-provide-visual-feedback-about-a-uielement"></a>提供 UIElement 相關視覺化回應的類別  
 <xref:System.Windows.Documents.Adorner>類別會提供視覺提示給使用者。 例如，使用<xref:System.Windows.Documents.Adorner>將功能控點加入項目，或提供控制項的狀態資訊。 <xref:System.Windows.Documents.Adorner>類別所提供的架構，讓您可以建立自己的裝飾項。 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 不會提供任何已實作的裝飾項。 如需詳細資訊，請參閱[裝飾項概觀](adorners-overview.md)。  
  
<a name="classes_that_enable_users_to_enter_text"></a>   
## <a name="classes-that-enable-users-to-enter-text"></a>可讓使用者輸入文字的類別  
 WPF 提供三種可讓使用者輸入文字的主要控制項。 每一個控制項都會以不同方式顯示文字。 下表列出這三個文字相關控制項、它們顯示文字時的功能，以及其包含控制項文字的屬性。  
  
|控制項|文字顯示為|內容屬性|  
|-------------|--------------------------|----------------------|  
|<xref:System.Windows.Controls.TextBox>|純文字|<xref:System.Windows.Controls.TextBox.Text%2A>|  
|<xref:System.Windows.Controls.RichTextBox>|格式化文字|<xref:System.Windows.Controls.RichTextBox.Document%2A>|  
|<xref:System.Windows.Controls.PasswordBox>|隱藏文字 (字元會加上遮罩)|<xref:System.Windows.Controls.PasswordBox.Password%2A>|  
  
<a name="classes_that_display_text"></a>   
## <a name="classes-that-display-your-text"></a>顯示文字的類別  
 有數種類別可用來顯示純文字或格式化文字。 您可以使用<xref:System.Windows.Controls.TextBlock>顯示少量文字。 如果您想要顯示大量文字時，使用<xref:System.Windows.Controls.FlowDocumentReader>， <xref:System.Windows.Controls.FlowDocumentPageViewer>，或<xref:System.Windows.Controls.FlowDocumentScrollViewer>控制項。  
  
 <xref:System.Windows.Controls.TextBlock>有兩個內容屬性：<xref:System.Windows.Controls.TextBlock.Text%2A>和<xref:System.Windows.Controls.TextBlock.Inlines%2A>。 當您想要顯示使用一致格式設定的文字<xref:System.Windows.Controls.TextBlock.Text%2A>屬性通常是您最佳的選擇。 如果您打算使用不同的格式，在整個文字，使用<xref:System.Windows.Controls.TextBlock.Inlines%2A>屬性。 <xref:System.Windows.Controls.TextBlock.Inlines%2A>屬性是集合<xref:System.Windows.Documents.Inline>物件，指定如何格式化文字。  
  
 下表列出的內容屬性<xref:System.Windows.Controls.FlowDocumentReader>， <xref:System.Windows.Controls.FlowDocumentPageViewer>，和<xref:System.Windows.Controls.FlowDocumentScrollViewer>類別。  
  
|控制項|內容屬性|內容屬性類型|  
|-------------|----------------------|---------------------------|  
|<xref:System.Windows.Controls.FlowDocumentPageViewer>|文件|<xref:System.Windows.Documents.IDocumentPaginatorSource>|  
|<xref:System.Windows.Controls.FlowDocumentReader>|文件|<xref:System.Windows.Documents.FlowDocument>|  
|<xref:System.Windows.Controls.FlowDocumentScrollViewer>|文件|<xref:System.Windows.Documents.FlowDocument>|  
  
 <xref:System.Windows.Documents.FlowDocument>會實作<xref:System.Windows.Documents.IDocumentPaginatorSource>介面; 因此，所有的三個類別都可以採用<xref:System.Windows.Documents.FlowDocument>做為內容。  
  
<a name="classes_that_format_text"></a>   
## <a name="classes-that-format-your-text"></a>格式化文字的類別  
 <xref:System.Windows.Documents.TextElement> 和其相關的類別可讓您格式化文字。 <xref:System.Windows.Documents.TextElement> 物件包含和中的文字格式化<xref:System.Windows.Controls.TextBlock>和<xref:System.Windows.Documents.FlowDocument>物件。 兩種主要類型<xref:System.Windows.Documents.TextElement>物件<xref:System.Windows.Documents.Block>項目和<xref:System.Windows.Documents.Inline>項目。 A<xref:System.Windows.Documents.Block>項目代表一個區塊的文字，例如段落或清單。 <xref:System.Windows.Documents.Inline>項目代表一部分的區塊中的文字。 許多<xref:System.Windows.Documents.Inline>類別可讓您指定套用至文字的格式。 每個<xref:System.Windows.Documents.TextElement>都有自己的內容模型。 如需詳細資訊，請參閱 [TextElement 內容模型概觀](../advanced/textelement-content-model-overview.md)。  
  
## <a name="see-also"></a>另請參閱

- [進階](../advanced/index.md)
