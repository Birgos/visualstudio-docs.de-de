---
title: Haltepunkte (Visual Studio SDK) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- breakpoints
ms.assetid: acfcabed-9f2f-436c-ad18-7ca2f45d631b
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4223f694c55025c0fc3e4d0afe8fca530940520b
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51764749"
---
# <a name="breakpoints-visual-studio-sdk"></a>Haltepunkte (Visual Studio SDK)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Es gibt drei Arten von Haltepunkten: Ausstehend "," gebunden und Fehler.  
  
 **Ein ausstehender Haltepunkt:**  
  
- Ist eine Abstraktion, die alle einen Haltepunkt für eine oder mehrere Codekontexte in einem oder mehreren Programmen binden erforderlichen Informationen enthält. Jedes Mal überprüft Ursachencode zum Laden eines Programms, gedebuggt werden, die Debug-Engine alle ausstehenden Haltepunkte, um festzustellen, ob sie gebunden werden können.  
  
   Ein ausstehender Haltepunkt selbst nie bindet an Code, aber stattdessen erfasst und alle gebundenen Breakpoints enthalten, die es generiert hat.  
  
- Wird durch dargestellt eine [IDebugPendingBreakpoint2](../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) Schnittstelle.  
  
  **Einen gebundenen Haltepunkt:**  
  
- Eine Abstraktion für einen Haltepunkt ist zugeordnet oder an einem einzigen Kontext gebunden. Jede gebundene Haltepunkt wird als Reaktion auf ein ausstehender Haltepunkt generiert. Ein ausstehender Haltepunkt kann jedoch mehr als einen gebundenen Haltepunkt generieren.  
  
   Wenn Code entladen wird, kann ein gebundener Haltepunkt aufgehoben und verworfen werden.  
  
- Wird durch dargestellt eine [IDebugBoundBreakpoint2](../../extensibility/debugger/reference/idebugboundbreakpoint2.md) Schnittstelle.  
  
  **Ein Haltepunkt Fehler:**  
  
- Ist eine Abstraktion zum Beschreiben eines Fehlers beim Versuch, einen ausstehenden Haltepunkt in einen Codekontext zu binden. Ein Haltepunkt auf Fehler wird entweder einen Fehler Standort oder an den Haltepunktausdruck selbst beschrieben. Weitere Informationen finden Sie unter [Binden von Haltepunkten](../../extensibility/debugger/binding-breakpoints.md).  
  
   Der haltepunktfehler kann entweder eine Fehler- oder eine Warnung sein.  
  
- Wird durch dargestellt eine [IDebugErrorBreakpoint2](../../extensibility/debugger/reference/idebugerrorbreakpoint2.md) Schnittstelle.  
  
## <a name="see-also"></a>Siehe auch  
 [Programme](../../extensibility/debugger/programs.md)   
 [Debuggerkonzepte](../../extensibility/debugger/debugger-concepts.md)   
 [Codekontext](../../extensibility/debugger/code-context.md)   
 [IDebugBoundBreakpoint2](../../extensibility/debugger/reference/idebugboundbreakpoint2.md)   
 [IDebugPendingBreakpoint2](../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [IDebugErrorBreakpoint2](../../extensibility/debugger/reference/idebugerrorbreakpoint2.md)

