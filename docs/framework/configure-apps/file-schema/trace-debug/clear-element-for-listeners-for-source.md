---
title: <clear> 項目<listeners>的 <source>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/clear
helpviewer_keywords:
- <clear> element for <listeners> for <source>
- clear element for <listeners> for <source>
ms.assetid: 76796bb2-9c0b-4526-8135-8bf18b16d8d9
ms.openlocfilehash: 63d3bb272fcdbee2c59b0569c85f8183cdac8666
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59158349"
---
# <a name="clear-element-for-listeners-for-source"></a>\<清除 > 項目\<接聽程式 > 針對\<來源 >
清除追蹤來源的 `Listeners` 集合。  
  
 \<configuration>  
\<system.diagnostics>  
\<sources>  
\<source>  
\<listeners>  
\<clear>  
  
## <a name="syntax"></a>語法  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
 無。  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|`configuration`|通用語言執行平台和 .NET Framework 應用程式所使用之每個組態檔中的根項目。|  
|`system.diagnostics`|指定用於收集、儲存及路由傳送訊息的追蹤接聽項，以及設定追蹤參數的層級。|  
|`sources`|包含起始追蹤訊息的追蹤來源。|  
|`source`|指定起始追蹤訊息的追蹤來源。|  
|`listeners`|指定用於收集、 儲存及路由傳送訊息的接聽程式。|  
  
## <a name="remarks"></a>備註  
 `<clear>`項目會移除所有的接聽程式，從`Listeners`集合的追蹤來源，包括<xref:System.Diagnostics.DefaultTraceListener>。 您可以使用`<clear>`項目之前使用`<add>`確有沒有其他作用中接聽程式集合中的項目。  
  
## <a name="configuration-file"></a>組態檔  
 這個項目可以用於電腦組態檔 (Machine.config) 和應用程式組態檔。  
  
## <a name="example"></a>範例  
 下列範例示範如何使用`<clear>`項目之前使用`<add>`加入接聽程式的項目`console`並`textListener`來`Listeners`追蹤來源的集合`TraceSourceApp`。  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
       <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <clear/>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"   
        type="System.Diagnostics.TextWriterTraceListener"   
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- [追蹤和偵錯設定結構描述](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [追蹤接聽項](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
