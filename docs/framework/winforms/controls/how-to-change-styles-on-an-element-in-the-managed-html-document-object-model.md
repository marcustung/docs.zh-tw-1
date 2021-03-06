---
title: HOW TO：變更受控 HTML 文件物件模型的項目樣式
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- managed HTML DOM [Windows Forms], changing styles on elements
ms.assetid: 154e8d9f-3e2d-4e8b-a6f3-c85a070e9cc1
ms.openlocfilehash: 804041991199dd2722e3a0f38800bafd8933bbab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59333661"
---
# <a name="how-to-change-styles-on-an-element-in-the-managed-html-document-object-model"></a>HOW TO：變更受控 HTML 文件物件模型的項目樣式

您可以使用在 HTML 中的樣式，來控制文件和其項目的外觀。 <xref:System.Windows.Forms.HtmlDocument> 並<xref:System.Windows.Forms.HtmlElement>支援<xref:System.Windows.Forms.HtmlElement.Style%2A>採用下列格式的樣式字串屬性：

`name1:value1;...;nameN:valueN;`

以下是`DIV`字型設定為要以粗體顯示的 新細明體和所有文字的樣式字串：

`<DIV style="font-face:arial;font-weight:bold;">`

`Hello, world!`

`</DIV>`

操作使用的樣式問題<xref:System.Windows.Forms.HtmlElement.Style%2A>屬性是，它可以證明難以加入和移除字串中的個別的樣式設定。 例如，它會變得複雜的程序，為您呈現先前斜體文字，每當使用者將游標置於`DIV`，並採取關閉當游標離開斜體`DIV`。 如果您需要處理大量的這種方式中的樣式，時間就會成為問題。

下列程序包含您可用來輕鬆地操作 HTML 文件和項目樣式的程式碼。 在程序需要您知道如何執行基本工作，在 Windows Forms 中，例如建立新的專案，以及將控制項加入表單。

### <a name="to-process-style-changes-in-a-windows-forms-application"></a>處理 Windows Forms 應用程式中的樣式變更

1. 建立新的 Windows Form 專案。

2. 建立新的類別檔案，以適合您的程式語言的延伸模組。

3. 複製`StyleGenerator`類別檔中，類別在本主題的範例 > 一節中的程式碼，並儲存程式碼。

4. 將下列 HTML 儲存到名為 Test.htm 檔案。

    ```html
    <HTML>
        <BODY>

            <DIV style="font-face:arial;font-weight:bold;">
                Hello, world!
            </DIV><P>

            <DIV>
                Hello again, world!
            </DIV><P>

        </BODY>
    </HTML>
    ```

5. 新增<xref:System.Windows.Forms.WebBrowser>控制項，名為`webBrowser1`至主要表單的專案。

6. 將下列程式碼新增至您的專案程式碼檔案。

    > [!IMPORTANT]
    >  請確認`webBrowser1_DocumentCompleted`事件處理常式設定為接聽程式<xref:System.Windows.Forms.WebBrowser.DocumentCompleted>事件。 在 Visual Studio 中，按兩下<xref:System.Windows.Forms.WebBrowser>控制; 請在文字編輯器中，設定接聽程式以程式設計的方式。  
  
     [!code-csharp[ManagedDOMStyles#2](~/samples/snippets/csharp/VS_Snippets_Winforms/ManagedDOMStyles/CS/Form1.cs#2)]
     [!code-vb[ManagedDOMStyles#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ManagedDOMStyles/VB/Form1.vb#2)]  
  
7. 執行專案。 執行您的資料指標在第一個`DIV`觀察程式碼的效果。  
  
## <a name="example"></a>範例  
 下列程式碼範例顯示的完整程式碼`StyleGenerator`類別，它會剖析現有的樣式值，支援加入、 變更和移除設定的樣式，並傳回新的樣式值，變更要求。  
  
 [!code-csharp[ManagedDOMStyles#1](~/samples/snippets/csharp/VS_Snippets_Winforms/ManagedDOMStyles/CS/StyleGenerator.cs#1)]
 [!code-vb[ManagedDOMStyles#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ManagedDOMStyles/VB/StyleGenerator.vb#1)]  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Windows.Forms.HtmlElement>
