---
title: HOW TO：從 Visual Basic 參考 COM 物件
ms.date: 07/20/2015
helpviewer_keywords:
- COM interop [Visual Basic], referencing COM objects
- referencing objects, COM objects from Visual Basic
- objects [Visual Basic], referencing
- COM objects, referencing
- interop assemblies
ms.assetid: 9c518fb4-27d9-4112-9e6a-5a7d0210af6f
ms.openlocfilehash: 0327c497025630747e526503556f4a1705948850
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59295259"
---
# <a name="how-to-reference-com-objects-from-visual-basic"></a>HOW TO：從 Visual Basic 參考 COM 物件
在 Visual Basic 中將參考加入至具有型別程式庫的 COM 物件需要建立 interop 組件的 COM 程式庫。 參考 COM 物件的成員會路由傳送至的 interop 組件，且接著轉送到實際的 COM 物件。 從 COM 物件的回應會路由傳送至的 interop 組件，並轉送至您[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]應用程式。  
  
 您可以參考 COM 物件，而不需使用 interop 組件中的.NET 組件內嵌 COM 物件的型別資訊。 若要內嵌類型資訊，請設定`Embed Interop Types`屬性設`True`的 COM 物件的參考。 如果您正在使用命令列編譯器來編譯，請使用`/link`參考的 COM 程式庫的選項。 如需詳細資訊，請參閱 < [/link (Visual Basic)](../../../visual-basic/reference/command-line-compiler/link.md)。  
  
 Visual Basic 會自動建立 interop 組件，當您將整合式的開發環境 (IDE) 中的型別程式庫的參考。 從命令列時，您可以使用 Tlbimp 公用程式來手動建立 interop 組件。  
  
### <a name="to-add-references-to-com-objects"></a>將參考加入至 COM 物件  
  
1. 在上**專案**功能表上，選擇**加入參考**，然後按一下  **COM**在對話方塊中的索引標籤。  
  
2. 選取您想要從清單中的 COM 物件使用的元件。  
  
3. 若要簡化的 interop 組件的存取，將新增`Imports`頂端的類別或模組中，您會使用 COM 物件的陳述式。 例如，下列程式碼範例匯入命名空間`INKEDLib`中所參考的物件`Microsoft InkEdit Control 1.0`程式庫。  
  
     [!code-vb[VbVbalrInterop#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#40)]  
  
### <a name="to-create-an-interop-assembly-using-tlbimp"></a>若要建立使用 Tlbimp 的 interop 組件  
  
1. 如果尚不搜尋路徑的一部分，而且您目前不在其所在的目錄，則您可以加入搜尋路徑中，Tlbimp 的位置。  
  
2. 呼叫 Tlbimp 從命令提示字元，提供下列資訊：  
  
    -   包含型別程式庫的 DLL 的名稱和位置  
  
    -   名稱和命名空間的位置資訊應放置的位置  
  
    -   目標的 interop 組件的名稱和位置  
  
     下列程式碼提供一個範例：  
  
    ```  
    Tlbimp test3.dll /out:NameSpace1 /out:Interop1.dll  
    ```  
  
     您可以使用 Tlbimp 建立 interop 組件的類型程式庫，即使未註冊的 COM 物件。 不過，您必須正確它們要使用的電腦上註冊 interop 組件所參考的 COM 物件。 您可以使用 Regsvr32 公用程式隨附於 Windows 作業系統中註冊的 COM 物件。  
  
## <a name="see-also"></a>另請參閱

- [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)
- [Tlbimp.exe (類型程式庫匯入工具)](../../../framework/tools/tlbimp-exe-type-library-importer.md)
- [Tlbexp.exe (類型程式庫匯出工具)](../../../framework/tools/tlbexp-exe-type-library-exporter.md)
- [逐步解說：實作 COM 物件的繼承](../../../visual-basic/programming-guide/com-interop/walkthrough-implementing-inheritance-with-com-objects.md)
- [互通性的疑難排解](../../../visual-basic/programming-guide/com-interop/troubleshooting-interoperability.md)
- [Imports 陳述式 (.NET 命名空間和類型)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
