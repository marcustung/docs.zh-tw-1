---
title: 儲存筆墨
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ISF (Ink Serialized Format)
- storing ink [WPF]
- ink [WPF], storing
- retrieving ink [WPF]
- Ink Serialized Format (ISF)
ms.assetid: a3f6d16b-d682-4680-9965-907332b4d2b8
ms.openlocfilehash: 4089aa7942105c14eb628c75edb7f53ffacfaeb0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182334"
---
# <a name="storing-ink"></a>儲存筆墨
<xref:System.Windows.Ink.StrokeCollection.Save%2A>方法儲存筆墨為 Ink Serialized Format (ISF) 提供支援。 建構函式<xref:System.Windows.Ink.StrokeCollection>類別提供讀取筆墨資料的支援。  
  
## <a name="ink-storage-and-retrieval"></a>筆墨儲存和擷取  
 本節討論如何儲存和擷取筆墨[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]平台。  
  
 下列範例會顯示 [儲存檔案] 對話方塊中，並將儲存筆墨的按鈕 click 事件處理常式<xref:System.Windows.Controls.InkCanvas>外的檔案。  
  
 [!code-csharp[DigitalInkTopics#12](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#12)]
 [!code-vb[DigitalInkTopics#12](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#12)]  
  
 下列範例會顯示 [開啟舊檔] 對話方塊，並從檔案讀取筆墨的按鈕 click 事件處理常式<xref:System.Windows.Controls.InkCanvas>項目。  
  
 [!code-csharp[DigitalInkTopics#13](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#13)]
 [!code-vb[DigitalInkTopics#13](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#13)]  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Windows.Controls.InkCanvas>
- [Windows Presentation Foundation](../index.md)
