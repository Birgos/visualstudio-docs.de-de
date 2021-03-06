---
title: Ausführungssteuerung und Zustandsauswertung | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], execution control
- expression evaluation, control of execution
ms.assetid: 55adde38-1622-4b51-83cb-ce1b04c1ca7a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e71fb57a4890c29652473338391a0f7181d19ac0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55010414"
---
# <a name="execution-control-and-state-evaluation"></a>Ausführung und Auswertung
Debuggen einer Anwendung erfordert die Implementierung von Ausführung Steuerelement Features wie Funktionen schrittweise an Haltepunkten anhalten und Fortsetzen der Ausführung. Visual Studio-debugging Basen werden die Steuerung der Ausführung auf Ereignissen zwischen Debuggerkomponenten gesendet.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Programmsteuerung](../../extensibility/debugger/program-control.md)  
 Listet die folgenden Routinen, die auf Programmebene auftreten: Festlegen der nächsten Anweisung, Ausführung, schrittweise ausführen, Sie den Vorgang fortsetzen, Anhalten und fortsetzen.  
  
 [Auf Haltepunkte bezogene Methoden](../../extensibility/debugger/breakpoint-related-methods.md)  
 Definiert die Grenze und die ausstehenden Typen von Haltepunkten, die Visual Studio unterstützt.  
  
 [Auswertung der Aufrufliste](../../extensibility/debugger/call-stack-evaluation.md)  
 Beschreibt die Implementierung der Methoden, mit die der Stapelrahmen der Aufrufliste anzeigen, während des Unterbrechungsmodus können.  
  
 [Auswertung von Ausdrücken](../../extensibility/debugger/expression-evaluation-visual-studio-debugging-sdk.md)  
 Erläutert, wie die Debug-Engine (DE), Ausdruck Evaluation (EE) und Sitzung Debug-Manager sind beteiligt, bei der Analyse und Auswertung eines Ausdrucks in eines der Fenster der IDE.  
  
 [Steuerelementereignisse](../../extensibility/debugger/control-events.md)  
 Erläutert die verwendete Schnittstelle zum Senden von Ereignissen während der kontrollierten Ausführung des Programms an.