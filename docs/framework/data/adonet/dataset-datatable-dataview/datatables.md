---
title: DataTables
ms.date: 03/30/2017
ms.assetid: 52ff0e32-3e5a-41de-9a3b-7b04ea52b83e
ms.openlocfilehash: f6509400d7f6633749155f778e3ba58ec6c27ec2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207314"
---
# <a name="datatables"></a>DataTables
<xref:System.Data.DataSet> 是由資料表集合、關係和條件約束所組成。 在 ADO.NET 中，<xref:System.Data.DataTable>物件用來代表中的資料表**資料集**。 A **DataTable**表示記憶體中關聯式資料; 的一個資料表資料位於本機。以.NET 為基礎的應用程式它位於，但可以從資料來源，例如 Microsoft SQL Server 使用填入**DataAdapter**如需詳細資訊，請參閱[從 DataAdapter 填入 DataSet](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md).  
  
 **DataTable**類別是隸屬**System.Data** .NET Framework 類別程式庫內的命名空間。 您可以建立並使用**DataTable**獨立或成員的身分**資料集**，並**DataTable**物件也可以用於搭配其他.NET Framework 物件，包括<xref:System.Data.DataView>。 存取集合中的資料表**資料集**透過**資料表**屬性**資料集**物件。  
  
 資料表的結構描述 (或稱為結構) 是由資料行或條件約束來表示。 您定義的結構描述**DataTable**使用<xref:System.Data.DataColumn>物件，以及<xref:System.Data.ForeignKeyConstraint>和<xref:System.Data.UniqueConstraint>物件。 資料表的資料行可對應到資料來源中的資料行、包含運算式所得的值、自動累加其值或包含主索引鍵值。  
  
 結構描述時，除了**DataTable**也必須包含和排列資料的資料列。 <xref:System.Data.DataRow> 類別 (Class) 代表資料表所包含的實際資料。 您使用**DataRow**其屬性和方法以擷取、 評估和管理資料表中的資料。 當您存取和變更資料列中的資料**DataRow**物件會維護其目前和原始的狀態。  
  
 您可以使用一或多個資料表中的相關資料行，在資料表之間建立父子關係 (Parent-Child Relationship)。 您建立的關聯性**DataTable**物件，使用<xref:System.Data.DataRelation>。 **DataRelation**物件可以再用來傳回特定資料列相關的子系或父資料列。 如需詳細資訊，請參閱 <<c0> [ 新增 Datarelation](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/adding-datarelations.md)。  
  
## <a name="in-this-section"></a>本節內容  
 [建立 DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/creating-a-datatable.md)  
 說明如何建立**DataTable**並將它加入**DataSet**。  
  
 [DataTable 結構描述定義](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-schema-definition.md)  
 提供建立和使用的相關資訊**DataColumn**物件和條件約束。  
  
 [在 DataTable 中操作資料](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)  
 說明如何加入、修改和刪除資料表中的資料。 說明如何使用**DataTable**事件，以檢視資料表中的資料變更。  
  
 [處理 DataTable 事件](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/handling-datatable-events.md)  
 提供可用事件的相關資訊，供**DataTable**，包括已修改資料行的值，並新增或刪除資料列時的事件。  
  
## <a name="related-sections"></a>相關章節  
 [ADO.NET](../../../../../docs/framework/data/adonet/index.md)  
 描述 ADO.NET 的架構和元件，以及如何使用它們來存取現有資料來源和管理應用程式資料。  
  
 [DataSet、DataTable 和 DataView](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 提供 ADO.NET 的相關資訊**資料集**包括如何建立資料表之間的關聯性。  
  
 <xref:System.Data.Constraint>  
 提供參考資訊的相關**條件約束**物件。  
  
 <xref:System.Data.DataColumn>  
 提供參考資訊的相關**DataColumn**物件。  
  
 <xref:System.Data.DataSet>  
 提供參考資訊的相關**資料集**物件。  
  
 <xref:System.Data.DataTable>  
 提供參考資訊的相關**DataTable**物件。  
  
 [類別庫概觀](../../../../../docs/standard/class-library-overview.md)  
 提供.NET Framework 類別庫的概觀包括**系統**命名空間以及它的第二層命名空間**System.Data**。  
  
## <a name="see-also"></a>另請參閱

- [ADO.NET Managed 提供者和 DataSet 開發人員中心](https://go.microsoft.com/fwlink/?LinkId=217917)
