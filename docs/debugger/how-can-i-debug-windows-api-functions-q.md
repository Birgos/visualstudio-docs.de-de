---
title: Debuggen von Windows-API-Funktionen | Microsoft-Dokumentation
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.api
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], Windows API functions
- NT symbols and debugging Windows API functions
- Windows API functions, debugging
- Windows API, debugging API functions
- APIs, debugging
ms.assetid: 7c126f57-62ab-4d94-9805-632d696ba1f0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b177ec2664014fa547908aa18e19f605a83a8282
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54931881"
---
# <a name="how-can-i-debug-windows-api-functions"></a>Wie können Funktionen der Windows-API gedebuggt werden?
Wenn Sie eine Windows API-Funktion debuggen möchten, in der NT-Symbole geladen sind, müssen Sie wie im Folgenden beschrieben vorgehen.  
  
### <a name="to-set-a-breakpoint-on-a-windows-api-function-with-nt-symbols-loaded"></a>So legen Sie einen Haltepunkt für eine Windows API-Funktion mit NT-Symbolen fest  
  
-   Geben Sie den Namen der Funktion und den Namen der DLL ein, in der sich die Funktion befindet. Verwenden Sie im 32-Bit-Code die ergänzte Form des Funktionsnamens. Zum Festlegen eines Breakpoints für **MessageBeep** müssen Sie z. B. Folgendes eingeben:  
  
    ```cpp
    {,,USER32.DLL}_MessageBeep@4  
    ```  
  
     Zum Abrufen des ergänzten Namens finden Sie unter [Anzeigen von ergänzten Namen](https://msdn.microsoft.com/library/f79e2717-a4db-4d12-a689-69830cce2be0).  
  
## <a name="see-also"></a>Siehe auch  
 [Debugging Native Code FAQs (Häufig gestellte Fragen zum Debuggen von nativem Code)](../debugger/debugging-native-code-faqs.md)   
 [Debuggen von nativem Code](../debugger/debugging-native-code.md)
