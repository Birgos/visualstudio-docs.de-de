---
title: IActiveScriptErrorDebug110::GetExceptionThrownKind | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptErrorDebug110::QueryIsFirstChance
ms.assetid: ecc16e54-93e4-4322-ae13-afa7cd860032
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ce3a164f3ee4d81ca849db7c4745948ffe17d56e
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097187"
---
# <a name="iactivescripterrordebug110getexceptionthrownkind"></a>IActiveScriptErrorDebug110::GetExceptionThrownKind
Gibt einen Wert zurück, der die Art der ausgelösten Ausnahme angibt.  
  
> [!IMPORTANT]
>  [IActiveScriptErrorDebug110-Schnittstelle](../../winscript/reference/iactivescripterrordebug110-interface.md) wird von PDM-Version 11.0 und höher implementiert. Gefunden in activdbg100.h.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT GetExceptionThrownKind(  
   SCRIPT_ERROR_DEBUG_EXCEPTION_THROWN_KIND*  pExceptionKind  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pExceptionKind`  
 [out] Die Art der Ausnahme, die ausgelöst wird, (z. B. erste Chance "oder" nicht behandelte), dargestellt durch eine [SCRIPT_ERROR_DEBUG_EXCEPTION_THROWN_KIND-Enumeration](../../winscript/reference/script-error-debug-exception-thrown-kind-enumeration.md) Enumerationswert.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Methode gibt ein `HRESULT` zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
  
## <a name="see-also"></a>Siehe auch  
 [IActiveScriptErrorDebug110-Schnittstelle](../../winscript/reference/iactivescripterrordebug110-interface.md)