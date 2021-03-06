---
title: HOW TO：排列 MDI 子表單
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- child forms [Windows Forms], arranging
- MDI [Windows Forms], arranging child forms
ms.assetid: a0786378-3206-4ccc-898e-7d3b38cc5089
ms.openlocfilehash: c7a9d03ef60586e1162f088d662dfe44bbdcb591
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59317229"
---
# <a name="how-to-arrange-mdi-child-forms"></a>HOW TO：排列 MDI 子表單
應用程式通常會包含 [並排]、[重疊顯示] 和 [排列] 等動作的功能表命令，以便控制所開啟之 MDI 子表單的配置。 您可以搭配使用 <xref:System.Windows.Forms.Form.LayoutMdi%2A> 方法和其中一個 <xref:System.Windows.Forms.MdiLayout> 列舉值，來重新排列 MDI 父表單中的子表單。  
  
 <xref:System.Windows.Forms.MdiLayout> 列舉值會以重疊顯示、水平或垂直並排方式來顯示子表單，或將子表單當做排列在 MDI 表單下方的子表單圖示來顯示。 這些值有相同的效果，為 Windows 命令**重疊顯示視窗**，**並排顯示視窗**，**堆疊顯示視窗**，和**顯示桌面**分別。  
  
 這些方法通常會當做由功能表項目的 <xref:System.Windows.Forms.Control.Click> 事件所呼叫的事件處理常式來使用。 如此一來，具有「重疊顯示視窗」文字的功能表項目就可在 MDI 子視窗上呈現出指定的效果。  
  
### <a name="to-arrange-child-forms"></a>排列子表單  
  
1. 在方法中，使用 <xref:System.Windows.Forms.Form.LayoutMdi%2A> 方法設定 MDI 父表單的 <xref:System.Windows.Forms.MdiLayout> 列舉。 下列範例針對 MDI 父表單 (<xref:System.Windows.Forms.MdiLayout.Cascade?displayProperty=nameWithType>) 的子視窗，使用 `Form1` 列舉值。 列舉型別會使用於程式碼中的事件處理常式<xref:System.Windows.Forms.Control.Click>事件的**串聯 Windows**功能表項目。  
  
    ```vb  
    Protected Sub CascadeWindows_Click(ByVal sender As System.Object, ByVal e As System.EventArgs)  
       Me.LayoutMdi(System.Windows.Forms.MdiLayout.Cascade)  
    End Sub  
    ```  
  
    ```csharp  
    protected void CascadeWindows_Click(object sender, System.EventArgs e){  
       this.LayoutMdi(System.Windows.Forms.MdiLayout.Cascade);  
    }  
    ```  
  
    > [!NOTE]
    >  您也可以藉由變更所使用的 <xref:System.Windows.Forms.MdiLayout> 列舉值，來並排顯示視窗，以及將視窗排列為圖示。  
  
2. 如果使用 Visual C#，請將下列程式碼置於表單的建構函式中，以註冊事件處理常式。  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
## <a name="see-also"></a>另請參閱

- [多重文件介面 (MDI) 應用程式](multiple-document-interface-mdi-applications.md)
- [如何：建立 MDI 父表單](how-to-create-mdi-parent-forms.md)
- [如何：建立 MDI 子表單](how-to-create-mdi-child-forms.md)
- [如何：決定作用中的 MDI 子系](how-to-determine-the-active-mdi-child.md)
- [如何：將資料傳送至作用中的 MDI 子系](how-to-send-data-to-the-active-mdi-child.md)
