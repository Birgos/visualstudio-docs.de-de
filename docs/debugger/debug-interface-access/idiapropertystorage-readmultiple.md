---
title: IDiaPropertyStorage::ReadMultiple | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadMultiple
ms.assetid: 6ccc9397-ce41-4f72-b261-72ac252cd4a5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f3c507df19fad7dd9594aeca1a53b9cb89a2e936
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55035562"
---
# <a name="idiapropertystoragereadmultiple"></a>IDiaPropertyStorage::ReadMultiple
Liest die angegebenen Eigenschaften aus der aktuellen Gruppe der Eigenschaft.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT ReadMultiple(   
   ULONG          cpspec,  
   PROPSPEC const rgpspec,  
   PROPVARIANT    rgvar  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `cpspec`  
 [in] Die Anzahl der in der angegebenen Eigenschaften der `rgpspec` Array. Falls der Wert NULL ist, wird die Methode gibt keine Eigenschaften zurück, aber gibt zurück, `S_OK` als einen Erfolgscode.  
  
 `rgpspec`  
 [in] Ein Array von Eigenschaften, die gelesen werden. Eigenschaften können entweder durch eine Eigenschafts-ID oder durch eine optionale Zeichenfolgenname angegeben werden. Es ist nicht erforderlich, um Eigenschaften in einer bestimmten Reihenfolge im Array anzugeben. Das Array kann doppelte Eigenschaften, was zu doppelten Eigenschaftswerten bei der Rückgabe für einfache Eigenschaften enthalten. Nicht-Simple-Eigenschaften sollten Zurückgeben der Zugriff verweigert beim Versuch, die sie ein zweites Mal zu öffnen. Das Array kann eine Mischung von Eigenschaft-IDs und Zeichenfolgen-IDs enthalten. Dieses Array benötigen mindestens `cpspec` Anzahl von Eigenschaftswerten.  
  
 `rgvar`  
 [in, out] Ein Array von `PROPVARIANT` Strukturen (im Namespace Microsoft.VisualStudio.OLE.Interop) mit Werten für jede Eigenschaft gefüllt werden soll. Das Array muss mindestens `cpspec` Elemente in der Größe. Der Aufrufer muss es sich nicht um die Werte im Array zu initialisieren.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt bei Erfolg `S_OK` zurück. Gibt `S_FALSE` Wenn mindestens eine der Eigenschaften wurde nicht gefunden. Andernfalls wird ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Wenn eine Eigenschaft wurde nicht gefunden, den zugehörigen Eintrag in der `rgvar` Array enthält einen `VARIANT` mit dem Typ des `VT_EMPTY`.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)