---
title: 'Idiaframedata:: Execute | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::execute method
ms.assetid: 7a6c7d03-1ff1-4059-bd54-5f407eeebc26
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6be6c631f9ea0db47829f305f90bd1c296de2f28
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/02/2019
ms.locfileid: "53958740"
---
# <a name="idiaframedataexecute"></a>IDiaFrameData::execute
Führt die stapelentladung und gibt Ergebnisse in eine Stackwalk-Frame-Schnittstelle zurück.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT execute (   
   IDiaStackWalkFrame* frame  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `frame`  
 [in] Ein [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md) -Objekt, das den Zustand der Frame-Register enthält.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben. Die folgende Tabelle zeigt die möglichen Rückgabewerte für diese Methode.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|E_DIA_INPROLOG|Einen Stapelrahmen im Prolog Code kann nicht ausgeführt werden.|  
|E_DIA_SYNTAX|Analysieren Sie Fehler im Frame-Programm.|  
|E_DIA_FRAME_ACCESS|Kann nicht den Zugriff registriert oder Arbeitsspeicher.|  
|E_DIA_VALUE|Fehler bei der Berechnung eines Werts (z. B. Division durch 0 (null)).|  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode wird aufgerufen, während des Debuggens, um den Stapel zu entladen. Die [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md) Objekt wird von der Clientanwendung zum Empfangen von Updates für die Register und Bereitstellen von verwendete Methoden implementiert die `execute` Methode.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)   
 [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md)