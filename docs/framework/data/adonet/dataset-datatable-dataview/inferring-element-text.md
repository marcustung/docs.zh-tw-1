---
title: 推斷項目文字
ms.date: 03/30/2017
ms.assetid: 789799e5-716f-459f-a168-76c5cf22178b
ms.openlocfilehash: 6ffe8f2fbf01fbe8dfa9d78f3dfb9e39b6e80b16
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59224958"
---
# <a name="inferring-element-text"></a>推斷項目文字
如果項目包含文字，而且沒有任何子項目，來推斷為資料表 （具有屬性的項目） 或重複的項目，例如新的資料行同名**TableName_Text**會加入項目，推斷的資料表。 項目中包含的文字會加入資料表中的資料列，並儲存在新資料行內。 **ColumnMapping**的新資料行的屬性會設定為**MappingType.SimpleContent**。  
  
 例如，請考量下列 XML。  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1">Text1</Element1>  
</DocumentElement>  
```  
  
 推斷程序會產生一個名為資料表**Element1**兩個資料行： **attr1**並**Element1_Text**。 **ColumnMapping**屬性**attr1**資料行都會設定為**MappingType.Attribute**。 **ColumnMapping**屬性**Element1_Text**資料行都會設定為**MappingType.SimpleContent**。  
  
 **資料集：** DocumentElement  
  
 **資料表：** Element1  
  
|attr1|Element1_Text|  
|-----------|--------------------|  
|value1|Text1|  
  
 如果項目包含文字，但是它的項目子系也包含文字，則不會有資料行加入資料表來儲存項目中包含的文字。 包含在項目中的文字會被忽略，而項目子系中的文字會被包含在資料表的資料列內。 例如，請考量下列 XML。  
  
```xml  
<Element1>  
  Text1  
  <ChildElement1>Text2</ChildElement1>  
  Text3  
</Element1>  
```  
  
 推斷程序會產生一個名為資料表**Element1**的資料行**ChildElement1**。 文字**ChildElement1**項目將會包含在資料表中的資料列。 其他文字則被忽略。 **ColumnMapping**屬性**ChildElement1**資料行都會設定為**MappingType.Element**。  
  
 **資料集：** DocumentElement  
  
 **資料表：** Element1  
  
|ChildElement1|  
|-------------------|  
|Text2|  
  
## <a name="see-also"></a>另請參閱

- [從 XML 推斷資料集關聯式結構](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [從 XML 載入資料集](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [從 XML 載入資料集結構描述資訊](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [在 DataSet 中使用 XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [DataSet、DataTable 和 DataView](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [ADO.NET Managed 提供者和 DataSet 開發人員中心](https://go.microsoft.com/fwlink/?LinkId=217917)
