---
title: 'Idiasymbol:: Get_constructor | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_constructor method
ms.assetid: 2f2cf1e0-f817-4ca0-b782-3341362c46a9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 81a684ac12a277036e5392cd3a76b4e55eee634f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54928533"
---
# <a name="idiasymbolgetconstructor"></a>IDiaSymbol::get_constructor
Ruft ein Flag, das angibt, ob der benutzerdefinierte Datentyp einen Konstruktor oder Destruktor hat.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT get_constructor (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pRetVal`  
 [out] Gibt `TRUE` der benutzerdefinierten Datentyp besitzt einen Konstruktor oder Destruktor; andernfalls gibt `FALSE`.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.  
  
> [!NOTE]
>  Der Rückgabewert `S_FALSE` bedeutet, dass die Eigenschaft nicht für das Symbol verfügbar ist.  
  
## <a name="requirements"></a>Anforderungen  
  
|Anforderung|Beschreibung|  
|-----------------|-----------------|  
|Header:|Dia2.h|  
|Version:|DIA-SDK V7. 0|  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)