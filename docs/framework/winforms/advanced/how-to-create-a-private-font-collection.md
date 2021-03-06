---
title: HOW TO：建立私用字型集合
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- private font collections [Windows Forms], creating
- fonts [Windows Forms], creating private collections
ms.assetid: 6533d5e5-a8dc-4b76-9fc4-3bf75c8b9212
ms.openlocfilehash: f78d48c88b72388676f5e7ae963b98d8f1b4beac
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59210682"
---
# <a name="how-to-create-a-private-font-collection"></a>HOW TO：建立私用字型集合
<xref:System.Drawing.Text.PrivateFontCollection>類別繼承自<xref:System.Drawing.Text.FontCollection>抽象基底類別。 您可以使用<xref:System.Drawing.Text.PrivateFontCollection>来維護一組專為您的應用程式的字型的物件。 私用字型集合可以包含已安裝的系統字型，以及您在尚未安裝在電腦的字型。 若要將字型檔案加入至私用字型集合中，呼叫<xref:System.Drawing.Text.PrivateFontCollection.AddFontFile%2A>方法的<xref:System.Drawing.Text.PrivateFontCollection>物件。  
  
 <xref:System.Drawing.Text.FontCollection.Families%2A>的屬性<xref:System.Drawing.Text.PrivateFontCollection>物件包含的陣列<xref:System.Drawing.FontFamily>物件。  
  
 私用字型集合中的字型家族數目不一定與字型檔案已加入至集合的數目相同。 例如，假設您將 ArialBd.tff、 Times.tff 和 TimesBd.tff 檔案新增至集合。 將會有三個檔案，但集合中的只有兩個系列因為 Times.tff 和 TimesBd.tff 屬於相同的系列。  
  
## <a name="example"></a>範例  
 下列範例會將在下列三個字型檔案<xref:System.Drawing.Text.PrivateFontCollection>物件：  
  
-   C:\\*systemroot*\Fonts\Arial.tff (Arial, regular)  
  
-   C:\\*systemroot*\Fonts\CourBI.tff (Courier New 粗斜體)  
  
-   C:\\*systemroot*\Fonts\TimesBd.tff （新細明體，粗體顯示）  
  
 程式碼會擷取陣列<xref:System.Drawing.FontFamily>物件從<xref:System.Drawing.Text.FontCollection.Families%2A>屬性<xref:System.Drawing.Text.PrivateFontCollection>物件。  
  
 每個<xref:System.Drawing.FontFamily>物件在集合中，程式碼會呼叫<xref:System.Drawing.FontFamily.IsStyleAvailable%2A>方法，以判斷是否有可用的各種樣式 （一般、 粗體、 斜體、 粗體斜體、 底線和刪除線）。 引數傳遞給<xref:System.Drawing.FontFamily.IsStyleAvailable%2A>方法屬於<xref:System.Drawing.FontStyle>列舉型別。  
  
 如果指定的家族樣式組合可供使用，<xref:System.Drawing.Font>物件建構是使用該家族和樣式。 第一個引數傳遞給<xref:System.Drawing.Font.%23ctor%2A>建構函式是字型系列名稱 (不<xref:System.Drawing.FontFamily>物件在此情況下的其他變化<xref:System.Drawing.Font.%23ctor%2A>建構函式)。 在後<xref:System.Drawing.Font>建構物件，則會傳遞至<xref:System.Drawing.Graphics.DrawString%2A>方法<xref:System.Drawing.Graphics>類別，以顯示系列名稱，以及該樣式的名稱。  
  
 下列程式碼的輸出大致如下圖所示的輸出：  
  
 ![如果螢幕擷取畫面顯示各種字型中的文字。](./media/how-to-create-a-private-font-collection/various-fonts-text-output.png)  
  
 Arial.tff （這新增下列程式碼範例中的私用字型集合） 是新細明體的一般樣式字型檔案。 不過，要注意的是，程式輸出會顯示數個可用的樣式，而不是一般的新細明體字型系列。 這是因為[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]可以模擬的粗體、 斜體和粗體斜體樣式規則的樣式。 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 也可以產生底線和 strikeouts 規則的樣式。  
  
 同樣地，[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]粗體樣式或斜體樣式的粗體斜體樣式模擬。 程式輸出顯示在即使 TimesBd.tff （新細明體，粗體顯示） 是唯一可用於時間系列粗體的斜體樣式集合中的次檔案。  
  
 [!code-csharp[System.Drawing.FontsAndText#51](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#51)]
 [!code-vb[System.Drawing.FontsAndText#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#51)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 上述範例中專為搭配 Windows Form 使用，而且需要<xref:System.Windows.Forms.PaintEventArgs> `e`，這是參數的<xref:System.Windows.Forms.PaintEventHandler>。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Drawing.Text.PrivateFontCollection>
- [使用字型和文字](using-fonts-and-text.md)
