---
title: 常數運算式
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9d98a7be-b110-4edb-8eba-bed10f250b6d
ms.openlocfilehash: 10c74ede8d490bf96a9d0855889669bdc2628b01
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209199"
---
# <a name="constant-expressions"></a>常數運算式
常數運算式是由常數值所組成。 常數值會直接轉換成常數命令樹運算式，而不需在用戶端上進行任何轉譯。 其中包括產生常數值的運算式。 因此，所有牽涉到常數的運算式應該都會有資料來源行為。 這樣可能會產生與 CLR 行為不同的行為。  
  
 下列範例會顯示在伺服器上評估的常數運算式。  
  
 [!code-csharp[DP L2E Conceptual Examples#ConstantExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#constantexpression)]
 [!code-vb[DP L2E Conceptual Examples#ConstantExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#constantexpression)]  
  
 [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] 不支援使用使用者類別當做常數。 但是，使用者類別上的屬性參考會視為常數，而且將會轉換成命令樹常數運算式，並在資料來源上執行。  
  
## <a name="see-also"></a>另請參閱

- [LINQ to Entities 查詢中的運算式](../../../../../../docs/framework/data/adonet/ef/language-reference/expressions-in-linq-to-entities-queries.md)
