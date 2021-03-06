---
title: IApplicationDebugger::onDebuggerEvent | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IApplicationDebugger.onDebuggerEvent
apilocation:
- scrobj.dll
helpviewer_keywords:
- IApplicationDebugger::onDebuggerEvent
ms.assetid: 82a5faaa-1222-4bf1-8569-10439dbdf16d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7dec2cea6cfcf11cc756ef730f98feee9ed9bb0e
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54092676"
---
# <a name="iapplicationdebuggerondebuggerevent"></a>IApplicationDebugger::onDebuggerEvent
Behandelt ein Ereignis für die benutzerdefinierte Anwendung.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT onDebuggerEvent(  
   REFIID     riid,  
   IUnknown*  punk  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `riid`  
 [in] Der Schnittstellenbezeichner für das Objekt.  
  
 `punk`  
 [in] Das Ereignisobjekt, die die Schnittstelle, die durch definiert implementiert `riid`.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Methode gibt ein `HRESULT` zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
|`E_NOTIMPL`|Die Methode wird derzeit nicht implementiert.|  
  
## <a name="remarks"></a>Hinweise  
 Die Semantik der `IUnknown` ist eine vollständig Anwendung/Debugger definiert.  
  
 Diese Methode ermöglicht für benutzerdefinierte Erweiterungen des Modells Debugger; Es ist derzeit nicht implementiert.  
  
 Diese Methode wird aufgerufen, wenn `IDebugApplication::FireDebuggerEvent` aufgerufen wird.  
  
## <a name="see-also"></a>Siehe auch  
 [IApplicationDebugger-Schnittstelle](../../winscript/reference/iapplicationdebugger-interface.md)   
 [IDebugApplication::FireDebuggerEvent](../../winscript/reference/idebugapplication-firedebuggerevent.md)