---
title: IDebugProgram2::CauseBreak | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::CauseBreak
helpviewer_keywords:
- IDebugProgram2::CauseBreak
ms.assetid: 07d353fc-68ab-4297-a18f-3d3c7a80e121
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1f7dbad02632663474f62f561773aa62a8735071
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2019
ms.locfileid: "55069381"
---
# <a name="idebugprogram2causebreak"></a>IDebugProgram2::CauseBreak
Fordert an, dass das Programm die Ausführung der nächsten beenden Zeitpunkt eins seiner Threads Versuche ausgeführt.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT CauseBreak(   
   void   
);  
```  
  
```csharp  
int CauseBreak();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Ein [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) Ereignis wird immer dann gesendet, wenn Sie als Nächstes versucht das Programm, um Code auszuführen, nachdem diese Methode aufgerufen wird.  
  
 Diese Methode ist asynchron, darin, dass die Methode sofort zurückgegeben, ohne dass unbedingt zum Beenden des Programms.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)