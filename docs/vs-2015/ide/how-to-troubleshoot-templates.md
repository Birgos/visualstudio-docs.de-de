---
title: 'Vorgehensweise: Problembehandlung bei Vorlagen | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Visual Studio templates, troubleshooting
ms.assetid: 3e577ad2-f725-4c11-93b3-477f2404ec81
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a68097745de1f1d94e5c09963a474a0095588fba
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296425"
---
# <a name="how-to-troubleshoot-templates"></a>Gewusst wie: Problembehandlung bei Vorlagen
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Wenn keine Vorlage in der Entwicklungsumgebung geladen werden kann, gibt es einige Möglichkeiten, das Problem zu erfassen.  
  
## <a name="validating-the-vstemplate-file"></a>Überprüfen der VSTEMPLATE-Datei  
 Wenn die VSTEMPLATE-Datei in einer Vorlage nicht dem [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]-Vorlagenschema folgt, wird die Vorlage möglicherweise nicht im Dialogfeld **Neues Projekt** angezeigt.  
  
#### <a name="to-validate-the-vstemplate-file"></a>So überprüfen Sie die VSTEMPLATE-Datei  
  
1.  Suchen Sie die ZIP-Datei, die die Vorlage enthält.  
  
2.  Extrahieren Sie die ZIP-Datei.  
  
3.  Klicken Sie im Menü **Datei** in [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] auf **Öffnen** und dann auf **Datei**.  
  
4.  Wählen Sie die VSTEMPLATE-Datei für die Vorlage aus, und klicken Sie auf **Öffnen**.  
  
5.  Stellen Sie sicher, dass das XML-Format der VSTEMPLATE-Datei dem [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]-Vorlagenschema folgt. Weitere Informationen zum VSTEMPLATE-Schema finden Sie in der [Schemareferenz zu Visual Studio-Vorlagen](../extensibility/visual-studio-template-schema-reference.md).  
  
    > [!NOTE]
    >  Um IntelliSense-Unterstützung während der Erstellung der VSTEMPLATE-Datei abzurufen, fügen Sie eine `xmlns` -Attribut auf die `VSTemplate` Element, und weisen sie einen Wert von http://schemas.microsoft.com/developer/vstemplate/2005.  
  
6.  Speichern und schließen Sie die VSTEMPLATE-Datei.  
  
7.  Wählen Sie die Dateien aus, die in Ihrer Vorlage enthalten sind, klicken Sie mit der rechten Maustaste auf diese, wählen Sie **Senden an** aus, und klicken Sie auf **ZIP-komprimierter Ordner**. Die ausgewählten Dateien werden in einer ZIP-Datei komprimiert.  
  
8.  Platzieren Sie die neue ZIP-Datei in demselben Verzeichnis, in dem sich auch die alte ZIP-Datei befand.  
  
9. Löschen Sie die extrahierten Vorlagendateien und die alte ZIP-Datei der Vorlage.  
  
## <a name="monitoring-the-event-log"></a>Überwachen des Ereignisprotokolls  
 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] protokolliert Fehler, die bei der Verarbeitung von ZIP-Vorlagendateien aufgetreten sind. Wenn eine Vorlage nicht wie erwartet im Dialogfeld **Neues Projekt** angezeigt wird, können Sie die **Ereignisanzeige** zur Behebung des Problems verwenden.  
  
#### <a name="to-locate-template-errors-in-event-viewer"></a>So suchen Sie Vorlagenfehler in der Ereignisanzeige  
  
1.  Klicken Sie in Windows auf **Start** und **Systemsteuerung**, und doppelklicken Sie auf **Verwaltung** und dann auf **Ereignisanzeige**.  
  
2.  Klicken Sie im linken Bereich auf **Anwendung**.  
  
3.  Suchen Sie mit dem **Quellwert** `Visual Studio - VsTemplate` nach Ereignissen.  
  
4.  Doppelklicken Sie auf ein Vorlagenereignis, um den Fehler anzuzeigen.  
  
## <a name="see-also"></a>Siehe auch  
 [Anpassen von Vorlagen](../ide/customizing-project-and-item-templates.md)   
 [Erstellen von Projekt- und Elementvorlagen](../ide/creating-project-and-item-templates.md)   
 [Schemareferenz zu Visual Studio-Vorlagen](../extensibility/visual-studio-template-schema-reference.md)



