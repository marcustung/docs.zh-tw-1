---
title: <customCookieHandler>
ms.date: 03/30/2017
ms.assetid: a03b153d-5ec6-4915-9031-6f0c3fd348be
author: BrucePerlerMS
ms.openlocfilehash: 0129c63fe17b63889a77ea1a56c0d7e657def859
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59223972"
---
# <a name="customcookiehandler"></a>\<customCookieHandler>
設定自訂 cookie 處理常式型別。 這個項目只會出現如果`mode`屬性的`<cookieHandler>`項目是 「 自訂 」。 自訂型別必須衍生自<xref:System.IdentityModel.Services.CookieHandler>類別。  
  
 \<system.identityModel.services>  
\<federationConfiguration>  
\<cookieHandler>  
\<customCookieHandler>  
  
## <a name="syntax"></a>語法  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Custom">  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" >  
      </customCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|類型|指定自訂型別衍生自<xref:System.IdentityModel.Services.CookieHandler>類別。 如需有關如何指定`type`屬性，請參閱[自訂型別參考](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)。|  
  
### <a name="child-elements"></a>子元素  
 None  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<cookieHandler>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|會設定<xref:System.IdentityModel.Services.CookieHandler>，<xref:System.IdentityModel.Services.SessionAuthenticationModule>用以讀取和寫入 cookie。|  
  
## <a name="remarks"></a>備註  
 當您設定以指定自訂 cookie 處理常式`mode`的屬性`<cookieHandler>`項目為"Custom"，您必須指定自訂 cookie 處理常式的類型包括`<customCookieHandler>`子項目會參考的 cookie 處理常式類型。 此元素不能指定何時`mode`屬性設為"Chunked"或"Default"。 自訂 cookie 處理常式必須衍生自<xref:System.IdentityModel.Services.CookieHandler>類別。  
  
 `<customCookieHandler>`項目由<xref:System.IdentityModel.Configuration.CustomTypeElement>類別。  
  
## <a name="example"></a>範例  
 下列範例會設定使用自訂的 cookie 處理常式類型的 SAM `MyNamespace.MyCustomCookieHandler`。  
  
```xml  
<cookieHandler mode="Custom">  
    <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
</cookieHandler>  
```  
  
## <a name="see-also"></a>另請參閱

- <xref:System.IdentityModel.Services.CookieHandler>
