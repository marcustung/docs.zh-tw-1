---
title: 向量圖形概觀
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inclusive-inclusive endpoints
- coordinate systems
- graphics [Windows Forms], vector graphics
ms.assetid: 0195df81-66be-452d-bb53-5a582ebfdc09
ms.openlocfilehash: d424254839db6c403bafe779f475c0e344918a5e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59087959"
---
# <a name="vector-graphics-overview"></a>向量圖形概觀
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 座標系統上繪製線條、 矩形和其他形狀。 您可以選擇各式各樣的座標系統，但預設座標系統具有原點左上角的 x 軸指向右側和 y 軸指向下方。 預設座標系統中的測量單位為像素。  
  
## <a name="the-building-blocks-of-gdi"></a>GDI + 的建置組塊  
 ![向量圖形](./media/aboutgdip02-art01.gif "AboutGdip02_Art01")  
  
 電腦監視器上稱為圖片項目或像素為單位的點的矩形陣列建立它的顯示畫面。 出現在螢幕的像素數目從一部監視器到下一步，以及設定而有所不同個別的監視器顯示的像素數目可以通常是在某個程度使用者。  
  
 ![向量圖形](./media/aboutgdip02-art02.gif "AboutGdip02_Art02")  
  
 當您使用[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]繪製線條、 矩形或曲線時，您可以提供要繪製項目的特定索引鍵資訊。 比方說，您可以藉由提供兩個點，來指定一條線，而您可以藉由提供一個點、 高度和寬度指定矩形。 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 若要判斷哪一個像素為單位必須開啟，以顯示線條、 矩形或曲線的顯示驅動程式軟體一起運作。 下圖顯示從點 （4，2） 顯示一條線，以點 （12，8） 開啟的像素。  
  
 ![向量圖形](./media/aboutgdip02-art03.gif "AboutGdip02_Art03")  
  
 經過一段時間，某些基本的建置組塊證明為十分最適用於建立二維的圖片。 這些建置組塊，所有支援的[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]下, 面清單中指定：  
  
-   線條  
  
-   矩形  
  
-   省略符號  
  
-   Arcs  
  
-   多邊形  
  
-   基線曲線  
  
-   貝茲曲線  
  
## <a name="methods-for-drawing-with-a-graphics-object"></a>繪製圖形物件的方法  
 <xref:System.Drawing.Graphics>類別內[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]提供下列方法來繪製上述清單中的項目： <xref:System.Drawing.Graphics.DrawLine%2A>， <xref:System.Drawing.Graphics.DrawRectangle%2A>， <xref:System.Drawing.Graphics.DrawEllipse%2A>， <xref:System.Drawing.Graphics.DrawPolygon%2A>， <xref:System.Drawing.Graphics.DrawArc%2A>， <xref:System.Drawing.Graphics.DrawCurve%2A> （適用於基本曲線），以及<xref:System.Drawing.Graphics.DrawBezier%2A>. 每一種方法多載;也就是說，每一種方法支援數個不同的參數清單。 比方說，一個變化<xref:System.Drawing.Graphics.DrawLine%2A>方法會接收<xref:System.Drawing.Pen>物件和四個整數，另一種變化的同時<xref:System.Drawing.Graphics.DrawLine%2A>方法會接收<xref:System.Drawing.Pen>物件和兩個<xref:System.Drawing.Point>物件。  
  
 繪製線條、 矩形和貝茲曲線的方法有複數隨附的方法，繪製單一呼叫中的數個項目： <xref:System.Drawing.Graphics.DrawLines%2A>， <xref:System.Drawing.Graphics.DrawRectangles%2A>，和<xref:System.Drawing.Graphics.DrawBeziers%2A>。 此外，<xref:System.Drawing.Graphics.DrawCurve%2A>方法具有附屬方法<xref:System.Drawing.Graphics.DrawClosedCurve%2A>，關閉的曲線，藉由連接曲線的結束點的開始點。  
  
 所有的繪圖方法<xref:System.Drawing.Graphics>類別搭配工作<xref:System.Drawing.Pen>物件。 若要繪製的任何項目，您必須建立至少兩個物件：<xref:System.Drawing.Graphics>物件和<xref:System.Drawing.Pen>物件。 <xref:System.Drawing.Pen>物件會儲存屬性，例如線條寬度和色彩，要繪製的項目。 <xref:System.Drawing.Pen>物件做為其中一個引數傳遞至繪圖的方法。 例如，一個變化<xref:System.Drawing.Graphics.DrawLine%2A>方法會接收<xref:System.Drawing.Pen>物件和四個整數，如下列的範例中，以繪製矩形的寬度為 100，高度為 50 和的左上角中所示 20 (10）：  
  
 [!code-csharp[LinesCurvesAndShapes#11](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#11)]
 [!code-vb[LinesCurvesAndShapes#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#11)]  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [線條、曲線和形狀](lines-curves-and-shapes.md)
- [如何：建立繪圖的圖形物件](how-to-create-graphics-objects-for-drawing.md)
