---
title: IDebugPendingBreakpoint2::Bind | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPendingBreakpoint2::Bind
helpviewer_keywords:
- Bind method
- IDebugPendingBreakpoint2::Bind method
ms.assetid: 46e3f307-219d-40cd-a929-d41399c60ecf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ea73240d6797daaee2cb51796800282bf5b60008
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54933762"
---
# <a name="idebugpendingbreakpoint2bind"></a>IDebugPendingBreakpoint2::Bind
Wird dieser ausstehenden Haltepunkt an einem oder mehreren Code-Speicherorten gebunden.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT Bind(   
   void   
);  
```  
  
```csharp  
int Bind();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben. Gibt `E_BP_DELETED` , wenn der Haltepunkt gelöscht wurde.  
  
## <a name="remarks"></a>Hinweise  
 Wenn diese Methode aufgerufen wird, sollten eine Debug-Engine (DE) versuchen, diese ausstehenden Haltepunkt auf alle Speicherorte von Code zu binden, die mit übereinstimmen.  
  
 Nach der Rückgabe dieser Methode benötigt der Aufrufer Ereignisse, die angibt, dass der ausstehenden Haltepunkt gebunden wurde oder fehlerhaft. bevor die Annahme getroffen ist, die Aufrufe zu warten, bis die [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md) oder [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)-Methoden aller Haltepunkte gebunden oder Fehler, bzw. Listet.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [IDebugBreakpointBoundEvent2](../../../extensibility/debugger/reference/idebugbreakpointboundevent2.md)   
 [IDebugBreakpointErrorEvent2](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md)   
 [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)   
 [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)