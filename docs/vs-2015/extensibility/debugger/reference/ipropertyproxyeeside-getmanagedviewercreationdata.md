---
title: IPropertyProxyEESide::GetManagedViewerCreationData | Microsoft-Dokumentation
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
- IPropertyProxyEESide::GetManagedViewerCreationData
helpviewer_keywords:
- IPropertyProxyEESide::GetManagedViewerCreationData
ms.assetid: c4eb4d60-8816-4d52-bc8d-dffd4f066499
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 570407afc4e06a1456f5e97e06814a44344aaa94
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51756581"
---
# <a name="ipropertyproxyeesidegetmanagedviewercreationdata"></a>IPropertyProxyEESide::GetManagedViewerCreationData
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ruft Informationen zu den Viewer für diesen Eigenschaftentyp um Instanziieren dieser Viewer ab.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
HRESULT GetManagedViewerCreationData(  
   BSTR*                  assemName,  
   IEEDataStorage**       assemBytes,  
   IEEDataStorage**       assemPdb,  
   BSTR*                  className,  
   ASSEMBLYLOCRESOLUTION* alr,  
   BOOL*                  replacementOk  
);  
```  
  
```csharp  
int GetManagedViewerCreationData(  
   out string                     assemName,  
   out IEEDataStorage             assemBytes,  
   out IEEDataStorage             assemPdb,  
   out string                     className,  
   out enum_ASSEMBLYLOCRESOLUTION alr,  
   out int                        replacementOk  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `assemName`  
 [out] Gibt den Namen der Assembly, die dieses Objekt enthält.  
  
 `assemBytes`  
 [out] Gibt eine [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) -Objekt, das die Assemblybytes dieses Objekts (Dies ist ein null-Wert, wenn keine Bytes verfügbar sind) enthält.  
  
 `assemPdb`  
 [out] Gibt eine `IEEDataStorage` Objektspeicher, die Symbol enthält Informationen für dieses Objekt (Dies ist ein null-Wert, wenn kein Symbolspeicher verfügbar ist).  
  
 `className`  
 [out] Gibt den Namen der Klasse, die dieses Objekt zurück.  
  
 `alr`  
 [out] Gibt einen Wert aus der [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md) Enumeration, die den Speicherort der Assembly angibt.  
  
 `replacementOk`  
 [out] Ungleich NULL zurückgibt (`TRUE`), wenn der Wert des Objekts geändert werden kann; NULL (`FALSE`), wenn das Objekt schreibgeschützt ist.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode wird vom Typ-Schnellansichten verwendet, um einen verwalteten Viewer zu instanziieren.  
  
## <a name="see-also"></a>Siehe auch  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)

