---
title: IDebugPendingBreakpoint2::SetCondition | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPendingBreakpoint2::SetCondition
helpviewer_keywords:
- SetCondition method
- IDebugPendingBreakpoint2::SetCondition method
ms.assetid: 0534224f-654f-4862-bc4d-a9a81a5f8899
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: df52c80b38a715f56df002720c002e66db112523
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54937560"
---
# <a name="idebugpendingbreakpoint2setcondition"></a>IDebugPendingBreakpoint2::SetCondition
Legt fest oder ändert die Bedingung, die dem ausstehenden Haltepunkt zugeordnet.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT SetCondition(   
   BP_CONDITION bpCondition  
);  
```  
  
```csharp  
int SetCondition(   
   BP_CONDITION bpCondition  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `bpCondition`  
 [in] Ein [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) Struktur, die die Bedingung festlegen angibt.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Jede Bedingung, die zuvor mit dem ausstehenden Haltepunkt verknüpft war, geht verloren. Alle Breakpoints, die von dieser ausstehenden Haltepunkt gebunden werden aufgerufen, um ihre Bedingung auf die im angegebenen Wert festlegen die `bpCondition` Parameter.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)