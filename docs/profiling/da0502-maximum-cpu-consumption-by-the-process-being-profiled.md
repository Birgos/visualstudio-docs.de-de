---
title: 'DA0502: Maximale CPU-Auslastung durch den Prozess, für den die Profilerstellung ausgeführt wird | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DA0502
- vs.performance.DA0502
- vs.performance.502
ms.assetid: 1ee53df5-b0dc-4265-9d4f-527830d08725
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1a9e2f83bc985423bad8764626be965d29148eed
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54923752"
---
# <a name="da0502-maximum-cpu-consumption-by-the-process-being-profiled"></a>DA0502: Maximale CPU-Auslastung durch den Prozess, für den die Profilerstellung ausgeführt wird

|||  
|-|-|  
|Regel-ID|DA0502|  
|Kategorie|Ressourcenüberwachung|  
|Profilerstellungsmethode|Alle|  
|Meldung|Diese Regel dient nur als Information. Der Leistungsindikator für die Process()\\%-Prozessorzeit dient zum Messen der CPU-Auslastung des Prozesses, für den die Profilerstellung ausgeführt wird. Bei dem gemeldeten Wert handelt es sich um den Maximalwert aus allen Messintervallen.|  
|Regeltyp|Information|  

 Wenn Sie Profile mithilfe der Sampling-, .NET-Arbeitsspeicher- oder Ressourcenkonfliktmethode Profile erstellen, müssen mindestens 10 Samplings erfasst werden, damit diese Regel ausgelöst wird.  

## <a name="rule-description"></a>Regelbeschreibung  
 In dieser Meldung wird der maximale Prozentsatz der Zeit angegeben, die ein Prozessor mit dem Ausführen von Anweisungen aus der Anwendung beschäftigt war. Bei dem gemeldeten Wert handelt es sich um den Maximalwert aller Messintervalle, in denen der Prozess, dessen Profil erstellt wird, aktiv war. Bei einem Computer mit mehreren Prozessoren kann der Prozentsatz 100 Prozent übersteigen.  

## <a name="how-to-use-the-rule-data"></a>Verwenden der Regeldaten  
 Mithilfe des Regelwerts können Sie die Leistung anderer Versionen oder Builds des Programms vergleichen oder die Leistung der Anwendung in unterschiedlichen Profilerstellungsszenarios nachvollziehen.