---
title: IDebugEnumField | Microsoft-Dokumentation
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
- IDebugEnumField
helpviewer_keywords:
- IDebugEnumField interface
ms.assetid: 42f685bf-0f39-47f4-98b0-6022efe2bf97
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6af5d77cd9aa622edafd144c885322768d3e4376
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51740596"
---
# <a name="idebugenumfield"></a>IDebugEnumField
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Diese Schnittstelle stellt einen Enumerationstyp dar.  
  
## <a name="syntax"></a>Syntax  
  
```  
IDebugEnumField : IDebugContainerField  
```  
  
## <a name="notes-for-implementers"></a>Hinweise für Implementierer  
 Ein symbolanbieter implementiert diese Schnittstelle, um eine Enumeration darstellt.  
  
## <a name="notes-for-callers"></a>Hinweise für Aufrufer  
 Verwendung [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) dieser Schnittstelle vom Abrufen der [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) Schnittstelle, wenn [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) gibt `FIELD_TYPE_ENUM`.  
  
## <a name="methods-in-vtable-order"></a>Methoden in VTable-Reihenfolge  
 Zusätzlich zu den Methoden für die `IDebugField` und `IDebugContainerField` Schnittstellen, die diese Schnittstelle implementiert die folgenden Methoden:  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[GetUnderlyingSymbol](../../../extensibility/debugger/reference/idebugenumfield-getunderlyingsymbol.md)|Gibt eine [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) , das die den Namen für den Enumerationstyp.|  
|[GetStringFromValue](../../../extensibility/debugger/reference/idebugenumfield-getstringfromvalue.md)|Gibt den Namen der Enumerationskonstante, die den angegebenen Wert zugeordnet.|  
|[GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)|Gibt den Wert mit den Namen der angegebenen Enumeration-Konstante|  
|[GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)|Gibt den Wert mit dem angegebene Enumeration-constant-Namen, aber Groß-/Kleinschreibung ignorieren.|  
  
## <a name="remarks"></a>Hinweise  
 Es ist das zugrunde liegende Symbol, das tatsächlich an einen Speicherort mit gebunden wird [binden](../../../extensibility/debugger/reference/idebugbinder-bind.md).  
  
## <a name="requirements"></a>Anforderungen  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Siehe auch  
 [Symbolanbieterschnittstellen](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md)

