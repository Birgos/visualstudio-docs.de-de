---
title: IDebugBreakpointUnboundEvent2 | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBreakpointUnboundEvent2
helpviewer_keywords:
- IDebugBreakpointUnboundEvent2
ms.assetid: 6b1e1863-0c64-4d85-8ab9-aface522fdea
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 14a16080424ae19e909751a797a49192a22e645d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54947863"
---
# <a name="idebugbreakpointunboundevent2"></a>IDebugBreakpointUnboundEvent2
Diese Schnittstelle weist den sitzungsbasierter Debug-Manager (SDM), ein gebundener Haltepunkt eine geladene Anwendung aufgehoben wurde.  
  
## <a name="syntax"></a>Syntax  
  
```  
IDebugBreakpointUnboundEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Hinweise für Implementierer  
 Die Debug-Engine (DE) implementiert diese Schnittstelle als Teil der Unterstützung für Haltepunkte an. Die [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) Schnittstelle muss auf dasselbe Objekt wie diese Schnittstelle implementiert werden (wird verwendet, das SDM [QueryInterface](/cpp/atl/queryinterface) für den Zugriff auf die `IDebugEvent2` Schnittstelle).  
  
## <a name="notes-for-callers"></a>Hinweise für Aufrufer  
 Die DE erstellt und sendet dieses Ereignisobjekt, wenn für ein gebundener Haltepunkt aufgehoben wurde. Das Ereignis gesendet wird, mithilfe der [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) Callback-Funktion, die durch die SDM angegeben wird, wenn diese an die zu debuggende Programm wird angefügt.  
  
## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge  
 Die folgende Tabelle zeigt die Methoden der `IDebugBreakpointUnboundEvent2`.  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md)|Ruft ab, die nicht gebundene Haltepunkt.|  
|[GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md)|Ruft den Grund ab, die, den der Haltepunkt aufgehoben wurde.|  
  
## <a name="remarks"></a>Hinweise  
 Bei eine Debug-Engine-DLL oder Klasse entladen wird, muss alle Breakpoints, die an Code in diesem Modul gebunden wurden die zu debuggende Programm wird aufgehoben. Ein `IDebugBreakpointUnboundEvent2` wird für jeden nicht gebundenen Haltepunkt gesendet.  
  
## <a name="requirements"></a>Anforderungen  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugBoundBreakpoint2](../../../extensibility/debugger/reference/idebugboundbreakpoint2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)