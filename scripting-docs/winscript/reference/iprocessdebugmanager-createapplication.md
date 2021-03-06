---
title: 'Iprocessdebugmanager:: CreateApplication | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IProcessDebugManager.CreateApplication
apilocation:
- pdm.dll
helpviewer_keywords:
- IProcessDebugManager::CreateApplication
ms.assetid: d6b646f2-8af0-445c-ae7e-a9772042b3a1
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6f182dd92d181067f930f415ec9332df2658c3ad
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088633"
---
# <a name="iprocessdebugmanagercreateapplication"></a>IProcessDebugManager::CreateApplication
Erstellt ein neues Objekt der Debug-Anwendung für diese Anwendung an.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT CreateApplication(  
   IDebugApplication**  ppda  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `ppda`  
 [out] Die Debug-Application-Objekt für diese Anwendung.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Methode gibt ein `HRESULT` zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
  
## <a name="remarks"></a>Hinweise  
 Das von dieser Methode erstellte Objekt hat keinen Namen und wird nicht hinzugefügt, mit der Ausführung Liste der Anwendungen. Verwenden der `IProcessDebugManager::AddApplication` um die Anwendung debuggen, um die Liste der hinzuzufügen.  
  
## <a name="see-also"></a>Siehe auch  
 [IProcessDebugManager-Schnittstelle](../../winscript/reference/iprocessdebugmanager-interface.md)   
 [IProcessDebugManager::AddApplication](../../winscript/reference/iprocessdebugmanager-addapplication.md)