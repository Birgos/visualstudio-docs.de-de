---
title: IScriptNode::Delete | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.Delete
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::Delete
ms.assetid: 6765ff80-a9a8-40a3-a669-7fcc284c87af
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: cce802cc1a6d63001cfbed020592b30a9d8dab1b
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094795"
---
# <a name="iscriptnodedelete"></a>IScriptNode::Delete
Löscht die Struktur dieses Objekts.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT Delete();  
```  
  
#### <a name="parameters"></a>Parameter  
 Die Methode nimmt keine Parameter.  
  
## <a name="return-value"></a>Rückgabewert  
 Eine `HRESULT`. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
  
## <a name="remarks"></a>Hinweise  
 Nach der `Delete` -Methode aufgerufen wird, die [IScriptNode::Alive](../../winscript/reference/iscriptnode-alive.md) -Methode herausstellt, Skriptknoten ist nicht aktiv.  
  
## <a name="see-also"></a>Siehe auch  
 [IScriptNode-Schnittstelle](../../winscript/reference/iscriptnode-interface.md)