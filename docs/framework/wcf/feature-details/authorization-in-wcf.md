---
title: WCF 的授權
ms.date: 03/30/2017
helpviewer_keywords:
- authorization [WCF]
- security [WCF], authorization
ms.assetid: 8ea0b552-af65-45b0-a157-c6c111b8ce5e
ms.openlocfilehash: 26aa445f3136fcb16e2eb9cdce6b245476297dfd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59161355"
---
# <a name="authorization-in-wcf"></a>WCF 的授權
授權是控制資源 (例如服務或檔案) 存取與權限的程序。 在本節中的主題會示範如何在 Windows Communication Foundation (WCF) 的各種不同的方式執行此基本工作。  
  
## <a name="in-this-section"></a>本節內容  
 [存取控制機制](../../../../docs/framework/wcf/feature-details/access-control-mechanisms.md)  
 提供 WCF，並且建議的使用的驗證機制的簡介。  
  
 [如何：以 PrincipalPermissionAttribute 類別限制存取](../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)  
 示範限制存取具有 <xref:System.Security.Permissions.PrincipalPermissionAttribute>之服務的程序。  
  
 [如何：使用 ASP.NET 角色提供者搭配服務](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)  
 逐步執行服務的組態設定，讓它能使用 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]的角色提供者功能。  
  
 [如何：使用 ASP.NET 授權管理員角色提供者搭配服務](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md)  
 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 可以使用授權管理員管理網站的授權。 同樣地可以利用 WCF [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]/Authorization 管理員的組合進行授權的用戶端。  
  
 [使用身分識別模型來管理宣告與授權](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)  
 解釋對宣告型授權使用「識別模型」基礎結構的基本概念。  
  
 [委派和模擬](../../../../docs/framework/wcf/feature-details/delegation-and-impersonation-with-wcf.md)  
 解釋委派與模擬之間的差異。  
  
## <a name="reference"></a>參考資料  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.ServiceModel.Description.PrincipalPermissionMode>  
  
 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>  
  
 <xref:System.Security.Permissions.PrincipalPermissionAttribute>  
  
## <a name="related-sections"></a>相關章節  
 [驗證](../../../../docs/framework/wcf/feature-details/authentication-in-wcf.md)  
  
## <a name="see-also"></a>另請參閱

- [安全性概觀](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [Windows Server App Fabric 的安全性模型](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
