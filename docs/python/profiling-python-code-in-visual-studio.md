---
title: Messen der Leistung von Python-Code
description: Verwenden der Visual Studio-Profilerstellung zum Überprüfen der Leistung von Python-Code beim Einsatz von auf CPython basierenden Interpretern
ms.date: 11/12/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.custom: seodec18
ms.workload:
- python
- data-science
ms.openlocfilehash: d598ce08942ed159b7e03a282ccf9f378f89c889
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54979542"
---
# <a name="profile-python-code"></a>Profilerstellung für Python-Code

Sie können eine Python-Anwendung unter Verwendung von CPython-basierten Interpreten profilen. (Weitere Informationen zur Verfügbarkeit dieses Features für die verschiedenen Visual Studio-Versionen finden Sie unter [Featurematrix: Profilerstellung](overview-of-python-tools-for-visual-studio.md#matrix-profiling).)

## <a name="profiling-for-cpython-based-interpreters"></a>Profilerstellung für CPython-basierte Interpreter

Die Profilerstellung wird mit dem Menübefehl **Analysieren** > **Python-Profilerstellung starten** gestartet, worauf ein Konfigurationsdialogfeld geöffnet wird:

![Konfigurationsdialogfeld für Profilerstellung](media/profiling-start.png)

Wenn Sie die Option **OK** wählen, wird der Profiler ausgeführt und öffnet einen Leistungsbericht, anhand dessen Sie den Zeitaufwand in der Anwendung untersuchen können:

![Leistungsbericht für Profilerstellung](media/profiling-results.png)

|   |   |
|---|---|
| ![Kamerasymbol für Video](../install/media/video-icon.png "Video ansehen") | [Sehen Sie sich ein Video (Microsoft Virtual Academy)](https://mva.microsoft.com/en-US/training-courses-embed/python-tools-for-visual-studio-2017-18121/Video-Profiling-Python-s6FoC6LWE_1005918567) mit einer Demonstration zur Python-Profilerstellung an (3 Minuten, 0 Sekunden).|

> [!Note]
> Gegenwärtig unterstützt Visual Studio nur diese Stufe der vollständigen Erstellung von Anwendungsprofilen, aber wir freuen uns auf jeden Fall über Ihr Feedback zu künftigen Funktionen. Verwenden Sie unten auf dieser Seite die Schaltfläche [**Produktfeedback**](#feedback).

## <a name="profiling-for-ironpython"></a>Profilerstellung für IronPython

Da IronPython kein CPython-basierter Interpreter ist, funktioniert die oben genannte Profilerstellungsfunktion nicht.

Verwenden Sie stattdessen den Visual Studio .NET-Profiler, indem Sie *ipy.exe* direkt als Zielanwendung starten und die entsprechenden Argumente zum Starten Ihres Startskripts verwenden. Beziehen Sie `-X:Debug` in die Befehlszeile ein, um sicherzustellen, dass für Ihren gesamten Python-Code Debugging und Profilerstellung durchgeführt werden kann. Dieses Argument generiert einen Leistungsbericht einschließlich der sowohl in der IronPython-Laufzeit als auch Ihrem Code aufgewendeten Zeit. Ihr Code wird anhand beschädigter Namen identifiziert.

Alternativ verfügt IronPython über eigene integrierte Profilerstellungsmethoden, wofür es derzeit aber keine gute Schnellansicht gibt. Unter [An IronPython-Profiler](https://blogs.msdn.microsoft.com/curth/2009/03/30/an-ironpython-profiler/) (Ein IronPython-Profiler) (MSDN-Blogs) erfahren Sie, was verfügbar ist.
