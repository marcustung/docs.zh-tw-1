---
ms.openlocfilehash: 3cd5052dffcb059c240a310e0b89384f28409264
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234397"
---
### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>在具有觸控功能的系統上呼叫 System.Windows.Input.PenContext.Disable 可能會擲回 ArgumentException

|   |   |
|---|---|
|詳細資料|在某些情況下，在具有觸控功能的系統上呼叫內部 <strong>System.Windows.Intput.PenContext.Disable</strong> 方法，可能會擲回由於重新進入而未處理的 <code>T:System.ArgumentException</code>。|
|建議|.NET Framework 4.7 中已解決這個問題。 若要避免這個例外狀況，請升級至從 .NET Framework 4.7 開始的 .NET Framework 版本。|
|範圍|Edge|
|版本|4.6.1|
|類型|正在重定目標|
