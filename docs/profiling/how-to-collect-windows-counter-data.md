---
title: 'Vorgehensweise: Sammeln von Windows-Indikatordaten | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.syscounter
- vs.performance.property.wincounter
helpviewer_keywords:
- windows counters
- performance tools, using windows counters
- profiling tools, using windows counters
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5d9554740cc576fc90ed232e64dbc4f73b619a8f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55022468"
---
# <a name="how-to-collect-windows-counter-data"></a>Vorgehensweise: Sammeln von Windows-Indikatordaten

Windows-Indikatoren sind Systemleistungsindikatoren, die während der Profilerstellung in festgelegten Intervallen gesammelt werden können In der Markierungsansicht des Berichts „Profilerstellungstools“, wird eine Zeile für jedes Sammlungsintervall als **AutoMark** bezeichnet. Die Zeile enthält Spalten, die die Leistungsindikatorwerte in diesem Intervall beschreibt. Klicken Sie zum Beschränken der Analyse auf eine Zeitraum zwischen zwei bestimmten Markierungen auf die Markierungen, anschließend auf die rechte Maustaste, und wählen Sie dann im Kontextmenü **Filtern nach** > **Markierungen** aus

> [!NOTE]
> Verbesserte Sicherheitsfunktionen in Windows 8 und Windows Server 2012 erforderten tiefgreifende Änderungen bei der Datenerfassung des Visual Studio-Profilers auf diesen Plattformen. Außerdem benötigen UWP-Apps neue Erfassungsmethoden. Siehe [Profilerstellungstools für Windows 8- und Windows Server 2012-Anwendungen](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="to-collect-windows-counter-data"></a>So sammeln Sie Windows-Indikatordaten

1. Klicken Sie im Leistungs-Explorer mit der rechten Maustaste auf die Sitzung, für die Sie Windows-Indikatoren konfigurieren möchten, und wählen Sie **Eigenschaften** aus.

2. Klicken Sie in den **Eigenschaftenseiten** auf **Windows-Indikatoren**.

3. Wählen Sie das Kontrollkästchen **Windows-Indikatoren auflisten** aus.

4. Geben Sie im Textfeld **Sammlungsintervall (ms)** ein Zeitintervall ein.

5. Wählen Sie eine Kategorie aus der Dropdownliste **Indikatorkategorie** aus.

6. Wählen Sie eine Instanz aus der Dropdownliste **Instanz** aus.

7. Wählen Sie die Indikatoren aus, die Sie bei der Profilerstellung Ihrer Anwendung verwenden möchten.

8. Klicken Sie auf **Übernehmen**.

## <a name="see-also"></a>Siehe auch

[Konfigurieren von Leistungssitzungen](../profiling/configuring-performance-sessions.md)  
[Eigenschaften von Leistungssitzungen](../profiling/performance-session-properties.md)  
[CPU- und Windows-Indikatoren](../profiling/cpu-and-windows-counters.md)