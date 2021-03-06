---
title: IActiveScript::GetScriptSite | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetScriptSite
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetScriptSite
ms.assetid: 83a2a89d-93d0-4cbd-9244-91a730cb406b
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 85b7d94ccb9e2589b10bf705721fc289df9638a9
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094158"
---
# <a name="iactivescriptgetscriptsite"></a>IActiveScript::GetScriptSite
Ruft das zugeordnete Windows-Skript-Engine-Objekt ab.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT GetScriptSite(  
    REFIID iid,           // interface identifier  
    void **ppvSiteObject  // address of host site interface  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `iid`  
 [in] Der Bezeichner der angeforderten Schnittstelle.  
  
 `ppvSiteObject`  
 [out] Die Adresse des Speicherorts, die den Schnittstellenzeiger auf den Host Site-Objekt empfängt.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt einen der folgenden Werte zurück:  
  
|Rückgabewert|Bedeutung|  
|------------------|-------------|  
|`S_OK`|Erfolgreich.|  
|`E_INVALIDARG`|Ein Argument war ungültig.|  
|`E_NOINTERFACE`|Die angegebene Schnittstelle wird nicht unterstützt.|  
|`E_POINTER`|Es wurde ein ungültiger Zeiger angegeben.|  
|`S_FALSE`|Keine Website wurde festgelegt wurde; die `ppvSiteObject` Parametersatz zu `NULL`.|  
  
## <a name="see-also"></a>Siehe auch  
 [IActiveScript](../../winscript/reference/iactivescript.md)