---
title: Testmischung der Browser für Auslastungstests
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, web browser types
- load tests, scenarios
- load tests, adding browsers
- load tests, removing browsers
ms.assetid: 47f981d9-3038-45cc-a486-82b9daf9a9a1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.openlocfilehash: 722efbae40cb5e11f91a75a858ba89df4688a4c9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988102"
---
# <a name="edit-the-test-mix-to-specify-which-web-browsers-types-in-a-load-test-scenario"></a>Bearbeiten der Testmischung zur Angabe der Webbrowsertypen in einem Auslastungstestszenario

Mithilfe des *Browsermix* kann die Auslastung in einem Auslastungstestszenario realistischer simuliert werden. Die Auslastung wird dabei nicht durch einen einzelnen Webbrowser, sondern durch eine heterogene Webbrowsermischung erzeugt. Dies ergibt eine bessere Annäherung an die Auslastung durch die Webbrowser, die im Normalfall mit Ihren Anwendungen verwendet werden.

Ein Browsermix legt die Wahrscheinlichkeit fest, mit der ein virtueller Benutzer einen bestimmten Webbrowsertyp in einem Auslastungstestszenario verwendet. Beim Erstellen eines Auslastungstests möchten Sie ggf. simulieren, dass die Auslastung durch verschiedene Webbrowser generiert wird. Wenn Sie der Mischung einen Webbrowsertyp aus den verfügbaren Webbrowsern hinzufügen, wird allen HTTP-Anforderungen, die von einem Webleistungstest gesendet werden, ein diesem Webbrowser zugeordneter Satz an Headern hinzugefügt.

Der Browsermix funktioniert wie andere Mischoptionen. Einem virtuellen Benutzer wird auf Grundlage des Browsermix zufällig ein Webbrowsertyp zugeordnet. Die Tests dieses Benutzers werden auf einem bestimmten Webbrowser ausgeführt, basierend auf der Wahrscheinlichkeit, die in der Mischung angegeben wurde.

Sie können dem Browsermix jederzeit weitere Webbrowsertypen hinzufügen oder Webbrowsertypen aus der Mischung entfernen. Über die Mischungssteuerung kann auch die Verteilung des Browsermixes geändert werden. Mit der Mischungssteuerung können Sie die Verteilung der Browser in einem Szenario auf einfache Weise anpassen.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="add-new-browsers-to-a-scenario"></a>Hinzufügen neuer Browser zu einem Szenario

### <a name="to-add-new-browsers-to-a-scenario"></a>So fügen Sie einem Szenario neue Browser hinzu

1.  Klicken Sie während des Angebens des Browsermix für ein Szenario auf **Hinzufügen**.

     Dem Raster wird ein neuer Browsereintrag hinzugefügt.

    > [!NOTE]
    > Klicken Sie mit der rechten Maustaste auf ein vorhandenes Szenario, und klicken Sie anschließend auf **Browsermix bearbeiten**, um das Dialogfeld **Browsermix bearbeiten** anzuzeigen.

2.  Klicken Sie in der Spalte **Browsertyp** auf den Pfeil für den neuen Eintrag, und wählen Sie den gewünschten Browsertyp aus.

3.  (Optional) Passen Sie die Mischungssteuerung an, um die Testverteilung anzugeben.

4.  Wenn Sie keine weiteren Browser hinzufügen möchten, klicken Sie auf **OK**.

##  <a name="remove-browsers-from-a-scenario"></a>Entfernen von Browsern aus einem Szenario

### <a name="to-remove-browsers-from-a-scenario"></a>So entfernen Sie Browser aus einem Szenario

1.  Öffnen Sie einen Auslastungstest.

2.  Klicken Sie mit der rechten Maustaste auf das Szenario, aus dem ein Browser entfernt werden soll, und klicken Sie auf **Browsermix bearbeiten**.

     Das Dialogfeld **Browsermix bearbeiten** wird angezeigt.

3.  Wählen Sie den Browser in der Tabelle aus, und klicken Sie dann auf **Entfernen**.

4.  (Optional) Passen Sie die Mischungssteuerung an, um die Testverteilung anzugeben.

5.  Wenn Sie keine weiteren Browser entfernen möchten, klicken Sie auf **OK**.

## <a name="about-the-mix-control"></a>Informationen zur Mischungssteuerung

 Mithilfe der Mischungssteuerung können Sie die Lastprozentsätze anpassen, die in einem Auslastungstestszenario auf die Tests, Browsertypen bzw. Netzwerktypen verteilt werden. Die Prozentsätze werden mit Schiebereglern angepasst. Die Mischung für die Browsertypen gibt die Wahrscheinlichkeit an, mit der ein virtueller Benutzer einen bestimmten Browsertyp in einem Auslastungstestszenario ausführt.

 Wenn Sie einen Schieberegler bewegen, werden die Prozentwerte aller verfügbaren Elemente geändert. Wenn mehr als zwei Elemente vorhanden sind, wird der hinzugefügte bzw. entfernte Betrag gleichmäßig auf die anderen Elemente verteilt. Dieses Verhalten kann geändert werden. Wenn Sie für ein bestimmtes Element das Kontrollkästchen in der Sperrspalte aktivieren, wird der für dieses Element festgelegte Prozentsatz gesperrt. Wenn Sie anschließend einen Schieberegler bewegen, wird der hinzugefügte bzw. entfernte Betrag nur auf die verbleibenden, nicht gesperrten Elemente verteilt.

 Mit der Schaltfläche **Verteilen** werden die Prozentsätze gleichmäßig auf alle Elemente verteilt. Wenn beispielsweise drei Elemente vorhanden sind und Sie auf die Schaltfläche **Verteilen** klicken, werden die Prozentsätze auf 34, 33 und 33 festgelegt.

> [!WARNING]
> Gesperrte Elemente werden durch Klicken auf die Schaltfläche **Verteilen** überschrieben.

 Statt die Schieberegler zu verwenden, können Sie die Prozentsätze auch direkt in die Spalte **%** eintragen. Wenn Sie einen Prozentsatz direkt eingeben, werden die anderen Elemente nicht automatisch angepasst.

> [!NOTE]
> Die Schieberegler werden deaktiviert, wenn die Gesamtsumme nicht 100 % ergibt oder Dezimalwerte in die Spalte **%** eingetragen werden.

 Wenn Sie Prozentsätze manuell eingeben, sollten Sie sich vergewissern, dass die Summe aller Elemente 100 % ergibt. Wenn Sie eine Mischung speichern, deren Summe nicht 100 % beträgt, werden Sie aufgefordert, die vorhandenen Prozentsätze zu bestätigen oder anzupassen. Wenn Sie die Prozentsätze bestätigen, werden diese anteilsmäßig auf 100 % umgerechnet.  Wenn beispielsweise zwei Elemente vorhanden sind und Sie diese auf 80 % und 40 % festgelegt haben, wird das erste Element auf 66,67 % (80 geteilt durch 120) und das zweite Element auf 33,33 % (40 geteilt durch 120) festgelegt.

## <a name="see-also"></a>Siehe auch

- [Bearbeiten von Auslastungstestszenarios](../test/edit-load-test-scenarios.md)