---
title: 'Idialoadcallback:: Notifydebugdir | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyDebugDir method
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: baa1dbde2f4cbe9d537c181c73832f57b31b6041
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55043037"
---
# <a name="idialoadcallbacknotifydebugdir"></a>IDiaLoadCallback::NotifyDebugDir
Aufgerufen, wenn ein Debugverzeichnis in die .exe-Datei gefunden wurde.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT NotifyDebugDir (   
   BOOL  fExecutable,  
   DWORD cbData,  
   BYTE  data[]  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `fExecutable`  
 [in] `TRUE` Wenn das Debugverzeichnis aus einer ausführbaren Datei (statt eine DBG-Datei) gelesen wird.  
  
 `cbData`  
 [in] Die Anzahl der Bytes der Daten in der Debugverzeichnis.  
  
 `data[]`  
 [in] Ein Array, das mit das Debugverzeichnis gefüllt ist.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben. Der Rückgabecode wird in der Regel ignoriert.  
  
## <a name="remarks"></a>Hinweise  
 Die [idiadatasource:: Loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) Methode dieser Rückruf aufruft, wenn beim Verarbeiten der ausführbaren Datei ein Debugverzeichnis gefunden.  
  
 Diese Methode entfernt die Notwendigkeit für den Client für das reverse Engineering der ausführbaren Datei bzw. das Debug-Datei zur Unterstützung von Debuginformationen nicht in der PDB-Datei gefunden. Mit diesen Daten kann der Client erkennen, den Typ der Debuginformationen zur Verfügung und gibt an, ob es sich in die ausführbare Datei oder die DBG-Datei befindet.  
  
 Die meisten Clients werden dieser Rückruf nicht erforderlich, da die `IDiaDataSource::loadDataForExe` -Methode öffnet transparent sowohl PDB .dbg-Dateien und bei Bedarf, um Symbole zu verarbeiten.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)