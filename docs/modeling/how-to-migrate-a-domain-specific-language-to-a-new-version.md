---
title: 'Vorgehensweise: Migrieren einer domänenspezifischen Sprache zu einer neuen Version'
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: c2ff1a820e5ac8492b627ac61ddfa234c71b5890
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54932336"
---
# <a name="how-to-migrate-a-domain-specific-language-to-a-new-version"></a>Vorgehensweise: Migrieren einer domänenspezifischen Sprache zu einer neuen Version
Sie können Projekte, die definieren, und Verwenden einer domänenspezifischen Sprache migrieren [!INCLUDE[vs2010](../misc/includes/vs2010_md.md)] von der Version der [!INCLUDE[dsl](../modeling/includes/dsl_md.md)] , die mit verteilt wurde [!INCLUDE[vs_orcas_long](../debugger/includes/vs_orcas_long_md.md)].

 Tool für die Migration erfolgt als Teil des [!INCLUDE[vssdk_current_long](../misc/includes/vssdk_current_long_md.md)]. Das Tool konvertiert die Visual Studio-Projekte und Projektmappen, die verwenden, oder definieren die DSL-Tools.

 Sie müssen das Migrationstool explizit ausführen: Es wird nicht automatisch gestartet, wenn Sie eine Projektmappe in Visual Studio öffnen. Dokument mit den Tools und detaillierte Anleitungen finden Sie unter folgendem Pfad:

 **%Program Files%\Microsoft Visual Studio 2010 SDK\VisualStudioIntegration\Tools\DSLTools\DslProjectsMigrationTool.exe**

## <a name="before-you-migrate-your-dsl-projects"></a>Vor dem Migrieren Sie Ihre DSL-Projekte
 Das Migrationstool, ändert Visual Studio-Projektdateien (**csproj**) und Projektmappendateien (**sln**).

#### <a name="to-prepare-projects-for-migration"></a>Um Projekte für die Migration vorzubereiten.

-   Stellen Sie sicher, dass die **csproj** und **sln** Dateien können geschrieben werden. Wenn sie sich unter quellcodeverwaltung sind, stellen Sie sicher, dass sie ausgecheckt sind.

-   Erstellen Sie eine Kopie der Ordner, die Sie migrieren möchten.

## <a name="migrating-a-collection-of-projects"></a>Migrieren Sie eine Sammlung von Projekten

#### <a name="to-migrate-dsl-projects-and-solutions-to-visual-studio-2010"></a>DSL-Projekte und Projektmappen in Visual Studio 2010 migrieren

1. Starten Sie das Migrationstool DSL.

   -   Sie können Doppelklicken Sie auf das Tool im Windows-Explorer (oder Datei-Explorer), oder Sie können das Tool an einer Eingabeaufforderung starten. Das Tool ist an diesem Speicherort:

        **%ProgramFiles%\Microsoft Visual Studio 2010 SDK\VisualStudioIntegration\Tools\DSLTools\DslProjectsMigrationTool.exe**

2. Wählen Sie einen Ordner mit Projektmappen und Projekte, die Sie konvertieren möchten.

   - Geben Sie den Pfad in das Feld am oberen Rand des Tools, oder klicken Sie auf **Durchsuchen**.

     Das Migrationstool zeigt eine Struktur von Projekten, die definieren, oder Verwenden von DSLs. Die Struktur enthält jedes Projekt, verwendet der **Microsoft.VisualStudio.Modeling.Sdk** oder **der TextTemplating** Assemblys.

3. Überprüfen Sie die Struktur von Projekten, und deaktivieren Sie die Projekte, die Sie nicht konvertieren möchten.

   -   Wählen Sie ein Projekt oder eine Lösung, um eine Liste der Änderungen anzuzeigen, die das Tool machen werden.

       > [!NOTE]
       >  Die Kontrollkästchen, die neben den Ordnernamen angezeigt werden, haben keine Auswirkungen. Erweitern Sie die Ordner, um die Projekte und Lösungen überprüfen.

4. Konvertieren Sie die Projekte an.

   1.  Klicken Sie auf **konvertieren**.

        Vor jede Projektdatei konvertiert wird, wird eine Kopie des _Projekt_**csproj** als gespeicherter _Projekt_**. vs2008.csproj**

        Eine Kopie aller _Lösung_**sln** als gespeicherter _Lösung_**. vs2008.sln**

   2.  Untersuchen Sie alle fehlerhaften Konvertierungen, die gemeldet werden.

        Fehler werden im Textfenster gemeldet. Darüber hinaus wird der Strukturansicht ein Warnsignal, das auf jedem Knoten, die konvertiert werden konnte. Sie können den Knoten, um weitere Informationen zu diesem Fehler erhalten, klicken.

5. **Alle Vorlagen transformieren** in Lösungen, die erfolgreich enthält Projekte konvertiert.

   1.  Öffnen Sie die Projektmappe.

   2.  Klicken Sie auf die **alle Vorlagen transformieren** Schaltfläche im Header des Projektmappen-Explorer.

       > [!NOTE]
       >  Sie können diesen Schritt nicht erforderlich machen. Weitere Informationen finden Sie unter [wie alle Vorlagen transformieren automatisieren](/previous-versions/visualstudio/visual-studio-2012/ff521399\(v\=vs.110\)).

6. Aktualisieren Sie Ihren benutzerdefinierten Code in die konvertierten Projekte ein.

   -   Versuchen Sie, erstellen Sie die Projekte, und untersuchen Sie alle Fehler.

   -   Testen Sie den Designer.


[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]

## <a name="see-also"></a>Siehe auch

- [Verwandte Blogbeiträge](https://blogs.msdn.microsoft.com/visualstudioalm/tag/code-index/)