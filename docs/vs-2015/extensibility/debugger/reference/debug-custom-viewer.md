---
title: DEBUG_CUSTOM_VIEWER | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- DEBUG_CUSTOM_VIEWER
helpviewer_keywords:
- DEBUG_CUSTOM_VIEWER structure
ms.assetid: 8e0ef3f0-0107-48e8-a037-6e52b4c4ed9d
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ba682680989b405eeb6343cf3b8a53e66c82bbe6
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51761200"
---
# <a name="debugcustomviewer"></a>DEBUG_CUSTOM_VIEWER
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Eine Struktur, die einen benutzerdefinierten Viewer identifiziert, oder geben Sie die Schnellansicht.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
typedef struct tagDEBUG_CUSTOM_VIEWER {  
   DWORD dwID;  
   BSTR  bstrMenuName;  
   BSTR  bstrDescription;  
   GUID  guidLang;  
   GUID  guidVendor;  
   BSTR  bstrMetric;  
} DEBUG_CUSTOM_VIEWER;  
```  
  
```csharp  
public struct DEBUG_CUSTOM_VIEWER {  
   public uint   dwID;  
   public string bstrMenuName;  
   public string bstrDescription;  
   public Guid   guidLang;  
   public Guid   guidVendor;  
   public string bstrMetric;  
};  
```  
  
## <a name="members"></a>Member  
 dwID  
 Eine ID, mehrere Viewer oder Schnellansichten, die von einer Implementierung zu unterscheiden `GUID`.  
  
 bstrMenuName  
 Der Text, der im Dropdown-Menü angezeigt wird.  
  
 bstrDescription  
 Eine Beschreibung der benutzerdefinierten Viewer oder typschnellansicht (muss ein null-Wert sein, wenn nicht verwendet).  
  
 guidLang  
 Sprache für die ausdrucksauswertung bereitstellt.  
  
 guidVendor  
 Hersteller, der die ausdrucksauswertung bereitstellt.  
  
 bstrMetric  
 Metrik unter dem die benutzerdefinierten Viewer oder typschnellansicht `CLSID` wird gespeichert.  
  
## <a name="remarks"></a>Hinweise  
 Eine Liste dieser Struktur wird zurückgegeben, durch einen Aufruf der [GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md) Methode (und durch Erweiterung, die [GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md) Methode).  
  
## <a name="requirements"></a>Anforderungen  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Siehe auch  
 [Strukturen und Unions](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md)   
 [GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md)

