---
title: IDebugExpression-Schnittstelle | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugExpression interface
ms.assetid: 36c00ffb-7160-4c30-a2c9-c9d70c8213cd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9684253343aa83cf95f7d816781705eab7fbc327
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345517"
---
# <a name="idebugexpression-interface"></a>IDebugExpression-Schnittstelle
Stellt einen asynchron ausgewerteten Ausdruck dar. Skript-Engines werden in der Regel diese Schnittstelle implementieren. Ein Debugger-IDE verwendet diese Schnittstelle in der Regel eine unmittelbare Ausführung Fenster aktivieren oder die Überwachung (Fenster).  
  
> [!NOTE]
>  Die `IDebugExpression` Schnittstelle nur über einen Stapelrahmen verfügbar ist.  
  
 Zusätzlich zu den von geerbten Methoden `IUnknown`, `IDebugExpression` Schnittstelle verfügbar macht, die folgenden Methoden.  
  
## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[IDebugExpression::Start](../../winscript/reference/idebugexpression-start.md)|Beginnt die Auswertung des Ausdrucks an.|  
|[IDebugExpression::Abort](../../winscript/reference/idebugexpression-abort.md)|Bricht den Ausdruck ab.|  
|[IDebugExpression::QueryIsComplete](../../winscript/reference/idebugexpression-queryiscomplete.md)|Bestimmt, ob der Vorgang abgeschlossen ist.|  
|[IDebugExpression::GetResultAsString](../../winscript/reference/idebugexpression-getresultasstring.md)|Gibt das Ergebnis der Auswertung des Ausdrucks als eine Zeichenfolge und der Rückgabewert des Vorgangs zurück.|  
|[IDebugExpression::GetResultAsDebugProperty](../../winscript/reference/idebugexpression-getresultasdebugproperty.md)|Gibt das Ergebnis der Auswertung des Ausdrucks als eine Debugeigenschaft und der Rückgabewert des Vorgangs zurück.|