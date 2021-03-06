---
title: Erstellen Ihrer ersten C#-Konsolenanwendung mit Visual Studio
titleSuffix: ''
description: Hier finden Sie eine ausführliche Anleitung zum Erstellen einer einfachen „Hallo Welt“-Konsolenanwendung mit C# in Visual Studio.
ms.date: 09/21/2018
ms.prod: visual-studio-dev15
ms.custom: seodec18
ms.topic: quickstart
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: 4ec3adbd0a8c8d6a4e37879295b040b3f91e66bd
ms.sourcegitcommit: 0f7411c1a47d996907a028e920b73b53c2098c9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55690178"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-c-console-app"></a>Schnellstart: Erstellen Ihrer ersten C#-Konsolenanwendung mit Visual Studio

Mithilfe dieser fünf- bis zehnminütigen Einführung in die integrierte Entwicklungsumgebung (IDE) von Visual Studio, können Sie eine einfache C#-Anwendung erstellen, die in der Konsole ausgeführt werden kann.

Wenn Sie Visual Studio noch nicht installiert haben, können Sie es auf der Seite [Visual Studio-Downloads](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) kostenlos herunterladen.

## <a name="create-a-project"></a>Erstellen eines Projekts

Zunächst müssen Sie ein Projekt für die C#-Anwendung erstellen. Der Projekttyp enthält, schon bevor Sie mit der Bearbeitung beginnen, alle Vorlagendateien, die Sie benötigen.

1. Öffnen Sie Visual Studio 2017.

2. Klicken Sie in der Menüleiste im oberen Bereich auf **Datei** > **Neu** > **Projekt**.

3. Erweitern Sie im linken Dialogfeld **Neues Projekt** den Eintrag **C#**, und klicken Sie auf **.NET Core**. Wählen Sie im mittleren Bereich die Option **Konsolenanwendung (.NET Core)** aus. Nennen Sie dann das Projekt *HalloWelt*.

   ![Projektvorlage „Console App (.NET Core)“ im Dialogfeld „Neues Projekt“ in der Visual Studio-IDE](../ide/media/new-project-csharp-dotnetcore-helloworld-console-app.png)

     Falls Sie die Projektvorlage **Konsolenanwendung (.NET Core)** nicht finden, klicken Sie auf den Link **Visual Studio-Installer öffnen** auf der linken Seite des Dialogfelds **Neues Projekt**.

   ![Auswählen des Links „Visual Studio-Installer öffnen“ im Dialogfeld „Neues Projekt“](../ide/media/csharp-open-visual-studio-installer-hello-world.png)

     Der Visual Studio-Installer wird gestartet. Wählen Sie die Workload **Plattformübergreifende .NET Core-Entwicklung** aus, und klicken Sie dann auf **Anpassen**.

     ![Workload „Plattformübergreifende .NET Core-Entwicklung“ im Visual Studio-Installer](../ide/media/dot-net-core-xplat-dev-workload.png)

## <a name="create-the-application"></a>Erstellen der Anwendung

Nachdem Sie Ihre C#-Projektvorlage ausgewählt und Ihr Projekt benannt haben, erstellt Visual Studio eine einfache „Hallo Welt“-Anwendung.

(Sie ruft zu diesem Zweck die <xref:System.Console.WriteLine%2A>-Methode auf, um die literale Zeichenfolge „Hello World!“ im Konsolenfenster anzuzeigen.)

   ![Sehen Sie sich den Standardcode für „Hallo Welt“ in der Vorlage an](../ide/media/csharp-console-helloworld-template.png)

Wenn Sie **F5** drücken, wird das Programm im Debugmodus ausgeführt. Das Konsolenfenster öffnet sich nur für einen kurzen Moment, bevor es wieder geschlossen wird.

Der Grund dafür ist, dass die Methode `Main` beendet wird, nachdem ihre einzige Anweisung ausgeführt wird. Also wird die Anwendung geschlossen.

### <a name="add-some-code"></a>Hinzufügen von Code

Fügen Sie Code hinzu, um die Anwendung anzuhalten, damit das Konsolenfenster nicht geschlossen wird, bis Sie die **EINGABETASTE** gedrückt haben.

1. Fügen Sie direkt nach dem Aufruf der <xref:System.Console.WriteLine%2A>-Methode folgenden Code ein:

   ```csharp
   Console.ReadLine();
   ```

1. Überprüfen Sie, ob der Code im Code-Editor wie folgt aussieht:

   ![Hinzufügen von Code zum Anhalten der Hallo Welt-App](../ide/media/csharp-console-helloworld-add-code.png)

## <a name="run-the-application"></a>Ausführen der Anwendung

1. Wählen Sie auf der Symbolleiste die Schaltfläche **HelloWorld** aus, um die Anwendung im Debugmodus auszuführen. Alternativ können Sie **F5** drücken.

   ![Wählen Sie die Schaltfläche „Hello World“ aus, um die App von der Symbolleiste aus auszuführen](../ide/media/csharp-console-hello-world-button.png)

1. Zeigen Sie Ihre App im Konsolenfenster an.

   ![Konsolenfenster mit „Hello World!“](../ide/media/csharp-console-hello-world.png)

### <a name="close-the-application"></a>Schließen der Anwendung

1. Drücken Sie die **EINGABETASTE**, um das Konsolenfenster zu schließen.

1. Schließen Sie den Bereich **Output** (Ausgabe) in Visual Studio.

   ![Schließen des Ausgabebereichs in Visual Studio](../ide/media/csharp-hello-world-close-output-pane.png)

1. Schließen Sie Visual Studio.

## <a name="next-steps"></a>Nächste Schritte

Damit haben Sie den Schnellstart erfolgreich abgeschlossen. Wir hoffen, dass Sie mehr über C# und die Visual Studio-IDE erfahren konnten. Wenn Sie noch mehr lernen möchten, fahren Sie mit den folgenden Tutorials fort.

> [!div class="nextstepaction"]
> [Erste Schritte mit einer C#-Konsolen-App in Visual Studio](../get-started/csharp/tutorial-console.md)
