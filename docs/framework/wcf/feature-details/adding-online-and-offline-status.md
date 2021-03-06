---
title: 加入上線與離線狀態
ms.date: 03/30/2017
ms.assetid: 05e5f51d-81b6-4c17-b364-9dda447a5fce
ms.openlocfilehash: 15a963d4de0dcf1d7f0162b0a3266e17d4073ecd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59147689"
---
# <a name="adding-online-and-offline-status"></a>加入上線與離線狀態
在許多情況下，應用程式監視對等通道連線狀態的特定詳細資訊是很重要的工作。 您可以在 `GetProperty` 介面實作上呼叫 <xref:System.ServiceModel.IOnlineStatus> 方法，以取得此項資訊。 含有此介面實作的物件可以監視連線狀態或註冊事件處理常式 (例如 `OnOnline` 和 `OnOffline`)，並且在發生上線狀態變更時立即做出反應。  
  
 在對等通道基礎結構中，用戶端在已連接至少一個的對等用戶端時會被視為上線，否則為離線。 對於偵錯開發中之應用程式或是向終端使用者顯示詳細資訊，這項功能特別有用。  
  
> [!NOTE]
>  上線事件處理常式在傳送任何訊息之前，應先確認節點是否已開啟。  
  
## <a name="see-also"></a>另請參閱

- [建置對等通道應用程式](../../../../docs/framework/wcf/feature-details/building-a-peer-channel-application.md)
