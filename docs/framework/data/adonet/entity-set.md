---
title: 實體集
ms.date: 03/30/2017
ms.assetid: 59ec6ab0-88e5-4d25-b112-7a4eccbe61f0
ms.openlocfilehash: 7fcaa2cb9bac02271940a712d4d044df25d7d4cf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126616"
---
# <a name="entity-set"></a>實體集
*實體集*是邏輯容器的執行個體[實體類型](../../../../docs/framework/data/adonet/entity-type.md)和衍生自該實體類型的任何類型的執行個體。 (有關衍生型別的資訊，請參閱[實體資料模型：繼承](../../../../docs/framework/data/adonet/entity-data-model-inheritance.md)。)實體類型和實體集之間的關聯性相當於一個資料列與關聯式資料庫中的資料表之間的關聯性：資料列，例如實體類型描述資料結構，和資料表，這類實體集包含指定的結構的執行個體。 實體集不是資料模型建構，也就是說，它不會描述資料結構。 反之，實體集會提供建構，讓裝載或儲存環境 (例如 Common Language Runtime 或 SQL Server 資料庫) 群組實體類型執行個體，以將其對應至資料存放區。  
  
 實體集內定義[實體容器](../../../../docs/framework/data/adonet/entity-container.md)，這是實體集的邏輯群組並[關聯集](../../../../docs/framework/data/adonet/association-set.md)。  
  
 實體類型執行個體若要存在於實體集中，下列條件必須為 true：  
  
-   執行個體的類型必須與該實體集所依據的實體類型相同，或者執行個體的型別為該實體類型的子類型。  
  
-   [實體索引鍵](../../../../docs/framework/data/adonet/entity-key.md)的執行個體中是唯一的實體集。  
  
-   執行個體不存在於任何其他實體集中。  
  
    > [!NOTE]
    >  您可以使用相同的實體類型定義多個實體集，但指定實體類型的執行個體只能存在於一個實體集中。  
  
 您不需定義概念模型中每個實體類型的實體集。  
  
## <a name="example"></a>範例  
 下圖顯示包含三種實體類型 (`Book`、`Publisher` 和 `Author`) 的概念模型。  
  
 ![具有三種實體類型的範例模型](./media/entity-set/example-model-three-entity-types.gif)  
  
 下圖顯示以前述概念模型為基礎的兩個實體集 (`Books` 和 `Publishers`)，以及一個關聯集 `PublishedBy`)。 在 bi`Books`實體集代表的執行個體`Book`在執行階段的實體類型。 同樣地，代表 Pj`Publisher`執行個體中`Publishers`實體集。 BiPj 表示的執行個體`PublishedBy`中的關聯`PublishedBy`關聯集。  
  
 ![如果螢幕擷取畫面顯示設定範例。](./media/entity-set/sets-example-association.gif)  
  
 [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)會使用稱為概念結構定義語言的特定領域語言 (DSL) ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 來定義概念模型。 下列 CSDL 定義實體容器，上述概念模型中的每個實體類型皆具有一個實體集。 請注意，每個實體集名稱和實體類型都是使用 XML 屬性定義的。  
  
 [!code-xml[EDM_Example_Model#EntityContainerExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entitycontainerexample)]  
  
 您可以定義每個類型的多重實體集 (MEST)。 下列 CSDL 所定義的實體容體具有兩個 `Book` 實體類型的實體集：  
  
 [!code-xml[EDM_Example_Model#MESTExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books2.edmx#mestexample)]  
  
## <a name="see-also"></a>另請參閱

- [實體資料模型索引鍵概念](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [實體資料模型](../../../../docs/framework/data/adonet/entity-data-model.md)
