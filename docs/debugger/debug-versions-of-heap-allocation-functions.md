---
title: Debugversionen von Heapreservierungsfunktionen | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.crt
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- _CRTDBG_MAP_ALLOC macro
- debugging [CRT], heap allocation functions
- debugging memory leaks, CRT debug library functions
- malloc function
- memory leaks, CRT debug library functions
- heap allocation, debug
- _malloc_dbg function
ms.assetid: 91748bdc-f4cd-4d8b-ab98-0493dab7ed0d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bf3865d8369b7b3b4a7407f8c54465f93bcc7bd7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54920877"
---
# <a name="debug-versions-of-heap-allocation-functions"></a>Debugversionen von Heapreservierungsfunktionen
Die C-Laufzeitbibliothek umfasst spezielle Debugversionen der Heapreservierungsfunktionen. Diese Funktionen haben dieselben Namen wie die Releaseversionen, gefolgt vom Suffix _dbg. In diesem Thema werden die Unterschiede zwischen der Releaseversion und der _dbg-Version einer CRT-Funktion beschrieben, wobei `malloc` und `_malloc_dbg` als Beispiele verwendet werden.  
  
 Wenn [_DEBUG](/cpp/c-runtime-library/debug) wird definiert, ordnet das CRT alle [Malloc](/cpp/c-runtime-library/reference/malloc) Aufrufe von [_malloc_dbg](/cpp/c-runtime-library/reference/malloc-dbg). Aus diesem Grund müssen Sie den Code nicht umschreiben, indem Sie `_malloc_dbg` durch `malloc` ersetzen, um die Vorteile beim Debuggen nutzen zu können.  
  
 Unter Umständen möchten Sie `_malloc_dbg` jedoch explizit aufrufen. Der explizite Aufruf von `_malloc_dbg` bietet zusätzliche Vorteile:  
  
- Nachverfolgen von `_CLIENT_BLOCK`-Reservierungen.  
  
- Speichern von Quelldatei und Zeilennummer an der Stelle, an der die Reservierung angefordert wurde.  
  
  Wenn Sie nicht konvertieren möchten Ihre `malloc` Aufrufe von `_malloc_dbg`, Sie können die Informationen zur Quelldatei abrufen, indem Sie definieren [_CRTDBG_MAP_ALLOC](/cpp/c-runtime-library/crtdbg-map-alloc), der bewirkt, dass der Präprozessor direkt Zuordnung alle Aufrufe von `malloc` zu `_malloc_dbg` statt auf einen Wrapper um `malloc`.  
  
  Um Reservierungstypen in Clientblöcken gesondert nachzuverfolgen, muss `_malloc_dbg` direkt aufgerufen und der `blockType`-Parameter auf `_CLIENT_BLOCK` festgelegt werden.  
  
  Wenn _DEBUG nicht definiert ist, Aufrufe von `malloc` nicht gestört werden, werden Aufrufe von `_malloc_dbg` werden aufgelöst, um `malloc`, die Definition der [_CRTDBG_MAP_ALLOC](/cpp/c-runtime-library/crtdbg-map-alloc) wird ignoriert, und bezieht sich auf Dateiinformationen Quelle der Anforderung wurde nicht angegeben. Da `malloc` keinen Blocktypparameter hat, werden `_CLIENT_BLOCK`-Anforderungen wie Standardreservierungen behandelt.  
  
## <a name="see-also"></a>Siehe auch  
 [CRT-Debugverfahren](../debugger/crt-debugging-techniques.md)