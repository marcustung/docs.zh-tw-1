---
title: PasswordBox 樣式和範本
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], PasswordBox
- templates [WPF], PasswordBox
- ControlTemplate [WPF], PasswordBox
- states [WPF], PasswordBox
- PasswordBox [WPF], styles and templates
- parts [WPF], PasswordBox
ms.assetid: deb52107-959f-4a60-b303-d21a0a933060
ms.openlocfilehash: 7783330dd56ec5b2759e783a6935761eb3587978
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57509527"
---
# <a name="passwordbox-styles-and-templates"></a>PasswordBox 樣式和範本

本主題描述的樣式和範本<xref:System.Windows.Controls.PasswordBox>控制項。 您可以修改預設<xref:System.Windows.Controls.ControlTemplate>，讓控制項的獨特的外觀。 如需詳細資訊，請參閱[透過建立 ControlTemplate 自訂現有控制項的外觀](customizing-the-appearance-of-an-existing-control.md)。

## <a name="passwordbox-parts"></a>PasswordBox 組件

下表列出的具名組件<xref:System.Windows.Controls.PasswordBox>控制項。

|組件|類型|描述|
|-|-|-|
|PART_ContentHost|<xref:System.Windows.FrameworkElement>|可包含的視覺元素<xref:System.Windows.FrameworkElement>。 文字<xref:System.Windows.Controls.PasswordBox>會顯示此項目中。|

## <a name="passwordbox-states"></a>PasswordBox 狀態

下表列出的視覺狀態<xref:System.Windows.Controls.PasswordBox>控制項。

|VisualState 名稱|VisualStateGroup 名稱|描述|
|-|-|-|
|一般|CommonStates|預設狀態。|
|MouseOver|CommonStates|滑鼠指標移到控制項上。|
|已停用|CommonStates|已停用控制項。|
|已取得焦點|FocusStates|控制項已取得焦點。|
|未取得焦點|FocusStates|控制項未取得焦點。|
|驗證|ValidationStates|控制項使用<xref:System.Windows.Controls.Validation>類別和<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`false`。|
|InvalidFocused|ValidationStates|<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`true`已在控制項具有焦點。|
|InvalidUnfocused|ValidationStates|<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`true`有控制項沒有焦點。|

## <a name="passwordbox-controltemplate-example"></a>PasswordBox ControlTemplate 範例

下列範例示範如何定義<xref:System.Windows.Controls.ControlTemplate>針對<xref:System.Windows.Controls.PasswordBox>控制項。

[!code-xaml[ControlTemplateExamples#PasswordBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#passwordbox)]

上述範例使用下列一或多項資源。

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

如需完整的範例，請參閱[使用 ControlTemplate 設定樣式範例](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)。

## <a name="see-also"></a>另請參閱

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [控制項的樣式和範本](control-styles-and-templates.md)
- [控制項自訂](control-customization.md)
- [樣式設定和範本化](styling-and-templating.md)
- [透過建立 ControlTemplate 自訂現有控制項的外觀](customizing-the-appearance-of-an-existing-control.md)
