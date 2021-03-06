---
title: IDebugApplicationThread110::GetActiveThreadRequestCount | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThread110::GetActiveThreadRequestCount
ms.assetid: 025d2072-1d7f-4448-8aa3-38a014313570
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8bd776aedd4df61797419795afb8dcc8afeb9318
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348188"
---
# <a name="idebugapplicationthread110getactivethreadrequestcount"></a>IDebugApplicationThread110::GetActiveThreadRequestCount
Gibt die Anzahl der Threadanforderungen aus der PDM Threadwechsel Mechanismen, die gerade verarbeitet werden zurück. Diese Nummer ist in der Regel 0 oder 1. Jedoch die Zahl kann höher sein, wenn ein Thread-Aufruf startet die Verarbeitung jedoch einen synchronen Aufruf Out-of-Thread startet oder andernfalls den Thread hält und eingehende Aufrufe an die erneut verarbeitet werden kann (z. B. durch Auslösen einer [ IRemoteDebugApplicationEvents-Schnittstelle](../../winscript/reference/iremotedebugapplicationevents-interface.md) -Ereignis, das für den Debuggerthread ausgestellt wird).  
  
> [!IMPORTANT]
>  [IDebugApplicationThread110-Schnittstelle](../../winscript/reference/idebugapplicationthread110-interface.md) wird implementiert von PDM V11. 0 und höher. Gefunden in activdbg100.h.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT GetActiveThreadRequestCount([out, annotation("_Out_")] UINT * puiThreadRequests);  
```  
  
#### <a name="parameters"></a>Parameter  
 `puiThreadRequests`  
 [out] Die Anzahl der Threadanforderungen.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugApplicationThread110-Schnittstelle](../../winscript/reference/idebugapplicationthread110-interface.md)