---
title: Neuerungen bei der Profilerstellung | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling
- what's new
ms.assetid: d4736cc8-8961-4089-be9e-d5190ce8353c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b1822ec74903c8baa75ce437b0115cecdfb911c3
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55026944"
---
# <a name="whats-new-in-profiling-tools-in-includevsdev15miscincludesvsdev15mdmd"></a>Neuerungen bei den Profilerstellungstools in [!include[vs_dev15](../misc/includes/vs_dev15_md.md)]

Die Diagnosetools enthalten neue Visualisierungen, um Ihnen bei der Identifizierung von Problemen in Ihrer App zu helfen, die behoben werden müssen. Die Diagnosetools umfassen jetzt Unterstützung für ASP.NET-Apps.

Weitere Informationen finden Sie in den [Anmerkungen zu [!include[vs_dev15](../misc/includes/vs_dev15_md.md)]](/visualstudio/releasenotes/vs2017-relnotes#debuggingdiag).

Zu den Tools wurde eine Registerkarte **Zusammenfassung** hinzugefügt, die Ihnen dabei hilft, den Fokus für Ihre Leistungsanalyse auf die Hauptbereiche zu legen. Diese Registerkarte zeigt, wie viele Ereignisse aufgetreten sind, lässt Sie Momentaufnahmen des Heaps machen und schnell die Datensammlung für die CPU-Auslastung aktivieren. In dieser Ansicht werden alle Ereignisse von [Application Insights](/azure/azure-monitor/app/visual-studio) oder der [Analyse der Benutzeroberfläche](/visualstudio/releasenotes/vs2017-relnotes#UIAnalysis) gezeigt. Darüber hinaus werden in dieser Ansicht auch IntelliTrace-Ereignisse für Visual Studio Enterprise gezeigt.

![Zusammenfassung Diagnosetools](../profiling/media/DiagToolsSummaryTab-2.png "DiagToolsSummaryTab")

Das Tool für die CPU-Auslastung verfügt über [neue Visualisierungen](../profiling/Beginners-Guide-to-Performance-Profiling.md), um Ihnen beim Identifizieren der Funktionen zu helfen, die am wahrscheinlichsten Leistungsprobleme verursachen. Die neue Ansicht **Aufrufer/Aufgerufener** können Sie zum Untersuchen der Kosten von Funktionsaufrufen verwenden, die an eine und von einer ausgewählten Funktion erfolgen.

![Diagnosetools Ansicht Aufrufer-Aufgerufener](../profiling/media/DiagToolsCallerCallee.png "DiagToolsCallerCallee")

## <a name="see-also"></a>Siehe auch

- [Profilerstellung in Visual Studio](../profiling/index.md)
- [Einführung in Profilerstellungstools](../profiling/profiling-feature-tour.md)