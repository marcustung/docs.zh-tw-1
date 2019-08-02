---
title: 選取集合類別
ms.date: 03/18/2019
ms.technology: dotnet-standard
helpviewer_keywords:
- last-in-first-out collections
- first-in-first-out collections
- collections [.NET Framework], selecting collection class
- indexed collections
- Collections classes
- grouping data in collections, selecting collection class
ms.assetid: ba049f9a-ce87-4cc4-b319-3f75c8ddac8a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 21c708f63faaedb9fbce60d7e4aef314f7a41ef8
ms.sourcegitcommit: 462dc41a13942e467984e48f4018d1f79ae67346
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "58185554"
---
# <a name="selecting-a-collection-class"></a>選取集合類別

請務必謹慎選擇您的集合類別。 使用錯誤的類型可能會限制您使用集合。  

> [!IMPORTANT]
> 避免在 <xref:System.Collections> 命名空間中使用那些型別。 由於泛型和並行版本的集合類型較安全，而且提供其他增強功能，因此建議使用這些版本。  

 請考慮下列問題：  
  
- 您是否需要循序清單，其中的項目通常會在擷取其值之後捨棄？  
  
  - 如果是，並且需要先進先出 (FIFO) 行為，請考慮使用 <xref:System.Collections.Queue> 類別或 <xref:System.Collections.Generic.Queue%601> 泛型類別。 如果需要後進先出 (LIFO) 行為，請考慮使用 <xref:System.Collections.Stack> 類別或 <xref:System.Collections.Generic.Stack%601> 泛型類別。 若要從多個執行緒進行安全存取，請使用並行版本 <xref:System.Collections.Concurrent.ConcurrentQueue%601> 和 <xref:System.Collections.Concurrent.ConcurrentStack%601>。  
  
  - 如果否，請考慮使用其他集合。  
  
- 您是否需要以特定順序 (例如 FIFO、LIFO 或隨機) 存取項目？  
  
  - <xref:System.Collections.Queue> 類別以及 <xref:System.Collections.Generic.Queue%601> 或 <xref:System.Collections.Concurrent.ConcurrentQueue%601> 泛型類別提供 FIFO 存取。 如需詳細資訊，請參閱[使用安全執行緒集合的時機](../../../docs/standard/collections/thread-safe/when-to-use-a-thread-safe-collection.md)。  
  
  - <xref:System.Collections.Stack> 類別以及 <xref:System.Collections.Generic.Stack%601> 或 <xref:System.Collections.Concurrent.ConcurrentStack%601> 泛型類別提供 LIFO 存取。 如需詳細資訊，請參閱[使用安全執行緒集合的時機](../../../docs/standard/collections/thread-safe/when-to-use-a-thread-safe-collection.md)。  
  
  - <xref:System.Collections.Generic.LinkedList%601> 泛型類別允許從頭到尾或從尾到頭進行循序存取。  
  
- 您是否需要依索引存取每個項目？  
  
  - <xref:System.Collections.ArrayList> 和 <xref:System.Collections.Specialized.StringCollection> 類別以及 <xref:System.Collections.Generic.List%601> 泛型類別，可依項目之以零為起始的索引來存取其項目。  
  
  - <xref:System.Collections.Hashtable>、<xref:System.Collections.SortedList>、<xref:System.Collections.Specialized.ListDictionary> 和 <xref:System.Collections.Specialized.StringDictionary> 類別以及 <xref:System.Collections.Generic.Dictionary%602> 和 <xref:System.Collections.Generic.SortedDictionary%602> 泛型類別，可依項目的索引鍵來存取其項目。  
  
  - <xref:System.Collections.Specialized.NameObjectCollectionBase> 和 <xref:System.Collections.Specialized.NameValueCollection> 類別以及 <xref:System.Collections.ObjectModel.KeyedCollection%602> 和 <xref:System.Collections.Generic.SortedList%602> 泛型類別，可依項目之以零為起始的索引或索引鍵來存取其項目。  
  
- 每個項目會包含一個值、一個索引鍵和一個值的組合，還是一個索引鍵和多個值的組合？  
  
  - 一個值：根據 <xref:System.Collections.IList> 介面或 <xref:System.Collections.Generic.IList%601> 泛型介面來使用任何集合。  
  
  - 一個索引鍵和一個值：根據 <xref:System.Collections.IDictionary> 介面或 <xref:System.Collections.Generic.IDictionary%602> 泛型介面來使用任何集合。  
  
  - 一個具有內嵌索引鍵的值：使用 <xref:System.Collections.ObjectModel.KeyedCollection%602> 泛型類別。  
  
  - 一個索引鍵和多個值：使用 <xref:System.Collections.Specialized.NameValueCollection> 類別。  
  
- 您是否需要使用與輸入項目不同的順序來排序項目？  
  
  - <xref:System.Collections.Hashtable> 類別會依其雜湊碼來排序其項目。  
  
  - <xref:System.Collections.SortedList> 類別，而 <xref:System.Collections.Generic.SortedList%602> 與 <xref:System.Collections.Generic.SortedDictionary%602> 泛型類別會依該索引鍵排序其元素。 排序次序是以 <xref:System.Collections.SortedList> 類別的 <xref:System.Collections.IComparer> 介面實作和 <xref:System.Collections.Generic.SortedList%602> 與 <xref:System.Collections.Generic.SortedDictionary%602> 泛型類別的 <xref:System.Collections.Generic.IComparer%601> 泛型介面實作為基礎。 在兩個泛型型別中，<xref:System.Collections.Generic.SortedDictionary%602> 提供比 <xref:System.Collections.Generic.SortedList%602> 更好的效能，而 <xref:System.Collections.Generic.SortedList%602> 會取用較少的記憶體。  
  
  - <xref:System.Collections.ArrayList> 提供 <xref:System.Collections.ArrayList.Sort%2A> 方法，這個方法接受 <xref:System.Collections.IComparer> 實作做為參數。 其對應的泛型版本 (<xref:System.Collections.Generic.List%601> 泛型類別) 會提供 <xref:System.Collections.Generic.List%601.Sort%2A> 方法，這個方法接受 <xref:System.Collections.Generic.IComparer%601> 泛型介面的實作做為參數。  
  
- 您是否需要快速搜尋和擷取資訊？  
  
  - 若為小型集合 (10 個項目或更少)，<xref:System.Collections.Specialized.ListDictionary> 的速度比 <xref:System.Collections.Hashtable> 更快。 <xref:System.Collections.Generic.Dictionary%602> 泛型類別提供比 <xref:System.Collections.Generic.SortedDictionary%602> 泛型類別更快的查閱速度。 多執行緒實作是 <xref:System.Collections.Concurrent.ConcurrentDictionary%602>。 <xref:System.Collections.Concurrent.ConcurrentBag%601> 會針對未排序的資料提供快速的多執行緒插入。 如需多執行緒型別的詳細資訊，請參閱[使用安全執行緒集合的時機](../../../docs/standard/collections/thread-safe/when-to-use-a-thread-safe-collection.md)。  
  
- 您是否需要只接受字串的集合？  
  
  - <xref:System.Collections.Specialized.StringCollection> (以 <xref:System.Collections.IList> 為基礎) 和 <xref:System.Collections.Specialized.StringDictionary> (以 <xref:System.Collections.IDictionary> 為基礎) 位於 <xref:System.Collections.Specialized> 命名空間中。  
  
  - 此外，您可以使用 <xref:System.Collections.Generic> 命名空間中的任何泛型集合類別做為強類型字串集合，方法是指定其泛型類型引數的 <xref:System.String> 類別。 例如，您可以將變數的型別宣告為 [List\<String>](xref:System.Collections.Generic.List%601) 或 [Dictionary<String,String>](xref:System.Collections.Generic.Dictionary%602)。
  
## <a name="linq-to-objects-and-plinq"></a>LINQ to Objects 和 PLINQ  
 只要物件類型實作 <xref:System.Collections.IEnumerable> 或 <xref:System.Collections.Generic.IEnumerable%601>，LINQ to Objects 就可讓開發人員使用 LINQ 提供的 API 查詢已存放在記憶體內的物件。 LINQ 查詢提供一般模式以存取資料，比標準的 `foreach` 迴圈更精簡、可讀性更高，並提供篩選、排序和群組功能。 如需詳細資訊，請參閱 [LINQ to Objects (C#)](../../csharp/programming-guide/concepts/linq/linq-to-objects.md) 和 [LINQ to Objects (Visual Basic)](../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md)。  
  
 PLINQ 提供 LINQ to Objects 的平行實作，這項實作透過更有效率地使用多核心電腦，在許多情況下會提供更快的查詢執行速度。 如需詳細資訊，請參閱 [Parallel LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Collections>
- <xref:System.Collections.Specialized>
- <xref:System.Collections.Generic>
- [安全執行緒集合](../../../docs/standard/collections/thread-safe/index.md)
