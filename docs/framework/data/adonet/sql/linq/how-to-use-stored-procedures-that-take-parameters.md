---
title: HOW TO：使用有參數的預存程序
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b935fd84-cb9c-4205-8c48-658d5db2ec93
ms.openlocfilehash: 8dd463c895efcddfe288fe1dc8571981872d9d80
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181762"
---
# <a name="how-to-use-stored-procedures-that-take-parameters"></a>HOW TO：使用有參數的預存程序
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 會將輸出參數對應至參考參數，而且會針對實值型別 (Value Type)，將參數宣告為可為 Null。  
  
 如需如何使用輸入的參數中的查詢會傳回一個資料列集的範例，請參閱[How to:傳回資料列集](../../../../../../docs/framework/data/adonet/sql/linq/how-to-return-rowsets.md)。  
  
## <a name="example"></a>範例  
 下列範例取用單一輸入參數 (客戶 ID)，並傳回輸出參數 (該客戶的總銷售量)。  
  
```  
CREATE PROCEDURE [dbo].[CustOrderTotal]   
@CustomerID nchar(5),  
@TotalSales money OUTPUT  
AS  
SELECT @TotalSales = SUM(OD.UNITPRICE*(1-OD.DISCOUNT) * OD.QUANTITY)  
FROM ORDERS O, "ORDER DETAILS" OD  
where O.CUSTOMERID = @CustomerID AND O.ORDERID = OD.ORDERID  
```  
  
 [!code-csharp[DLinqSprox#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/northwind-sprox.cs#2)]
 [!code-vb[DLinqSprox#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/northwind-sprox.vb#2)]  
  
## <a name="example"></a>範例  
 您可如下呼叫這個預存程序 (Stored Procedure)：  
  
 [!code-csharp[DLinqSprox#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/Program.cs#3)]
 [!code-vb[DLinqSprox#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>另請參閱

- [預存程序](../../../../../../docs/framework/data/adonet/sql/linq/stored-procedures.md)
- [下載範例資料庫](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
- [使用可為 Null 的型別](~/docs/csharp/programming-guide/nullable-types/using-nullable-types.md)
- [可為 Null 的值類型](~/docs/visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
