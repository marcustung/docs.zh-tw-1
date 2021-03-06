---
title: .NET 中的管道作業
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- pipes [.NET Framework]
- pipe operations [.NET Framework]
- interprocess communication [.NET Framework], pipes
- I/O [.NET Framework], pipes
ms.assetid: 7b964ebd-7a4f-4d28-8194-7841f9e4c702
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ba3690b6642601fd7d777e3ae1d1e34684e3b1dd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "58823554"
---
# <a name="pipe-operations-in-net"></a>.NET 中的管道作業
管道會提供一種處理序間通訊的方法。 管道有兩種類型：  
  
-   匿名管道。  
  
     匿名管道會在本機電腦上提供處理序間通訊。 相較於具名管道，匿名管道需要的額外負荷更少，但提供的服務有限。 匿名管道是單向的，而且無法透過網路使用。 它們僅支援單一伺服器執行個體。 匿名管道可用於執行緒之間的通訊，或父處理序和子處理序之間的通訊，其中管道控制代碼可以在建立通訊時，輕鬆地傳遞給子處理序。  
  
     在 .NET 中，您可以使用 <xref:System.IO.Pipes.AnonymousPipeServerStream> 和 <xref:System.IO.Pipes.AnonymousPipeClientStream> 類別實作匿名管道。  
  
     請參閱[如何：使用匿名管道進行本機處理序間通訊](../../../docs/standard/io/how-to-use-anonymous-pipes-for-local-interprocess-communication.md)。  
  
-   具名管道。  
  
     具名管道可在管道伺服器及一個或多個管道用戶端之間提供處理序間通訊。 具名管道可以是單向或雙向的。 它們支援訊息式通訊，且允許多個用戶端使用相同的管道名稱，同時連線到伺服器處理序。 具名管道也支援模擬，讓連線處理序在遠端伺服器上使用自己的權限。  
  
     在 .NET 中，您可以使用 <xref:System.IO.Pipes.NamedPipeServerStream> 和 <xref:System.IO.Pipes.NamedPipeClientStream> 類別實作匿名管道。  
  
     請參閱[如何：使用具名管道進行網路處理序間通訊](../../../docs/standard/io/how-to-use-named-pipes-for-network-interprocess-communication.md)。  
  
## <a name="see-also"></a>另請參閱

- [檔案和資料流 I/O](../../../docs/standard/io/index.md)
- [如何：使用匿名管道進行本機處理序間通訊](../../../docs/standard/io/how-to-use-anonymous-pipes-for-local-interprocess-communication.md)
- [如何：使用具名管道進行網路處理序間通訊](../../../docs/standard/io/how-to-use-named-pipes-for-network-interprocess-communication.md)
