---
title: BREAKREASON-Enumeration | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- BREAKREASON
apilocation:
- scrobj.dll
helpviewer_keywords:
- BREAKREASON enumeration
ms.assetid: bde07ede-2f9b-4fa2-affc-f9405683f5f7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d5c0dc03d8d24014e28ecf9510fa3d5faa21dba2
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096797"
---
# <a name="breakreason-enumeration"></a>BREAKREASON-Enumeration
Gibt an, was die Unterbrechung verursacht hat.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
typedef enum tagBREAKREASON {  
   BREAKREASON_STEP,  
   BREAKREASON_BREAKPOINT,  
   BREAKREASON_DEBUGGER_BLOCK,  
   BREAKREASON_HOST_INITIATED,  
   BREAKREASON_LANGUAGE_INITIATED,  
   BREAKREASON_DEBUGGER_HALT,  
   BREAKREASON_ERROR,  
   BREAKREASON_JIT  
} BREAKREASON;  
```  
  
## <a name="members"></a>Member  
  
|Member|Beschreibung|  
|------------|-----------------|  
|BREAKREASON_STEP|Die Sprach-Engine befindet sich im schrittweisen Modus.|  
|BREAKREASON_BREAKPOINT|Die Sprach-Engine hat keinen expliziten Haltepunkt festgestellt.|  
|BREAKREASON_DEBUGGER_BLOCK|Die Sprach-Engine hat einen Debugger-Block in einem anderen Thread festgestellt.|  
|BREAKREASON_HOST_INITIATED|Der Host hat eine Unterbrechung angefordert.|  
|BREAKREASON_LANGUAGE_INITIATED|Die Sprach-Engine hat eine Unterbrechung angefordert.|  
|BREAKREASON_DEBUGGER_HALT|Der Debugger-IDE hat eine Unterbrechung angefordert.|  
|BREAKREASON_ERROR|Ein Ausnahmefehler verursacht die Unterbrechung an.|  
|BREAKREASON_JIT|Es wird darauf zurückzuführen, dass JIT-Debuggen starten.|  
  
## <a name="see-also"></a>Siehe auch  
 [Konstanten, Enumerationen und Strukturen für Active Script-Debugger](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)