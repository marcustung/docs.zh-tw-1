---
title: 1004 - WorkflowInstanceAborted
ms.date: 03/30/2017
ms.assetid: edb9ab8c-0b9a-488d-aa96-9c8c7984b53c
ms.openlocfilehash: d34f6f1ab6af8e06a0f28fb043faf9fe16a8b211
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57485183"
---
# <a name="1004---workflowinstanceaborted"></a>1004 - WorkflowInstanceAborted

## <a name="properties"></a>屬性

|||
|-|-|
|ID|1004|
|關鍵字|WFRuntime|
|層級|資訊|
|通道|Microsoft-Windows-Application Server-Applications/Debug|

## <a name="description"></a>描述

表示工作流程執行個體已中止的例外狀況。

## <a name="message"></a>訊息

WorkflowInstance Id：'%1' 已中止，並發生例外狀況。

## <a name="details"></a>詳細資料

|資料項目名稱|資料項目型別|描述|
|--------------------|--------------------|-----------------|
|WorkflowInstanceId|`xs:string`|工作流程的執行個體 ID。|
|例外狀況|`xs:string`|例外狀況的例外狀況詳細資料|
|AppDomain|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 傳回的字串。|
