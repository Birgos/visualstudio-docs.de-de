---
title: IEnumDebugModules2::Reset | Microsoft-Dokumentation
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
- IEnumDebugModules2::Reset
helpviewer_keywords:
- IEnumDebugModules2::Reset
ms.assetid: f6ff364c-2644-4919-b950-3cb82eb6f601
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bc8ce2c93ef0e24025c5c87320bc38ab081ea438
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51760237"
---
# <a name="ienumdebugmodules2reset"></a>IEnumDebugModules2::Reset
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Setzt die Enumeration auf das erste Element zurück.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
HRESULT Reset(  
   void  
);  
```  
  
```csharp  
int Reset();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Nachdem diese Methode aufgerufen wird, wird beim nächsten Aufruf von der [Weiter](../../../extensibility/debugger/reference/ienumdebugmodules2-next.md) Methode gibt das erste Element der Enumeration.  
  
## <a name="see-also"></a>Siehe auch  
 [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)

