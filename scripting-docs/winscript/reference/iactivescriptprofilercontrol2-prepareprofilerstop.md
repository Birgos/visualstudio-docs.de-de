---
title: IActiveScriptProfilerControl2::PrepareProfilerStop | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerControl2::PrepareProfilerStop
ms.assetid: e43a63bc-c44f-44a8-9db4-29062b9e6a16
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 086ec8b4a126c65162638afde4d8081269757e1c
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54089517"
---
# <a name="iactivescriptprofilercontrol2prepareprofilerstop"></a>IActiveScriptProfilerControl2::PrepareProfilerStop
Benachrichtigt den Profiler an, dass Sie beabsichtigen, die profilerstellung für alle anwendbaren Skript-Engines zu beenden. Mithilfe dieser Methode können Sie die vollständige Aufrufliste abrufen, wenn [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] ausgeführt wird, wenn Sie die profilerstellung beenden.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT PrepareProfilerStop();  
```  
  
#### <a name="parameters"></a>Parameter  
 Die Methode ist keine Parameter annimmt.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt ein HRESULT zurück. Folgende Werte sind möglich:  
  
|Rückgabewert|Bedeutung|  
|------------------|-------------|  
|`S_OK`|Die Methode war erfolgreich.|  
|`E_FAIL`|Die profilerstellung konnte nicht gestartet werden.|  
|`S_FALSE`|Die profilerstellung wurde beendet, wenn ein Skript nicht ausgeführt wurde.|  
|`ACTIVPROF_E_PROFILER_ABSENT`|Die profilerstellung ist nicht aktiviert.|  
  
## <a name="remarks"></a>Hinweise  
 Aufrufen von `IActiveScriptProfilerControl2::PrepareProfilerStop` wird sichergestellt, dass Ereignisse für Funktionen in der Aufrufliste gesendet werden. Diese Methode muss aufgerufen werden, bevor Sie die profilerstellung für alle Skript-Engine, die auf der aktuellen Registerkarte beenden. Die Methode kann für alle Skript-Engine aufgerufen werden.  
  
## <a name="see-also"></a>Siehe auch  
 [IActiveScriptProfilerControl2::CompleteProfilerStart](../../winscript/reference/iactivescriptprofilercontrol2-completeprofilerstart.md)   
 [IActiveScriptProfilerControl2-Schnittstelle](../../winscript/reference/iactivescriptprofilercontrol2-interface.md)