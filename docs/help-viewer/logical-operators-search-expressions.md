---
title: Logische und erweiterte Operatoren in Suchausdrücken (Help Viewer)
ms.date: 11/02/2017
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Help Viewer, logical operators in search
- logical operators in search [Help Viewer]
ms.assetid: 0c38ae7d-3e20-4d47-a020-9677cd285916
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 827977f2763eff209e400538262b511a2124a1f9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54956193"
---
# <a name="logical-and-advanced-operators-in-search-expressions"></a>Logische und erweiterte Operatoren in Suchausdrücken

Sie können Ihre Suche im Hilfe-Inhalt in **Help Viewer** mit logischen Operatoren und erweiterten Suchoperatoren optimieren.

## <a name="logical-operators"></a>Logische Operatoren

Mit logischen Operatoren können Sie angeben, wie viele Suchausdrücke in einer Suchabfrage kombiniert werden sollen. In der folgenden Tabelle werden die logischen Operatoren AND, OR, NOT und NEAR veranschaulicht.

|Suchen nach|Verwendung|Beispiel|Ergebnis|
|-------------------|---------|-------------|------------|
|Beide Begriffe im gleichen Artikel|UND|dib UND palette|Themen, die sowohl „Dib“ als auch „Palette“ enthalten.|
|Einer der Begriffe in einem Artikel|ODER|Raster ODER Vektor|Themen, die entweder „Raster“ oder „Vektor“ enthalten.|
|Erster Begriff ohne den zweiten Begriff im gleichen Artikel|NICHT|„Betriebssystem“ NICHT DOS|Themen, die „Betriebssystem“ aber nicht „DOS“ enthalten.|
|Beide Begriffe nah beieinander in einem Artikel|NAH|Benutzer NAH Kernel|Themen mit „Benutzer“ in der Nähe von „Kernel“.|

> [!IMPORTANT]
> Sie müssen logische Operatoren in Großbuchstaben eingeben, damit sie von der Suchmaschine erkannt werden.

## <a name="advanced-operators"></a>Erweiterte Operatoren

Mit erweiterten Suchoperatoren können Sie Ihre Suche nach Inhalt optimieren, indem Sie festlegen, in welchem Bereich des Artikels nach dem Suchbegriff gesucht werden soll. In der folgenden Tabelle werden die vier verfügbaren erweiterten Suchoperatoren veranschaulicht.

|Suchen nach|Verwendung|Beispiel|Ergebnis|
|-------------------|---------|-------------|------------|
|Ein Begriff im Titel des Artikels|`title:`|`title:binaryreader`|Themen, die „Binaryreader“ im Titel enthalten.|
|Eine Benennung in einem Codebeispiel|`code:`|`code:readdouble`|Themen, die „readdouble“ in einem Codebeispiel enthalten.|
|Eine Benennung in einem Beispiel einer spezifischen Programmiersprache|`code:vb:`|`code:vb:string`|Themen, die „string“ in einem Visual Basic-Codebeispiel enthalten.|
|Ein Artikel, der einem bestimmten Indexschlüsselwort zugeordnet ist|`keyword:`|`keyword:readbyte`|Themen, die dem Index-Schlüsselwort „readbyte“ zugeordnet sind.|

> [!IMPORTANT]
> Sie müssen erweiterte Suchoperatoren mit einem abschließenden Doppelpunkt eingeben. Es dürfen sich keine Leerzeichen zwischen dem Suchoperator und dem Doppelpunkt befinden, damit die Suchmaschine diesen erkennen kann.

### <a name="programming-languages-for-code-examples"></a>Programmiersprachen für Codebeispiele

Mit dem Operator `code:` können Sie nach Inhalt von einer der Programmiersprachen suchen. Verwenden Sie einen der folgenden Programmiersprachenwerte, um Beispiele für eine bestimmte Programmiersprache zurückzugeben:

|Programmiersprache|Suchoperatorsyntax|
| - |---------|
|Visual Basic|`code:vb`<br/>`code:visualbasic`|
|C#|`code:c#`<br/>`code:csharp`|
|C++|`code:cpp`<br/>`code:c++`<br/>`code:cplusplus`|
|F#|`code:f#`<br/>`code:fsharp`|
|JavaScript|`code:javascript`<br/>`code:js`|
|XAML|`code:xaml`|

> [!NOTE]
> Der Operator `code:` findet nur Inhalt, der mit einem Programmiersprachenbezeichner markiert ist, und keinen Inhalt, der generisch als Code markiert ist.

## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Search for topics (Vorgehensweise: Suchen von Themen)](../help-viewer/find-topics.md)
- [Microsoft Help Viewer](../help-viewer/overview.md)
