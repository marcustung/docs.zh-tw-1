---
title: HOW TO：使用繼承選取器對話方塊繼承表單
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], forms
- Inheritance Picker dialog box
- inherited forms [Windows Forms], creating
ms.assetid: 969b4c04-12aa-4297-93a2-0ae747447823
ms.openlocfilehash: 5ae1c236835141b10bc704cd39f55de6e3e974b0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59342085"
---
# <a name="how-to-inherit-forms-using-the-inheritance-picker-dialog-box"></a>HOW TO：使用繼承選取器對話方塊繼承表單
繼承表單或其他物件的最簡單方式是使用 [繼承選取器] 對話方塊。 您可以藉助它來利用在其他方案中已建立的程式碼或使用者介面 (UI)。  
  
> [!NOTE]
>  為了繼承包含 [繼承選取器] 對話方塊的表單，包含該表單的專案必須已建置為可執行檔或 DLL。 若要建置專案，請從 [建置] 功能表中選擇 [建置方案]。  
>   
>  根據您目前使用的設定或版本，您所看到的對話方塊與功能表命令可能會與 [說明] 中描述的不同。 若要變更設定，請從 [ **工具** ] 功能表中選取 [ **匯入和匯出設定** ]。 如需詳細資訊，請參閱[將 Visual Studio IDE 個人化](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
### <a name="to-create-a-windows-form-inherited-from-an-existing-form-by-using-the-inheritance-picker"></a>使用繼承選取器建立繼承自現有表單的 Windows Form   
  
1. 在 [專案] 功能表中，選擇 [新增 Windows Form]。  
  
     [新增項目] 對話方塊隨即開啟。  
  
2. 搜尋**繼承的表單**範本從 searchbox，或是按一下**Windows Forms**分類中，選取它，並將它在命名**名稱** 方塊中。 按一下 [新增] 按鈕繼續。  
  
     [繼承選取器] 對話方塊隨即開啟。 如果目前的專案已包含表單，它們會顯示在 [繼承選取器] 對話方塊。  
  
3. 若要自另一個組件中的表單繼承，按一下 [瀏覽] 按鈕。  
  
4. 在 [選取包含要繼承元件的檔案] 對話方塊中，巡覽至包含您想要的表單或模組的專案。  
  
5. 按一下 .exe 或 .dll 檔案的名稱以選取它，然後按一下 [開啟] 按鈕。  
  
     這會讓您返回 [繼承選取器] 對話方塊，其中會立即列出元件及它所在的專案。  
  
6. 選取元件  
  
     在 [方案總管] 中，此元件已新增至您的專案。 如果它具有 UI，繼承表單一部分的控制項將會標示以圖像 (![螢幕擷取畫面的 Visual Basic 繼承符號](./media/how-to-inherit-forms-using-the-inheritance-picker-dialog-box/visual-basic-inheritance-glyph.gif))，並選取時，有框線，表示控制項具有的安全性層級superclass 表單。 對應至不同的安全性層級的行為會在下表中列出。  
  
    |控制項的安全性層級|設計工具和程式碼編輯器與繼承表單之可用的互動|  
    |-------------------------------|--------------------------------------------------------------------------------|  
    |Public|具有縮放控點的標準框線：可調整控制項大小和移動。 藉由宣告控制項的類別和外部的其他類別，可以在內部存取此控制項。|  
    |Protected|具有縮放控點的標準框線：可調整控制項大小和移動。 可以由宣告它的類別和繼承自父類別的任何類別內部存取，但無法由外部類別所存取。|  
    |Protected Internal (在 Visual Basic 中為 Protected Friend)|具有縮放控點的標準框線：可調整控制項大小和移動。 可以由宣告它的類別、繼承自父類別的任何類別以及包含它的組件之其他成員內部存取。|  
    |Internal (在 Visual Basic 中為 Friend)|在表單上顯示的沒有縮放控點之標準框線，其屬性於 [屬性] 視窗中可見。 不過，此控制項的所有層面都會被視為唯讀。 您無法移動、調整控制項大小，或變更其屬性。 如果控制項為其他控制項的容器，例如群組方塊，則無法加入新的控制項，也不能移除現有的控制項，即使這些控制項為公用。 該控制項只能由包含它的組件之其他成員存取。|  
    |Private|在表單上顯示的沒有縮放控點之標準框線，其屬性於 [屬性] 視窗中可見。 不過，此控制項的所有層面都會被視為唯讀。 您無法移動、調整控制項大小，或變更其屬性。 如果控制項為其他控制項的容器，例如群組方塊，則無法加入新的控制項，也不能移除現有的控制項，即使這些控制項為公用。 該控制項只能由宣告它的類別存取。|  
  
     如需更改基底表單外觀的相關資訊，請參閱[修改基底表單外觀的效果](effects-of-modifying-base-form-appearance.md)。  
  
    > [!NOTE]
    >  當您將繼承的控制項和元件與標準控制項和 Windows Form 上的元件結合時，您可能會遇到疊置順序衝突。 您可以藉由修改疊置順序來修正，其作法是在 [格式]  功能表中按一下，指向 [順序]，然後按一下 [提到最上層] 或 [移到最下層]。 控制項的疊置順序的相關資訊，請參閱[How to:在 Windows Forms 上的物件分層](../controls/how-to-layer-objects-on-windows-forms.md)。  
  
## <a name="see-also"></a>另請參閱

- [Inherits 陳述式](~/docs/visual-basic/language-reference/statements/inherits-statement.md)
- [using](~/docs/csharp/language-reference/keywords/using.md)
- [修改基底表單外觀的效果](effects-of-modifying-base-form-appearance.md)
- [Windows Forms 視覺繼承](windows-forms-visual-inheritance.md)
