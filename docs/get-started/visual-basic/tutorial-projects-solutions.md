---
title: Tutorialprojekte und -projektmappen für Visual Basic
ms.date: 12/12/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.custom: get-started
ms.topic: tutorial
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
ms.workload:
- dotnet
ms.openlocfilehash: b9de49d9e5c7c1ebbe8fef41ff5efdb65c96d6e9
ms.sourcegitcommit: e3d96b20381916bf4772f9db52b22275763bb603
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2019
ms.locfileid: "55483873"
---
# <a name="learn-about-projects-and-solutions-using-visual-basic"></a>Erfahren Sie mehr über Projekte und Projektmappen mithilfe von Visual Basic

In diesem einführenden Artikel erfahren Sie mehr über das Erstellen einer *Projektmappe* und eines *Projekts* in Visual Studio. Eine Projektmappe ist ein Container, der zum Organisieren von mindestens einem zugehörigen Codeprojekt verwendet wird, wie z. B. eines Klassenbibliotheksprojekts und dem entsprechenden Testprojekt. Die Eigenschaften eines Projekts und einige der darin enthaltenen Dateien sollen betrachtet werden. Darüber hinaus wird ein Verweis von einem Projekt auf das andere erstellt.

> [!TIP]
> Wenn Sie Visual Studio noch nicht installiert haben, können Sie es auf der Seite [Visual Studio-Downloads](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) kostenlos herunterladen.

Eine Projektmappe und ein Projekt werden von Grund auf neu erstellt, damit Sie das Konzept eines Projekts nachvollziehen können. Wenn Sie Visual Studio normalerweise verwenden, nutzen Sie sehr wahrscheinlich einige der verschiedenen *Projektvorlagen*, die Visual Studio bei der Erstellung eines neuen Projekts zur Verfügung stellt.

> [!NOTE]
> Projektmappen und Projekte werden nicht unbedingt zum Entwickeln von Apps in Visual Studio benötigt. Sie können auch einfach nur einen Ordner öffnen, der Code enthält, und mit dem Codieren, Erstellen und Debuggen beginnen. Wenn Sie beispielsweise ein [GitHub](https://github.com/)-Repository klonen, enthält dieses möglicherweise keine Visual Studio-Projekte und Projektmappen. Weitere Informationen finden Sie unter [Entwickeln von Code in Visual Studio ohne Projekte oder Projektmappen](../../ide/develop-code-in-visual-studio-without-projects-or-solutions.md).

## <a name="solutions-and-projects"></a>Projektmappen und Projekte

Trotz der englischen Bezeichnung „Solution“ ist eine Projektmappe keine „Lösung“. Projektmappen sind lediglich Container, die in Visual Studio zum Ordnen von mindestens einem Projekt verwendet werden. Wenn Sie eine Projektmappe in Visual Studio öffnen, werden automatisch alle Projekte geladen, die die Projektmappe enthält.

### <a name="create-a-solution"></a>Erstellen einer Projektmappe

Zunächst soll eine leere Projektmappe erstellt werden. Wenn Sie einmal mit Visual Studio vertraut sind, werden Sie wahrscheinlich eher selten leere Projektmappen erstellen. Wenn Sie in Visual Studio ein neues Projekt erstellen, wird automatisch auch eine Projektmappe für das Projekt erstellt, wenn noch keine geöffnet ist.

1. Öffnen Sie Visual Studio.

1. Wählen Sie in der Menüleiste (die Zeile, die Menüs wie **Datei** und **Bearbeiten** enthält) die Option **Datei** > **Neu** > **Projekt** aus.

   Das Dialogfeld **Neues Projekt** wird angezeigt.

1. Erweitern Sie im linken Bereich **Andere Projekttypen**, und klicken Sie dann auf **Visual Studio-Projektmappen**. Wählen Sie im mittleren Bereich die Vorlage **Leere Projektmappe** aus. Geben Sie Ihrer Projektmappe den Namen **QuickSolution**, und klicken Sie anschließend auf die Schaltfläche **OK**.

   ![Vorlage „Leere Projektmappe“ in Visual Studio](../media/tutorial-projects-new-solution.png)

   Die **Startseite** wird geschlossen, und im **Projektmappen-Explorer** wird auf der rechten Seite im Visual Studio-Fenster eine Projektmappe angezeigt. Sie verwenden den **Projektmappen-Explorer** wahrscheinlich häufig, um die Inhalte Ihrer Projekte zu durchsuchen.

### <a name="add-a-project"></a>Hinzufügen eines Projekts

Fügen Sie nun der Projektmappe Ihr erstes Projekt hinzu. Beginnen Sie mit einem leeren Projekt, und fügen Sie anschließend die benötigten Elemente hinzu.

1. Klicken Sie im Kontextmenü (Rechtsklick) der **Projektmappe „QuickSolution“** im **Projektmappen-Explorer** auf **Hinzufügen** > **Neues Projekt**.

   Das Dialogfeld **Neues Projekt hinzufügen** wird geöffnet.

1. Erweitern Sie im linken Bereich **Visual Basic**, und wählen Sie **Windows-Desktop** aus. Wählen Sie anschließend im mittleren Bereich die Vorlage **Leeres Projekt (.NET Framework)** aus. Geben Sie dem Projekt den Namen **QuickDate**, und klicken Sie anschließend auf die Schaltfläche **OK**.

   Unter der Projektmappe wird im **Projektmappen-Explorer** ein Projekt mit dem Namen „QuickDate“ angezeigt. Zu diesem Zeitpunkt enthält das Projekt nur eine Datei mit dem Namen *App.config*.

   > [!NOTE]
   > Wenn im linken Bereich des Dialogfelds nicht **Visual Basic** angezeigt wird, müssen Sie die *Workload* **.NET-Desktopentwicklung** von Visual Studio installieren. Visual Studio verwendet die Workload-basierte Installation, damit nur die Komponenten installiert werden, die Sie für Ihren Entwicklungstyp benötigen. Sie können dies problemlos über den Link **Visual Studio-Installer öffnen** im unteren linken Bereich des Dialogfelds **Neues Projekt hinzufügen** erledigen. Wählen Sie nach dem Starten des Visual Studio-Installers die Workload **.NET-Desktopentwicklung** aus, und klicken Sie anschließend auf die Schaltfläche **Ändern**.

   ![Öffnen des Links „Visual Studio-Installer“](media/tutorial-projects-open-installer-vb.png)

## <a name="add-an-item-to-the-project"></a>Hinzufügen eines Elements zum Projekt

Ihnen liegt ein leeres Projekt vor. Fügen Sie eine Codedatei hinzu.

1. Wählen Sie im Kontextmenü (Rechtsklick) des Projekts **QuickDate** im **Projektmappen-Explorer** die Option **Hinzufügen** > **Neues Element** aus.

   Das Dialogfeld **Neues Element hinzufügen** wird angezeigt.

1. Erweitern Sie **allgemeine Elemente**, und wählen Sie anschließend **Code** aus. Wählen Sie im mittleren Bereich die Elementvorlage **Klasse** aus. Geben Sie der Klasse den Namen **Kalender**, und klicken Sie anschließend auf die Schaltfläche **Hinzufügen**.

   Dem Projekt wird eine Datei mit dem Namen *Calendar.vb* hinzugefügt. Visual Basic-Codedateien wird am Ende des Dateinamens die Erweiterung *.vb* angefügt. Die Datei wird im **Projektmappen-Explorer** in der visuellen Projekthierarchie angezeigt, und ihre Inhalte werden im Editor geöffnet.

1. Ersetzen Sie den Inhalt der Datei *Calendar.vb* durch den folgenden Code:

   ```vb
   Class Calendar
       Public Shared Function GetCurrentDate() As Date
           Return DateTime.Now.Date
       End Function
   End Class
   ```

   Die `Calendar`-Klasse enthält eine einzelne Funktion (`GetCurrentDate`), die das aktuelle Datum zurückgibt.

1. Öffnen Sie die Projekteigenschaften, indem Sie im **Projektmappen-Explorer** auf **Mein Projekt** doppelklicken. Ändern Sie den **Anwendungstyp** auf der Registerkarte **Anwendung** in **Klassenbibliothek**. Dieser Schritt ist erforderlich, um das Projekt erfolgreich zu kompilieren.

1. Erstellen Sie das Projekt, indem Sie im **Projektmappen-Explorer** mit der rechten Maustaste auf **QuickDate** klicken und **Erstellen** auswählen. Im Fenster **Ausgabe** sollte nun eine Meldung zum erfolgreichen Buildvorgang angezeigt werden.

## <a name="add-a-second-project"></a>Hinzufügen eines zweiten Projekts

Projektmappen enthalten oft mehrere Projekte, die aufeinander verweisen. Bei einigen Projekten in der Projektmappe handelt es sich möglicherweise um Klassenbibliotheken oder einige ausführbare Anwendungen, und bei anderen handelt es sich möglicherweise um Komponententestprojekte oder Websites.

Fügen Sie Ihrer Projektmappe einen Komponententest hinzu. Beginnen Sie diesmal mit einer Projektvorlage, damit Sie dem Projekt keine zusätzliche Codedatei hinzufügen müssen.

1. Klicken Sie im Kontextmenü (Rechtsklick) der **Projektmappe „QuickSolution“** im **Projektmappen-Explorer** auf **Hinzufügen** > **Neues Projekt**.

   Das Dialogfeld **Neues Projekt hinzufügen** wird geöffnet.

1. Erweitern Sie im linken Bereich **Visual Basic**, und wählen Sie die Kategorie **Test** aus. Wählen Sie im mittleren Bereich die Projektvorlage **Komponententestprojekt (.NET Framework)** aus. Geben Sie dem Projekt den Namen **QuickTest**, und klicken Sie anschließend auf die Schaltfläche **OK**.

   Daraufhin wird dem **Projektmappen-Explorer** ein zweites Projekt hinzugefügt, und im Editor wird eine Datei mit dem Namen *UnitTest1.vb* geöffnet.

   ![Projektmappen-Explorer von Visual Studio mit zwei Projekten](media/tutorial-projects-solution-explorer-vb.png)

## <a name="add-a-project-reference"></a>Hinzufügen eines Projektverweises

Jetzt soll das neue Komponententestprojekt verwendet werden, um die Methode im Projekt **QuickDate** zu testen. Aus diesem Grund müssen Sie einen Verweis auf das Projekt hinzufügen. Dadurch entsteht eine *Buildabhängigkeit* zwischen den beiden Projekten, d.h., **QuickDate** wird beim Erstellen der Projektmappe vor **QuickTest** erstellt.

1. Klicken Sie im **QuickTest**-Projekt auf den Knoten **Verweise**, und klicken Sie anschließend im Kontextmenü (Rechtsklick) auf **Verweis hinzufügen**.

   ![Hinzufügen eines Verweismenüs](media/tutorial-projects-add-reference-vb.png)

   Das Dialogfeld **Verweis-Manager** wird geöffnet.

1. Erweitern Sie im linken Bereich **Projekte**, und wählen Sie **Projektmappe** aus. Aktivieren Sie im mittleren Bereich das Kontrollkästchen neben **QuickDate**, und klicken Sie dann auf **OK**.

   Dem **QuickDate**-Projekt wird ein Verweis hinzugefügt.

## <a name="add-test-code"></a>Hinzufügen von Testcode

1. Fügen Sie jetzt der Visual Basic-Codedatei Testcode hinzu. Ersetzen Sie den Inhalt von *UnitTest1.vb* durch den folgenden Code.

   ```vb
   <TestClass()> Public Class UnitTest1

       <TestMethod()> Public Sub TestGetCurrentDate()
           Assert.AreEqual(Date.Now.Date, QuickDate.Calendar.GetCurrentDate())
       End Sub

   End Class
   ```

   Unter einigen Teilen des Codes werden rote Wellenlinien angezeigt. Sie können diesen Fehler beheben, indem Sie das Testprojekt als [Friend-Assembly](/dotnet/visual-basic/programming-guide/concepts/assemblies-gac/friend-assemblies) für das **QuickDate**-Projekt festlegen.

1. Öffnen Sie im Projekt **QuickDate** die Datei *Calendar.vb*, falls diese noch nicht geöffnet ist, und fügen Sie die folgende [Imports-Anweisung](/dotnet/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type) und das folgende Attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> zur Datei hinzu, um den Fehler im Testprojekt zu beheben.

   ```vb
   Imports System.Runtime.CompilerServices

   <Assembly: InternalsVisibleTo("QuickTest")>
   ```

   Die Codedatei sollte wie folgt aussehen:

   ![Visual Basic-Code](media/tutorial-projects-code-vb.png)

## <a name="project-properties"></a>Projekteigenschaften

In der Zeile in der Datei *Calendar.vb* mit dem Attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> wird auf den Assemblynamen (Dateinamen) des Projekts **QuickTest** verwiesen. Der Assemblyname stimmt nicht immer mit dem Projektnamen überein. Öffnen Sie die Projekteigenschaften, um den Assemblynamen eines Projekts zu suchen.

1. Wählen Sie im **Projektmappen-Explorer** das **QuickTest**-Projekt aus. Wählen Sie im Kontextmenü (Rechtsklick) **Eigenschaften** aus, oder drücken Sie **ALT**+**EINGABETASTE**. (Alternativ können Sie hierfür im **Projektmappen-Explorer** auf **Mein Projekt** doppelklicken.)

   Die *Eigenschaftenseiten* für das Projekt werden auf der Registerkarte **Anwendung** geöffnet. Die Eigenschaftenseiten enthalten verschiedene Einstellungen für das Projekt. Beachten Sie, dass der Assemblyname des **QuickTest**-Projekts tatsächlich „QuickTest“ lautet. Falls gewünscht können Sie ihn an dieser Stelle ändern. Wenn Sie das Testprojekt erstellen, ändert sich der Name der entstandenen Binärdatei von *QuickTest.dll* in den von Ihnen ausgewählten Namen.

   ![Projekteigenschaften](../media/tutorial-projects-properties.png)

1. Entdecken Sie einige der anderen Registerkarten der Eigenschaftenseiten des Projekt, z.B. **Kompilieren** und **Einstellungen**. Diese Registerkarten sind bei den verschiedenen Projekttypen unterschiedlich.

## <a name="optional-run-the-test"></a>Ausführen des Tests (Optional)

Wenn Sie testen möchten, ob der Komponententest funktioniert, klicken Sie in der Menüleiste auf **Testen** > **Ausführen** > **Alle Tests**. Ein Fenster mit dem Namen **Test-Explorer** wird geöffnet, und der **TestGetCurrentDate**-Test sollte erfolgreich sein.

![Test-Explorer in Visual Studio, der erfolgreiche Tests anzeigt](../media/tutorial-projects-test-explorer.png)

> [!TIP]
> Wenn Sich der **Test-Explorer** nicht automatisch öffnet, können Sie ihn über die Menüleiste öffnen, indem Sie auf **Test** > **Windows** > **Test-Explorer** klicken.

## <a name="next-steps"></a>Nächste Schritte

Wenn Sie Visual Studio näher kennenlernen möchten, können Sie eine App erstellen, indem Sie eines der [Tutorials zu Visual Basic](index.yml) durchführen.

## <a name="see-also"></a>Siehe auch

- [Erstellen von Projekten und Projektmappen](../../ide/creating-solutions-and-projects.md)
- [Verwalten von Projekt- und Projektmappeneigenschaften](../../ide/managing-project-and-solution-properties.md)
- [Verwalten von Verweisen in einem Projekt](../../ide/managing-references-in-a-project.md)
- [Entwickeln von Code in Visual Studio ohne Projekte oder Projektmappen](../../ide/develop-code-in-visual-studio-without-projects-or-solutions.md)
- [Übersicht über die Visual Studio-IDE](../../get-started/visual-studio-ide.md)