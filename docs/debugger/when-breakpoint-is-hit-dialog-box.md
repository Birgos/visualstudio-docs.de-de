---
title: Haltepunkt ist bei Treffer Dialogfeld | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.whenbreakpointishit
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
- SQL
ms.assetid: 476e3d98-cf35-4338-b124-cd0f3010d854
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 53f27b400c96f6b4336339e8d1beeec0dd87277c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54944747"
---
# <a name="when-breakpoint-is-hit-dialog-box"></a>Dialogfeld "Beim Erreichen eines Haltepunktes"
In diesem Dialogfeld können Sie die Aktion anpassen, die beim Erreichen eines Haltepunkts ausgeführt wird.  
  
## <a name="uielement-list"></a>UIElement-Liste  
 **Meldung drucken**  
 Druckt eine Meldung mithilfe der DebuggerDisplay-Syntax. Weitere Informationen finden Sie unter [Verwenden des DebuggerDisplay-Attributs](../debugger/using-the-debuggerdisplay-attribute.md).  
  
 Dieses Textfeld unterstützt auch spezielle Schlüsselwörter (z. B. $ADDRESS), die alleine oder innerhalb der geschweiften Klammern eines DebuggerDisplay-Ausdrucks verwendet werden können. Die verfügbaren Schlüsselwörter werden im Dialogfeld aufgelistet.  
  
 **Ausführung fortsetzen**  
 Dieses Steuerelement ist nur aktiviert, wenn **Meldung drucken** ausgewählt ist. Durch Auswählen dieses Steuerelements können Sie einen Haltepunkt als Ablaufverfolgungspunkt verwenden, um die Programmausführung zu verfolgen, statt beim Erreichen des Haltepunkts zu unterbrechen.  
  
## <a name="see-also"></a>Siehe auch  
 [Verwenden von Haltepunkten](../debugger/using-breakpoints.md)   
 [Verwenden des DebuggerDisplay-Attributs](../debugger/using-the-debuggerdisplay-attribute.md)