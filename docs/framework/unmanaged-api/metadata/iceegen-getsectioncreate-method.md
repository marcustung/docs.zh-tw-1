---
title: ICeeGen::GetSectionCreate 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9768dfd43b6b60df1660c48cb6d6f498b049e256
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59103307"
---
# <a name="iceegengetsectioncreate-method"></a>ICeeGen::GetSectionCreate 方法
產生並取得使用指定的名稱和旗標值的程式碼區段。  
  
 這個方法已經過時，不應使用。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
## <a name="parameters"></a>參數  
 `name`  
 [in]指定要建立的區段名稱的字串指標。  
  
 `flags`  
 [in]指定選項的旗標。  
  
 `section`  
 [out]新建立的程式碼區段指標。  
  
## <a name="remarks"></a>備註  
 呼叫`GetSectionCreate`只有當您有未處理的其他方法的特殊區段需求。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** Cor.h  
  
 **LIBRARY:** 做為 MsCorEE.dll 中的資源  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱

- [ICeeGen 介面](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
