---
title: Angeben der in Auslastungstestszenarios zu verwendenden Test-Agents
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- test agents, load tests
- load tests, scenarios
- load tests, specifying for load tests
- tests agents, load tests, specifying
- load tests, test agents
ms.assetid: e86806dd-5897-4e4c-bfd4-8d687fb72a6e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.openlocfilehash: ef1325fbe568e82f03d694523a4580f2d61265c6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54966737"
---
# <a name="how-to-specify-test-agents-to-use-in-load-test-scenarios"></a>Vorgehensweise: Angeben der in Auslastungstestszenarios zu verwendenden Test-Agents

Nachdem Sie den Auslastungstest mithilfe des **Assistenten für neuen Auslastungstest** erstellt haben, können Sie die Szenarioeigenschaften mit dem **Auslastungstest-Editor** entsprechend Ihren Testanforderungen und -zielen ändern.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

> [!NOTE]
> Eine vollständige Liste der Eigenschaften von Auslastungstestszenarios und deren Beschreibungen finden Sie unter [Load test scenario properties (Eigenschaften von Auslastungstestszenarios)](../test/load-test-scenario-properties.md).

Die Agents werden mit dem **Auslastungstest-Editor** angegeben, um die Eigenschaft **Zu verwendende Agents** im **Eigenschaftenfenster** zu ändern.

Sie können die Agents angeben, die für das zu verwendende Szenario verwendet werden sollen, wenn Sie den Auslastungstest remote mithilfe von Controllern und Agents ausführen. Sie möchten z. B. einen bestimmten Satz von Agents angeben, damit Sie die Konsistenz beim Analysieren von Leistungstrends aufrechterhalten. Zudem sind Agents möglicherweise geografisch verteilt, sodass bezüglich der ausgeführten Skripts und dem Standort des Agents eine Affinität besteht.

> [!TIP]
> Neben der physischen Anordnung eines Agents auf der Remotewebsite besteht auch die Möglichkeit, die Netzwerkemulation zum Emulieren des langsamen Netzwerks zu verwenden. Weitere Informationen finden Sie unter [Angeben von virtuellen Netzwerktypen](../test/specify-virtual-network-types-in-a-load-test-scenario.md).

Weitere Informationen finden Sie unter [Test controllers and test agents (Testcontroller und Test-Agents)](configure-test-agents-and-controllers-for-load-tests.md).

Ein anderer Grund besteht darin, dass möglicherweise auf einigen, jedoch nicht allen Agents Software installiert ist, die für ein bestimmtes Szenario erforderlich ist.

Sie können die Agent-Auswahl für einen angegebenen Testlauf mit Rollen in den Testeinstellungen steuern. Weitere Informationen finden Sie unter [Erfassen von Diagnoseinformationen mithilfe von Testeinstellungen](../test/collect-diagnostic-information-using-test-settings.md).

Fügen Sie dem Auslastungstest mehr Agents hinzu, wenn auf einem Test-Agent-Computer eine CPU-Auslastung von mehr als 75 Prozent vorliegt oder weniger als 10 Prozent des physischen Speichers verfügbar sind. So können Sie sicherstellen, dass der Agent-Computer nicht zum Engpass im Auslastungstest wird.

## <a name="to-specify-the-agents-to-use-for-a-scenario"></a>So geben Sie die Agents an, die für ein Szenario verwendet werden sollen

1.  Öffnen Sie einen Auslastungstest.

     Der **Auslastungstest-Editor** wird angezeigt. Die Auslastungsteststruktur wird angezeigt.

2.  Klicken Sie im Ordner **Szenarios** der Auslastungsteststruktur auf den Szenarioknoten, für den Sie die zu verwendenden Agents angeben möchten.

3.  Klicken Sie im Menü **Ansicht** auf **Eigenschaftenfenster**.

     Die Szenariokategorien und -eigenschaften werden im Fenster **Eigenschaften** angezeigt.

4.  Geben Sie im Textfeld für die Eigenschaft **Zu verwendende Agents** die Liste der Agents ein, mit denen das Szenario möglicherweise ausgeführt wird.

     Agents müssen durch Kommas getrennt sein, z.B. **Agent1, Agent2, Agent3**. Wenn Sie keine Eigenschaft angeben, verwendet das Szenario alle verfügbaren Agents.

    > [!NOTE]
    > Die Eigenschaft **Zu verwendende Agents** wird bei lokalen Testläufen ignoriert. Wenn bei Remotetestläufen keiner der in **Zu verwendende Agents** angegebenen Agents vorhanden ist, werden im Szenario keine Tests ausgeführt.

5.  Klicken Sie nach dem Ändern der Eigenschaft auf im Menü **Datei** auf **Speichern**. Sie können anschließend den Auslastungstest mit dem neuen Wert für **Zu verwendende Agents** ausführen.

## <a name="see-also"></a>Siehe auch

- [Bearbeiten von Auslastungstestszenarios](../test/edit-load-test-scenarios.md)
- [Exemplarische Vorgehensweise: Erstellen und Ausführen eines Auslastungstests](../test/walkthrough-create-and-run-a-load-test.md)
- [Testcontroller und Test-Agents](configure-test-agents-and-controllers-for-load-tests.md)
- [Load test scenario properties (Eigenschaften von Auslastungstestszenarios)](../test/load-test-scenario-properties.md)