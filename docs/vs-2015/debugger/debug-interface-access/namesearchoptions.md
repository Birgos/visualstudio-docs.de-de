---
title: NameSearchOptions | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- NameSearchOptions enumeration
ms.assetid: 67dfbede-2678-47df-b664-5c49841d0b9b
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 17896f1a32ab939a7f2ee5a2ebd863136ea5aaa1
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51771339"
---
# <a name="namesearchoptions"></a>NameSearchOptions
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Gibt die Suchoptionen für Symbol und den Dateinamen an.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
enum NameSearchOptions {   
   nsNone,  
   nsfCaseSensitive     = 0x1,  
   nsfCaseInsensitive   = 0x2,  
   nsfFNameExt          = 0x4,  
   nsfRegularExpression = 0x8,  
   nsfUndecoratedName   = 0x10,  
  
// For backward compatibility:  
   nsCaseSensitive           = nsfCaseSensitive,  
   nsCaseInsensitive         = nsfCaseInsensitive,  
   nsFNameExt                = nsfCaseInsensitive | nsfFNameExt,  
   nsRegularExpression       = nsfRegularExpression | nsfCaseSensitive,  
   nsCaseInRegularExpression = nsfRegularExpression | nsfCaseInsensitive  
};  
```  
  
## <a name="elements"></a>Elements  
 `nsNone`  
 Es wurden keine Optionen angegeben.  
  
 `nsfCaseSensitive`  
 Wendet eine namensübereinstimmung der Groß-/Kleinschreibung an.  
  
 `nsfCaseInsensitive`  
 Wendet eine namensübereinstimmung der Groß-/Kleinschreibung an.  
  
 `nsfFNameExt`  
 Namen behandelt, als Pfade und eine namensübereinstimmung filename.ext gilt.  
  
 `nsfRegularExpression`  
 Wendet die Groß-/Kleinschreibung namensübereinstimmung mithilfe von Sternchen (*) und Fragezeichen (?) als Platzhalter.  
  
 `nsfUndecoratedName`  
 Gilt nur für Symbole, die nicht ergänzten Form und ergänzte Namen haben.  
  
## <a name="remarks"></a>Hinweise  
 Die Werte aus dieser Enumeration werden für die folgenden Methoden übergeben:  
  
-   [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)  
  
-   [IDiaSession::findFile](../../debugger/debug-interface-access/idiasession-findfile.md)  
  
-   [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)  
  
## <a name="requirements"></a>Anforderungen  
 Header: dia2.h  
  
## <a name="see-also"></a>Siehe auch  
 [Enumerationen und Strukturen](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasession:: Findchildren](../../debugger/debug-interface-access/idiasession-findchildren.md)   
 [Idiasession:: FindFile](../../debugger/debug-interface-access/idiasession-findfile.md)   
 [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)



