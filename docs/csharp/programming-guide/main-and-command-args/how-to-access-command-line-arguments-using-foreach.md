---
title: 作法：使用 foreach 存取命令列引數 - C# 程式設計指南
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- command-line arguments [C#]
ms.assetid: 89c3e335-3f5b-4e24-8c5a-b8036561fe8a
ms.openlocfilehash: 5813ad573e89886ba991ca8cbcebb7232af05821
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/28/2019
ms.locfileid: "56971672"
---
# <a name="how-to-access-command-line-arguments-using-foreach-c-programming-guide"></a>作法：使用 foreach 存取命令列引數 (C# 程式設計指南)
逐一查看陣列的另一種方法是使用 [foreach](../../../csharp/language-reference/keywords/foreach-in.md) 陳述式，如本例所示。 `foreach` 陳述式可用來逐一查看陣列、.NET Framework 集合類別，或實作 <xref:System.Collections.IEnumerable> 介面的任何類別或結構。  
  
> [!NOTE]
>  在 Visual Studio 中執行應用程式時，您可以在[專案設計工具、偵錯頁面](/visualstudio/ide/reference/debug-page-project-designer)中指定命令列引數。  
  
## <a name="example"></a>範例  
 本例會示範如何使用 `foreach` 印出命令列引數。  
  
 [!code-csharp[csProgGuideMain#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideMain/CS/Class2.cs#10)]  
  
 [!code-csharp[csProgGuideMain#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideMain/CS/Class1.cs#11)]  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Array>
- <xref:System.Collections>
- [使用 csc.exe 建置命令列](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)
- [foreach、in](../../../csharp/language-reference/keywords/foreach-in.md)
- [Main() 和命令列引數](../../../csharp/programming-guide/main-and-command-args/index.md)
- [如何：顯示命令列引數](../../../csharp/programming-guide/main-and-command-args/how-to-display-command-line-arguments.md)
- [Main() 傳回值](../../../csharp/programming-guide/main-and-command-args/main-return-values.md)
