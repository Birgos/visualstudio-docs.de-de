---
title: 'Idiasourcefile:: Get_uniqueid | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_uniqueId method
ms.assetid: e0b8dbc0-6061-4f31-bead-2cd72be44e41
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4399c6f3c1bc5168f4a7bce0a82e251051432033
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54964417"
---
# <a name="idiasourcefilegetuniqueid"></a>IDiaSourceFile::get_uniqueId
Ruft einen Wert des Schlüssels einfachen ganzen Zahl, der eindeutig für dieses Image ist.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT get_uniqueId (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pRetVal`  
 [out] Gibt einen Wert des Schlüssels einfachen ganzen Zahl, der eindeutig für dieses Image ist.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Vergleichen von Schlüsseln, anstatt Zeichenfolgen Line Number Verarbeitung beschleunigt werden können.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)