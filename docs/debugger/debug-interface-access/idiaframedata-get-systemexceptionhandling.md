---
title: 'Idiaframedata:: Get_systemexceptionhandling | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_systemExceptionHandling method
ms.assetid: e8df1972-913c-446c-9779-775575b0caa9
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cf18ed2bb25ab2632c471c0da7d19ea54239c70d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939939"
---
# <a name="idiaframedatagetsystemexceptionhandling"></a>IDiaFrameData::get_systemExceptionHandling
Ruft ein Flag, das angibt, ob die Behandlung von Ausnahmen aktiviert ist.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT get_systemExceptionHandling (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 pRetVal  
 [out] Gibt `TRUE` ist Behandlung von Ausnahmen in Kraft ist, andernfalls gibt `FALSE`.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt bei Erfolg `S_OK` zurück. Gibt `S_FALSE` Wenn diese Eigenschaft nicht unterstützt wird. Andernfalls wird ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Behandlung von Ausnahmen wird häufiger als strukturierte Ausnahmebehandlung bezeichnet.  
  
 Um zu bestimmen, wenn die C++-Ausnahmebehandlung gültig ist, rufen Sie die [idiaframedata:: Get_cplusplusexceptionhandling](../../debugger/debug-interface-access/idiaframedata-get-cplusplusexceptionhandling.md) Methode.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)   
 [IDiaFrameData::get_cplusplusExceptionHandling](../../debugger/debug-interface-access/idiaframedata-get-cplusplusexceptionhandling.md)