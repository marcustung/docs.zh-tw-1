---
title: ICorDebugGenericValue 介面
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue
helpviewer_keywords:
- ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: bc14f408-b359-4c8c-ade2-888ccdf7261b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ad2209c6e28c7749bd149902e5b696955ee7f13f
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/28/2019
ms.locfileid: "56981981"
---
# <a name="icordebuggenericvalue-interface"></a>ICorDebugGenericValue 介面

「 ICorDebugValue"，套用至所有值的子類別。 這個介面提供值的 Get 和 Set 方法。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[GetValue 方法](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-getvalue-method.md)|將值複製到指定的緩衝區。|  
|[SetValue 方法](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-setvalue-method.md)|複製指定的緩衝區中的新值。|  
  
## <a name="remarks"></a>備註  
 `ICorDebugGenericValue` 因為它是非可遠端處理，則是子介面。  
  
 若是參考類型，值會是參考，而不是參考的內容。  
  
 這個介面不支援跨電腦或跨處理序的遠端呼叫。  
  
> [!NOTE]
>  這個介面不支援跨電腦或跨處理序的遠端呼叫。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorDebug.idl、 CorDebug.h  
  
 **程式庫：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱

- [偵錯介面](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
