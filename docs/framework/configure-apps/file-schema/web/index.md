---
title: Web 設定結構描述
ms.date: 03/30/2017
helpviewer_keywords:
- Web.config configuration file [ASP.NET]
- ASP.NET configuration system, Web settings schema
- schema Web settings
- Web settings, schema [ASP.NET]
- configuration files [ASP.NET]
- configuration schema [.NET Framework], Web settings
ms.assetid: ae1ac356-267d-4753-8d7a-7a04eb45a9be
ms.openlocfilehash: 1f0241b65c915dd5703ceea97dd5b07f88832003
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59113057"
---
# <a name="web-settings-schema"></a>Web 設定結構描述
Web 設定會指定 CPU 和執行層級 ASP.NET 設定，這些設定將套用至 ASP.NET 裝載層管理的整個處理序行為。 這些設定不同於 ASP.NET 應用程式之 Web.config 檔中所指定的應用程式定義域類型設定。  
  
 Web 設定包含在 Aspnet.config 檔中，此檔案位於 .NET Framework 各版本的安裝資料夾中。 例如，[!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] 的 Aspnet.config 檔位於下列資料夾：  
  
 `C:\Windows\Microsoft.NET\Framework\v2.0.50727\`  
  
 Web 設定會在於任何其他組態檔中使用，例如 machine.config 檔、根目錄 Web.config 或應用程式層級 Web.config 檔。  
  
 [\<configuration> 項目](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [\<system.web> 項目 (Web 設定)](../../../../../docs/framework/configure-apps/file-schema/web/system-web-element-web-settings.md)  
  
 [\<applicationPool> 項目 (Web 設定)](../../../../../docs/framework/configure-apps/file-schema/web/applicationpool-element-web-settings.md)  
  
|項目|描述|  
|-------------|-----------------|  
|[\<system.web>](../../../../../docs/framework/configure-apps/file-schema/web/system-web-element-web-settings.md)|包含 ASP.NET 裝載層使用的資訊。|  
|[\<applicationPool>](../../../../../docs/framework/configure-apps/file-schema/web/applicationpool-element-web-settings.md)|指定 CPU 和執行層級 ASP.NET 設定，這些設定將套用至 ASP.NET 裝載層管理的整個處理序行為。|  
  
## <a name="see-also"></a>另請參閱

- [組態檔結構描述](../../../../../docs/framework/configure-apps/file-schema/index.md)
