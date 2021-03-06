---
title: 'Vorgehensweise: Ändern des Buildausgabeverzeichnisses'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- output directory, changing
ms.assetid: a8333c89-afb2-4b1d-b2e2-9146da852402
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e74dfb3c9a5e5ccd4a1e61e15a12991433032e6e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54989509"
---
# <a name="how-to-change-the-build-output-directory"></a>Vorgehensweise: Ändern des Buildausgabeverzeichnisses

Sie können den Speicherort der vom das Projekt generierten Ausgabe auf Basis der Konfiguration („Debug“, „Release“ oder beides) angeben.

> [!NOTE]
> Wenn Sie über ein **Setup**-Projekt verfügen, beachten Sie den Hinweis am Ende dieses Artikels.

## <a name="change-the-build-output-directory"></a>Ändern des Buildausgabeverzeichnisses

1.  Wählen Sie in der Menüleiste **Projekt** > **\<App-Name> Eigenschaften** aus. Klicken Sie im **Projektmappen-Explorer** erst mit der rechten Maustaste auf den Projektknoten und anschließend mit der Linken auf **Eigenschaften**.

2.  Wenn Sie ein Visual Basic-Projekt haben, wählen Sie die Registerkarte **Kompilieren** . Wenn Sie ein C#-Projekt haben, wählen Sie die Registerkarte **Build** aus. Wenn Sie ein C++-Projekt oder ein JavaScript-Projekt haben, wählen Sie die Registerkarte **Allgemein** .

3.  Wählen Sie in der Konfigurationen-Dropdownliste am oberen Rand die Konfiguration aus, deren Speicherort der Ausgabedatei Sie ändern möchten („Debug“, „Release“ oder beides).

     Suchen Sie den Eintrag des Ausgabepfads (**Buildausgabepfad** in Visual Basic **Ausgabeverzeichnis** in Visual C++, **Ausgabepfad** in JavaScript und C#). Geben Sie ein neues Buildausgabeverzeichnis relativ zum Projektverzeichnis an.

> [!NOTE]
> In einem Setup-Projekt wird durch das Feld **Ausgabedateiname** lediglich der Speicherort der Datei *Setup.exe* und nicht der Speicherort der Projektdateien geändert. Weitere Informationen finden Sie unter **Build, Configuration Properties, Deployment Project Properties dialog box (Dialogfelder „Erstellen“, „Konfigurationseigenschaften“ und „Bereitstellungsprojekteigenschaften“)**.

## <a name="see-also"></a>Siehe auch

- [Seite „Erstellen“, Projekt-Designer (C#)](../ide/reference/build-page-project-designer-csharp.md)
- [Allgemeine Eigenschaftenseite (Projekt)](/cpp/ide/general-property-page-project)
- [Kompilieren und Erstellen](../ide/compiling-and-building-in-visual-studio.md)