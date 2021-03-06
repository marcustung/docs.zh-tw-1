---
title: 如何：選擇不自動升級檔案對話方塊
ms.date: 03/30/2017
helpviewer_keywords:
- OpenFileDialog [Windows Forms], opt out of automatic upgrade
- file dialog box [Windows Forms], opt out of automatic upgrade
- Windows Vista file dialog box [Windows Forms], opt out of automatic upgrade
- SaveFileDialog [Windows Forms], opt out of automatic upgrade
- AutoUpgradeEnabled property
ms.assetid: 522e482e-cc01-48b1-8d59-9617dc2c4ac1
ms.openlocfilehash: a4be35617e8be1c6c83ac6f2d06e03b6cbb2977f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59769407"
---
# <a name="how-to-opt-out-of-file-dialog-box-automatic-upgrade"></a>如何：選擇不自動升級檔案對話方塊
當<xref:System.Windows.Forms.OpenFileDialog>和<xref:System.Windows.Forms.SaveFileDialog>類別用在應用程式，其外觀和行為取決於 Windows 執行應用程式的版本。 所建立的應用程式時[!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)]或先前會顯示在[!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)]，<xref:System.Windows.Forms.OpenFileDialog>並<xref:System.Windows.Forms.SaveFileDialog>會自動顯示具有[!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)]外觀和行為。 從開始[!INCLUDE[net_v30_short](../../../../includes/net-v30-short-md.md)]，您可以選擇不自動升級，以顯示<xref:System.Windows.Forms.OpenFileDialog>並<xref:System.Windows.Forms.SaveFileDialog>使用[!INCLUDE[winxp](../../../../includes/winxp-md.md)]-樣式外觀和行為。  
  
### <a name="to-opt-out-of-file-dialog-box-automatic-upgrade"></a>選擇不自動升級檔案對話方塊  
  
1. 設定<xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A>的屬性<xref:System.Windows.Forms.OpenFileDialog>或是<xref:System.Windows.Forms.SaveFileDialog>到`false`顯示對話方塊之前。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Windows.Forms.FileDialog>
