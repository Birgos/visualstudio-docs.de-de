---
title: Markerbericht | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 20e9ece55f1e17c874832f473236dfbae7684c54
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2019
ms.locfileid: "54833851"
---
# <a name="markers-report"></a>Markerbericht
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Der Markerbericht führt die Marker im angezeigten Zeitrahmen auf.  Das Schwenken, Zoomen oder Ausblenden von Bereichen führt, möglicherweise dazu, das Marker angezeigt werden oder wieder ausgeblendet werden. Der Bericht enthält folgende Informationen über jeden Marker:  
  
- Die Startzeit, relativ zum Beginn der Ablaufverfolgung.  
  
- Die Dauer. Die Dauer beträgt 0 (null) für Flags und Nachrichten, da sie einen Zeitpunkt darstellen.  
  
- Die ID des Threads, der sie generiert hat.  
  
- Die Ereignisablaufverfolgung (ETW) für den Windows-Anbieter, der diese generiert hat.  
  
- Die Markerreihe aus die er geschrieben wurde.  
  
- Die Kategorie der Ereignisse, denen er angehört.  
  
- Die Wichtigkeitsstufe.  
  
- Der Typ (span, flag oder message).  
  
- Eine allgemeine Beschreibung der Bedeutung.  
  
  Wählen Sie die Schaltfläche **Exportieren** aus, um den Markerbericht als CSV-Datei zu speichern. Sie können die Daten in der CSV-Datei mit anderen Apps oder Tools verwenden.  
  
> [!NOTE]
>  Der Markerbericht kann 1.000 Marker anzeigen. Um alle Marker anzuzeigen, exportieren Sie den vollständigen Bericht in eine CSV-Datei.
