---
title: <state> 的 <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ab483c7f-a091-4933-ba6b-708d96846d38
ms.openlocfilehash: ff75895949c50cd369e4297ea77dc21106994067
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59073932"
---
# <a name="state-of-states"></a>\<狀態 > 的\<狀態 >
組態項目，其中包含應該發出追蹤記錄之已訂閱活動的狀態。  
  
 如需有關追蹤設定檔查詢的詳細資訊，請參閱 <<c0> [ 追蹤設定檔](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)。  
  
\<system.serviceModel>  
\<tracking>  
\<trackingProfile>  
\<workflow>  
\<activityStateQueries>  
\<activityStateQuery>  
\<states>  
\<state>  
  
## <a name="syntax"></a>語法  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <states>
          <state name="String" />
        </states>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|名稱|可指定追蹤記錄應發出之已訂閱活動狀態的字串。|  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states-of-activitystatequery.md)|組態元素的集合，其中包含應該發出追蹤記錄之已訂閱活動的狀態。|  
  
## <a name="remarks"></a>備註  
 ActivityStateQuery 的一項獨特功能，就是可在追蹤工作流程的執行時擷取資料。 它可在存取追蹤記錄後期執行時，提供額外的內容。 您可以使用[\<引數 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)， [\<狀態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)並[\<狀態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)項目擷取任何變數或引數從工作流程中的任何活動。 下列範例示範活動狀態查詢，此查詢會在發出活動的 `Closed` 追蹤記錄時擷取變數及引數。 變數和引數只能使用 ActivityStateRecord 擷取，並因此訂閱在追蹤設定檔中使用[ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)。  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a>另請參閱

- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [工作流程追蹤及追蹤](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [追蹤設定檔](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
