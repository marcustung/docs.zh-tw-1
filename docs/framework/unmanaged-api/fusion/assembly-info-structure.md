---
title: ASSEMBLY_INFO 結構
ms.date: 03/30/2017
api_name:
- ASSEMBLY_INFO
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- ASSEMBLY_INFO
helpviewer_keywords:
- ASSEMBLY_INFO structure [.NET Framework fusion]
ms.assetid: b3cbb47c-457f-4083-8895-49562ca99ab8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bae19ec18c54eccc7aa54d2d3a006f36ba8ab762
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59110873"
---
# <a name="assemblyinfo-structure"></a>ASSEMBLY_INFO 結構
包含在全域組件快取中註冊組件的相關資訊。  
  
## <a name="syntax"></a>語法  
  
```  
typedef struct _ASSEMBLY_INFO {  
    ULONG           cbAssemblyInfo;  
    DWORD           dwAssemblyFlags;  
    ULARGE_INTEGER  uliAssemblySizeInKB;  
    LPWSTR          pszCurrentAssemblyPathBuf;  
    ULONG           cchBuf;  
} ASSEMBLY_INFO;  
```  
  
## <a name="members"></a>成員  
  
|成員|描述|  
|------------|-----------------|  
|`cbAssemblyInfo`|以位元組為單位的結構大小。 此欄位保留以供未來擴充。|  
|`dwAssemblyFlags`|旗標，表示安裝的組件的詳細資料。 支援下列值：<br /><br /> -ASSEMBLYINFO_FLAG_INSTALLED 」 值，指出已安裝的組件。 目前版本的.NET framework 一律設定`dwAssemblyFlags`為此值。<br />-ASSEMBLYINFO_FLAG_PAYLOADRESIDENT 」 值，指出組件是常駐承載。 目前的.NET framework 版本永遠不會設定`dwAssemblyFlags`為此值。|  
|`uliAssemblySizeInKB`|總大小，以 kb 為單位的組件包含的檔案。|  
|`pszCurrentAssemblyPathBuf`|資訊清單檔案會保留目前的路徑字串緩衝區的指標。 路徑必須以 null 字元結尾。|  
|`cchBuf`|的寬字元數目，包括 null 結束字元，`pszCurrentAssemblyPathBuf`包含。|  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** Fusion.h  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱

- [融合結構](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)
- [全域組件快取](../../../../docs/framework/app-domains/gac.md)
