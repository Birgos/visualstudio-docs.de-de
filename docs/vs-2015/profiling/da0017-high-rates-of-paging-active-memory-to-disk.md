---
title: 'DA0017: Hohes Maß an Paging von aktivem Speicher auf den Datenträger | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.17
- vs.performance.rules.DA0017
- vs.performance.DA0017
ms.assetid: 01011eec-5930-43b3-980d-2cb01e2ca7f6
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6a7fbe924ee3d0f5dbd142d8e7f7020c6eed1ee5
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51766584"
---
# <a name="da0017-high-rates-of-paging-active-memory-to-disk"></a>DA0017: Hohes Maß an Paging von aktivem Speicher auf den Datenträger
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Regel-Id | DA0017 |  
| Kategorie | Speicher und Auslagerung |  
| Profilerstellungsmethode | Alle |  
| Nachricht | Ein hohes Maß an paging von aktivem Speicher auf den Datenträger wurde festgestellt. Ihre Anwendung ist möglicherweise speichergebunden. |  
| Regeltyp | Informationen |  
  
 Wenn Sie Profile mithilfe der Sampling-, .NET-Arbeitsspeicher- oder Ressourcenkonfliktmethode Profile erstellen, müssen mindestens 10 Samplings erfasst werden, damit diese Regel ausgelöst wird.  
  
## <a name="cause"></a>Ursache  
 Die bei der Profilerstellung erfassten Systemleistungsdaten deuten darauf hin, dass während der Profilerstellung ein hohes Maß an Auslagerungen von aktivem Speicher auf den Datenträger (und umgekehrt) aufgetreten ist. Solch hohe Auslagerungsraten wirken sich in der Regel negativ auf Leistung und Reaktionszeit der Anwendung aus. Verringern Sie ggf. die Speicherbelegungen, indem Sie die Algorithmen überarbeiten. Sie müssen möglicherweise auch die Speicheranforderungen der Anwendung berücksichtigen.  
  
## <a name="rule-description"></a>Regelbeschreibung  
  
> [!NOTE]
>  Diese Informationsregel wird ausgelöst, wenn die Auslagerung des aktiven Speichers ein hohes Maß erreicht. Bei Erreichen eines äußerst hohen Auslagerungsaufkommens wird stattdessen die Warnregel [DA0014: Äußerst hohes Maß an Paging von aktivem Speicher auf den Datenträger](../profiling/da0014-extremely-high-rates-of-paging-active-memory-to-disk.md) ausgelöst.  
  
 Eine übermäßige Auslagerung auf den Datenträger kann auf einen zu kleinen physischen Speicher zurückzuführen sein. Wenn der physische Datenträger, auf dem sich die Auslagerungsdatei befindet, hauptsächlich für Auslagerungsvorgänge verwendet wird, kann dies zu einer Verlangsamung anderer anwendungsorientierter Datenträgervorgänge auf diesem Datenträger führen.  
  
 Seiten werden häufig in Massenauslagerungsvorgängen vom Datenträger gelesen oder auf den Datenträger geschrieben. Die Anzahl der geänderten Seiten pro Sekunde ist häufig deutlich größer als beispielsweise die Anzahl der Seiten-Schreibvorgänge pro Sekunde. Der Grund hierfür ist, dass die geänderten Seiten pro Sekunde auch geänderte Datenseiten aus dem Systemdateicache beinhalten. ist jedoch nicht immer einfach, den direkt für die Auslagerung verantwortlichen Prozess oder den Grund für die Auslagerung zu ermitteln.  
  
## <a name="how-to-fix-violations"></a>Behandeln von Verstößen  
 Doppelklicken Sie auf die Meldung im Fenster „Fehlerliste“, um zur Ansicht [Markierungen](../profiling/marks-view.md) zu navigieren. Suchen Sie die Spalte **Arbeitsspeicher\Seiten/s**. Überprüfen Sie, ob die Auslagerung von E/A-Aktivitäten in bestimmten Phasen der Programmausführung besonders häufig auftritt.  
  
 Wenn Sie in einem Auslastungstest-Szenario Profildaten für eine ASP.NET-Anwendung erfassen, führen Sie den Auslastungstest auf einem Computer mit zusätzlichem physischem Speicher (oder RAM) erneut aus.  
  
 Verringern Sie ggf. die Speicherbelegungen, indem Sie die Algorithmen überarbeiten, und vermeiden Sie speicherintensive APIs wie String.Concat und String.Substring.



