---
title: '- （減）(Entity SQL)'
ms.date: 03/30/2017
ms.assetid: bc4327f9-09c0-438f-a008-927c5c478040
ms.openlocfilehash: 2e4c08788ea57000e189c8371f0494641931184b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316683"
---
# <a name="--subtract-entity-sql"></a>- (減號) (Entity SQL)
兩個數字相減。  
  
## <a name="syntax"></a>語法  
  
```  
expression - expression  
```  
  
## <a name="arguments"></a>引數  
 `expression`  
 任何一個數值資料型別的任何有效運算式。  
  
## <a name="result-types"></a>結果型別  
 從兩個引數的隱含型別提升產生的資料型別。 如需有關隱含型別提升的詳細資訊，請參閱[型別系統](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md)。  
  
## <a name="example"></a>範例  
 下列 Entity SQL 查詢會使用 - 算術運算子讓兩個數字相減。 此查詢是根據 AdventureWorks Sales Model。 若要編譯及執行此查詢，請遵循以下步驟：  
  
1. 請依照下列中的程序[How to:執行可傳回 StructuralType 結果的查詢](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)。  
  
2. 將下列查詢當成引數，傳遞至 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-csharp[DP EntityServices Concepts 2#SUBTRACT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#subtract)]  
  
## <a name="see-also"></a>另請參閱

- [Entity SQL 參考](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
