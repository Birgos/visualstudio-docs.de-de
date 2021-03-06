---
title: IDebugExpressionContext-Schnittstelle | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugExpressionContext Interface
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugExpressionContext interface
ms.assetid: 52af82e8-0dec-49e2-a7f3-d00f66ca1401
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 12b997d5edab866f77dcb71f4d5ea0273786c577
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345980"
---
# <a name="idebugexpressioncontext-interface"></a>IDebugExpressionContext-Schnittstelle
Stellt einen Kontext, in dem Ausdrücke ausgewertet werden können. Das Stack-Frame-Objekt implementiert diese Schnittstelle.  
  
 Zusätzlich zu den von geerbten Methoden `IUnknown`, `IDebugExpressionContext` Schnittstelle verfügbar macht, die folgenden Methoden.  
  
## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[IDebugExpressionContext::ParseLanguageText](../../winscript/reference/idebugexpressioncontext-parselanguagetext.md)|Erstellt einen Debug-Ausdruck für den angegebenen Text.|  
|[IDebugExpressionContext::GetLanguageInfo](../../winscript/reference/idebugexpressioncontext-getlanguageinfo.md)|Gibt einen Namen und eine GUID zurück, für die Sprache, die diesem Kontext besitzt.|