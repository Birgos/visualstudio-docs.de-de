---
title: EXE-Datei | Microsoft-Dokumentation
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
- .dll files
- Exe symbol
- .exe files
- executable files, Exe symbol
ms.assetid: a781d2cf-55fe-4373-9cf1-b732864244e0
caps.latest.revision: 20
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 52015c5086f3f637568ed3ecc5a8c7c974ae10fa
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51778475"
---
# <a name="exe"></a>Exe
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

EXE-Datei ist die einzige symbol ohne eine lexikalische oder übergeordneten-Klasse, weil er den globalen Bereich der .exe oder .dll-Datei darstellt. Es ist nur ein Symbol mit dem `SymTagExe` Tag pro Datei. Die [idiasession:: Get_globalscope](../../debugger/debug-interface-access/idiasession-get-globalscope.md) Methode gibt das Symbol zurück.  
  
## <a name="properties"></a>Eigenschaften  
 Die folgende Tabelle zeigt die Eigenschaften, die für diesen Symboltyp gültig sind.  
  
|Eigenschaft|Datentyp|Beschreibung|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_age](../../debugger/debug-interface-access/idiasymbol-get-age.md)|`DWORD`|Alter dieser ausführbaren Datei.|  
|[IDiaSymbol::get_guid](../../debugger/debug-interface-access/idiasymbol-get-guid.md)|`GUID`|`GUID` dieser ausführbaren Datei.|  
|[IDiaSymbol::get_isCTypes](../../debugger/debug-interface-access/idiasymbol-get-isctypes.md)|`BOOL`|`TRUE` Wenn die Symboldatei zugeordnet enthält diese ausführbare Datei C-Typen (nur in DIA-SDK-Version 8.0 oder höher).|  
|[IDiaSymbol::get_isStripped](../../debugger/debug-interface-access/idiasymbol-get-isstripped.md)|`BOOL`|`TRUE` Wenn private Symbole aus der Symboldatei, die diese ausführbare Datei (nur in DIA-SDK-Version 8.0 oder höher) zugeordneten entfernt haben.|  
|[IDiaSymbol::get_machineType](../../debugger/debug-interface-access/idiasymbol-get-machinetype.md)|`DWORD`|Wert, der angibt, der Ziel-CPU (eines der [CV_CPU_TYPE_e-Enumeration](../../debugger/debug-interface-access/cv-cpu-type-e.md) Werte).|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol-get-name.md)|`BSTR`|Der Name der .exe-Datei.|  
|[IDiaSymbol::get_signature](../../debugger/debug-interface-access/idiasymbol-get-signature.md)|`DWORD`|Die Signatur der ausführbaren Datei.|  
|[IDiaSymbol::get_symbolsFileName](../../debugger/debug-interface-access/idiasymbol-get-symbolsfilename.md)|`BSTR`|Vollständiger Pfad der .exe-Datei PDB oder DBG-Datei.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|Index-ID des Symbols.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|Gibt `SymTagExe` (eines der [SymTagEnum-Enumeration](../../debugger/debug-interface-access/symtagenum.md) Werte).|  
  
## <a name="see-also"></a>Siehe auch  
 [Idiasession:: Get_globalscope](../../debugger/debug-interface-access/idiasession-get-globalscope.md)   
 [Lexikalische Hierarchie der Symboltypen](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)



