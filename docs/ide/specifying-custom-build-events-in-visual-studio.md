---
title: Angeben benutzerdefinierter Buildereignisse
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- build events, customizing
ms.assetid: 69e935a5-e208-4bcd-865c-3e5f9b047ca8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 46bc4ed35538a0203938cd45a6fb160690212bef
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54996869"
---
# <a name="specify-custom-build-events-in-visual-studio"></a>Festlegen von benutzerdefinierten Buildereignissen in Visual Studio

Durch Angeben eines benutzerdefinierten Buildereignisses können Sie vor dem Starten oder nach dem Beenden eines Builds Befehle automatisch ausführen. Sie können beispielsweise eine *BAT-Datei* ausführen, bevor ein Build gestartet wird, oder neue Dateien in einen Ordner kopieren, nachdem der Build abgeschlossen wurde. Buildereignisse werden nur ausgeführt, wenn der Build die betreffenden Punkte im Buildprozess erfolgreich erreicht.

 Spezifische Informationen zu den verwendeten Programmiersprachen finden Sie in den folgenden Themen:

-   Visual Basic: [Vorgehensweise: Angeben von Buildereignissen (Visual Basic)](../ide/how-to-specify-build-events-visual-basic.md)

-   C# und F#: [Vorgehensweise: Angeben von Buildereignissen (C#)](../ide/how-to-specify-build-events-csharp.md)

-   Visual C++: [Festlegen von Buildereignissen](/cpp/ide/specifying-build-events).

## <a name="syntax"></a>Syntax

Buildereignisse folgen derselben Syntax wie DOS-Befehle, Sie können aber außerdem Makros verwenden, um die Erstellung zu erleichtern. Eine Liste der verfügbaren Makros finden Sie unter [Pre-build Event/Post-build Event command line dialog box (Dialogfelder „Befehlszeile für Präbuildereignis“ und „Befehlszeile für Postbuildereignis“)](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md).

 Um optimale Ergebnisse zu erhalten, befolgen Sie diese Tipps zur Formatierung:

- Fügen Sie allen Buildereignissen, die *BAT-Dateien* ausführen, eine `call`-Anweisung hinzu.

   Ein Beispiel: `call C:\MyFile.bat`

   Ein Beispiel: `call C:\MyFile.bat call C:\MyFile2.bat`

- Schließen Sie Dateipfade in Anführungszeichen ein.

   Beispiel (für [!INCLUDE[win8](../debugger/includes/win8_md.md)]): "%ProgramFiles(x86)%\Microsoft SDKs\Windows\v8.0A\Bin\NETFX 4.0 Tools\gacutil.exe" -if "$(TargetPath)"

- Trennen Sie mehrere Befehle durch Zeilenumbrüche.

- Verwenden Sie Platzhalterzeichen nach Bedarf.

   Beispiel: `for %I in (*.txt *.doc *.html) do copy %I c:\`*meinverzeichnis*`\`

  > [!NOTE]
  >  `%I` im oben abgebildeten Code sollte in Batchskripts zu `%%I` werden.

## <a name="see-also"></a>Siehe auch

- [Kompilieren und Erstellen](../ide/compiling-and-building-in-visual-studio.md)
- [Pre-build Event/Post-build Event command line dialog box (Dialogfelder „Befehlszeile für Präbuildereignis“ und „Befehlszeile für Postbuildereignis“)](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)
- [MSBuild-Sonderzeichen](../msbuild/msbuild-special-characters.md)
- [Exemplarische Vorgehensweise: Erstellen einer Anwendung](../ide/walkthrough-building-an-application.md)
