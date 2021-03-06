---
title: 'Vorgehensweise: Suchen nach einem Fenster in der Windows-Ansicht | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- windows, searching in Windows view
ms.assetid: 30306970-b861-4315-acf8-f86a43d4e73b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1526ed73b1a4f5c665f6b60c3cbb7e5b0b659380
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54974057"
---
# <a name="how-to-search-for-a-window-in-windows-view"></a>Vorgehensweise: Suchen nach einem Fenster in der Fensteransicht
Sie können für ein bestimmtes Fenster in der Windows-Ansicht mit das Handle, Beschriftung, Klasse oder eine Kombination der Beschriftung und die Klasse als Suchkriterium suchen. Sie können auch die anfangsrichtung für die Suche angeben. Die Felder im Dialogfeld werden die Attribute des ausgewählten Fensters in der Fensterstruktur im angezeigt werden.  
  
 Beginnen Sie mit der Struktur auf der zweiten Ebene (alle Fenster, die untergeordnete Elemente des Desktops), erweitert, damit Sie Windows-Desktop auf von ihren Klassennamen und den Titel identifizieren können. Nachdem Sie ein Fenster auf Desktop-Ebene ausgewählt haben, können Sie dieser Ebene um ein bestimmtes untergeordnetes Fenster suchen erweitern.  
  
### <a name="to-search-for-a-window-in-windows-view"></a>Suchen Sie nach einem Fenster in Windows-Ansicht  
  
1. Ordnen Sie die Fenster also, Spy++, die [Windows-Ansicht](../debugger/windows-view.md) Fenster und das Ziel sind sichtbar.  
  
2. Von der **Suche** Menü wählen **Fenster Suchen**.  
  
    Die [Dialogfeld Fenstersuche](../debugger/window-search-dialog-box.md) wird geöffnet.  
  
   > [!TIP]
   >  Um die Übersichtlichkeit des Bildschirms, wählen Sie die **Spy++ ausblenden** Option. Mit dieser Option das Hauptfenster Spy++ verbirgt und verbleibt nur der **Fenstersuche** Dialogfeld sichtbar ist, zusätzlich zu anderen Anwendungen. Spy++-Hauptfenster wird wiederhergestellt, wenn Sie auf **OK** oder **Abbrechen**, oder wenn Sie das Kontrollkästchen der **Spy++ ausblenden** Option.  
  
3. Ziehen Sie die **Suchtool** über das Zielfenster. Wie Sie das Tool, ziehen Sie die **Fenstersuche** Dialogfeld zeigt die Details für das ausgewählte Fenster.  
  
   - ODER  
  
     Wenn Sie wissen das Handle des Fensters werden sollen (z. B. aus dem Debugger), können Sie eingeben, in der **behandeln** Feld.  
  
   - ODER  
  
     Wenn Sie wissen, die Beschriftung und/oder die Klasse des Fensters werden sollen, können Sie eingeben, in der **Beschriftung** und **Klasse** Textfelder, und Deaktivieren der **behandeln** Textfeld.  
  
4. Wählen Sie **einrichten** oder **unten** für die anfängliche Richtung für die Suche.  
  
5. Klicken Sie auf **OK**.  
  
    Wenn ein entsprechendes Fenster gefunden wird, ist die Hervorhebung der [Windows-Ansicht](../debugger/windows-view.md) Fenster.