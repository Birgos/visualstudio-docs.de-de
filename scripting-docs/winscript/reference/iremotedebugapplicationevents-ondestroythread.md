---
title: IRemoteDebugApplicationEvents::OnDestroyThread | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationEvents.OnDestroyThread
apilocation:
- jscript.dll
helpviewer_keywords:
- IRemoteDebugApplicationEvents::OnDestroyThread
ms.assetid: 7c716ccc-7b82-41b2-9a16-d0366999dee8
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 53e07b7f90068dac5b39b1dedfd2bb91d65540f2
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086477"
---
# <a name="iremotedebugapplicationeventsondestroythread"></a>IRemoteDebugApplicationEvents::OnDestroyThread
Behandelt ein Ereignis Thread zerstört.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT OnDestroyThread(  
   IRemoteDebugApplicationThread*  prdat  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `prdat`  
 [in] Der Thread, der zerstört wurde.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Methode gibt ein `HRESULT` zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode behandelt das Ereignis Thread zerstört.  
  
## <a name="see-also"></a>Siehe auch  
 [IRemoteDebugApplicationEvents-Schnittstelle](../../winscript/reference/iremotedebugapplicationevents-interface.md)