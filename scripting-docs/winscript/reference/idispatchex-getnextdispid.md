---
title: IDispatchEx::GetNextDispID | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.GetNextDispID
apilocation:
- scrobj.dll
helpviewer_keywords:
- GetNextDispID method
ms.assetid: 8263d441-85ee-47f4-bdba-fbf2ad07e85f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 24aa5ad2b780d5ff61efcde4d24b6700bb5b353e
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "54092988"
---
# <a name="idispatchexgetnextdispid"></a>IDispatchEx::GetNextDispID
Listet die Member des Objekts.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT GetNextDispID(  
   DWORD grfdex,  
   DISPID id,  
   DISPID *pid  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `grfdex`  
 Bestimmt, welche Gruppe von Elementen sind, aufgelistet werden sollen. Dies kann eine Kombination der folgenden Werte sein:  
  
|Wert|Bedeutung|  
|-----------|-------------|  
|fdexEnumDefault|Fordert an, dass das Objekt die Standardelemente zählt. Das Objekt kann einen beliebigen Satz von Elementen aufzählen.|  
|fdexEnumAll|Fordert an, dass das Objekt alle Elemente zählt. Das Objekt kann einen beliebigen Satz von Elementen aufzählen.|  
  
 `id`  
 Gibt das aktuelle Element. GetNextDispID Ruft das Element in der Enumeration nach dieser ab. Verwendet GetDispID oder einem vorherigen Aufruf von GetNextDispID, um diesen Bezeichner abzurufen. Wird mit den DISPID_STARTENUM-Wert des ersten Elements den ersten Bezeichner abgerufen.  
  
 `pid`  
 Adresse des einen DISPID-Variable, die den Bezeichner des nächsten Elements in der Enumeration empfängt.  
  
 Wenn ein Element, indem gelöscht wird `DeleteMemberByName` oder `DeleteMemberByDispID`, `DISPID` gültig bleiben muss `GetNextDispID`.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt einen der folgenden Werte zurück:  
  
|||  
|-|-|  
|`S_OK`|Erfolgreich.|  
|`S_FALSE`|Enumeration erfolgt.|  
  
## <a name="example"></a>Beispiel  
  
```cpp
HRESULT hr;  
   BSTR bstrName;  
   DISPID dispid;  
   IDispatchEx *pdex;  
  
   // Assign to pdex  
   hr = pdex->GetNextDispID(fdexEnumAll, DISPID_STARTENUM, &dispid);  
   while (hr == NOERROR)  
   {  
      hr = pdex->GetMemberName(dispid, &bstrName);  
      if (!wcscmp(bstrName, OLESTR("Bar")))  
      {  
         SysFreeString(bstrName);  
         return TRUE;  
      }  
      SysFreeString(bstrName);  
      hr = pdex->GetNextDispID(fdexEnumAll, dispid, &dispid);  
   }  
```  
  
## <a name="see-also"></a>Siehe auch  
 [IDispatchEx-Schnittstelle](../../winscript/reference/idispatchex-interface.md)   
 [IDispatchEx::GetDispID](../../winscript/reference/idispatchex-getdispid.md)   
 [IDispatchEx::GetNextDispID](#lrfidispatchexgetnextdispid)   
 [IDispatchEx::DeleteMemberByName](../../winscript/reference/idispatchex-deletememberbyname.md)   
 [IDispatchEx::DeleteMemberByDispID](../../winscript/reference/idispatchex-deletememberbydispid.md)