---
title: Common Language Runtime 中的 ETW 事件
ms.date: 03/30/2017
helpviewer_keywords:
- CLR ETW events
- ETW, common language runtime
- ETW, CLR events
ms.assetid: 5bb9b6a2-7b57-4aea-8809-32b28bc73e88
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1d059a5d4df402b309f628bf3e9393114c4cdeec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59191389"
---
# <a name="etw-events-in-the-common-language-runtime"></a>Common Language Runtime 中的 ETW 事件
Common language runtime (CLR) 透過各式各樣的偵錯和分析事件，提供有用的 Windows 事件追蹤 (ETW) 診斷資訊。 CLR ETW 事件會運用 Windows ETW 追蹤系統，來增強 Common Language Runtime 提供的現有分析和偵錯支援。  
  
 您可以在 MSDN 上的[使用 ETW 改善偵錯和效能調整](https://go.microsoft.com/fwlink/?LinkID=161142)一文中取得 ETW 的詳細資訊。 您可以在 NTDebugging 部落格的 [Windows 效能工具組 - Xperf](https://go.microsoft.com/fwlink/?LinkID=161144) 一文中找到 Xperf 的相關資訊。  
  
 這些事件主題中所描述的所有事件都需要 [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] (含) 以後版本。 Windows Vista 作業系統是支援的最低需求用戶端，而 Windows Server 2008 是支援的最低需求伺服器。  
  
## <a name="in-this-section"></a>本節內容  
 [控制 .NET Framework 記錄](../../../docs/framework/performance/controlling-logging.md)  
 描述擷取及檢視 ETW 事件的工具與命令。  
  
 [CLR ETW 提供者](../../../docs/framework/performance/clr-etw-providers.md)  
 提供執行階段和取消提供者的相關資訊，以及您如何使用它們處理 ETW 資料收集。  
  
 [CLR ETW 關鍵字和層級](../../../docs/framework/performance/clr-etw-keywords-and-levels.md)  
 說明可依分類啟用事件篩選的執行階段和取消提供者的關鍵字。  
  
 [CLR ETW 事件](../../../docs/framework/performance/clr-etw-events.md)  
 提供 CLR ETW 事件、其關鍵字、層級和事件資料的詳細資訊。  
  
## <a name="see-also"></a>另請參閱

- [.NET Framework 中的 ETW 事件](../../../docs/framework/performance/etw-events.md)
