---
title: IBindEventHandler::BindHandler | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IBindEventHandler.BindHandler
apilocation:
- scrobj.dll
helpviewer_keywords:
- IBindEventHandler::BindHandler
ms.assetid: 87909828-2224-4bb1-a6c9-dfe715ac4c9b
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62ac6de8342f0a436d984f4194351507fdcd5edd
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090713"
---
# <a name="ibindeventhandlerbindhandler"></a>IBindEventHandler::BindHandler
Wird ein Ereignis auf ein Objekt gebunden.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT BindHandler(  
   LPCOLESTR   pstrEvent,  
   IDispatch*  pdisp  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pstrEvent`  
 [in] Gibt das Ereignis behandelt.  
  
 `pdisp`  
 [in] Gibt das Objekt zur Behandlung des Ereignisses.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Methode gibt ein `HRESULT` zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode wird ein Ereignis auf ein Objekt gebunden.  
  
## <a name="see-also"></a>Siehe auch  
 [IBindEventHandler-Schnittstelle](../../winscript/reference/ibindeventhandler-interface.md)