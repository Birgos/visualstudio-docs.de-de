---
title: IDebugProcess3::Continue | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugProcess3::Continue
helpviewer_keywords:
- IDebugProcess3::Continue
ms.assetid: 57506242-5763-4c08-adb9-8a78ce02cebb
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ae71aa79aba54b8954e309131f4b5e82357e1555
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51817112"
---
# <a name="idebugprocess3continue"></a>IDebugProcess3::Continue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Wird fortgesetzt, das Ausführen dieses Prozesses vom Status "beendet". Alle vorherigen Ausführungsstatus (z. B. in einem Schritt) wird beibehalten, und der Vorgang beginnt, erneut ausführen.  
  
> [!NOTE]
>  Diese Methode sollte verwendet werden, anstelle von [Weiter](../../../extensibility/debugger/reference/idebugprogram2-continue.md).  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT Continue(  
   IDebugThread2* pThread  
);  
```  
  
```csharp  
int Continue(  
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pThread`  
 [in] Ein [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) Objekt, das den Thread fortgesetzt werden darstellt.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt den Fehlercode zurück.  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode wird aufgerufen, zu diesem Vorgang unabhängig davon, wie viele Prozesse gedebuggt werden oder welcher Prozess das Stopping-Ereignis generiert. Die Implementierung muss behalten den vorherigen Ausführungsstatus (z. B. in einem Schritt) und die Ausführung wird fortgesetzt, als wären es nie vor dem Abschluss der vorherigen Ausführung beendet haben. Das heißt, wenn ein Thread, in diesen Prozess wurde einen Schritt-für-Vorgang durchführen und wurde beendet, weil ein anderer Prozess beendet, und klicken Sie dann `Continue` war aufgerufen wird, den angegebenen Thread muss den ursprünglichen Prozedurschritten-Vorgang abzuschließen.  
  
 **Warnung** senden Sie eine Beenden-Ereignis oder ein sofort (synchron) Ereignis [Ereignis](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) bei der Verarbeitung dieser Aufruf ist; andernfalls der Debugger wird, reagiert.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)

