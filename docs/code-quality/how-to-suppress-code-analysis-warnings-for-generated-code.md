---
title: 'Vorgehensweise: Unterdrücken von Codeanalysewarnungen für generierten Code'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 3a96434e-d419-43a7-81ba-95cccac835b8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9c6628692014cd495490384e8a707c23fdcb3bde
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55012949"
---
# <a name="how-to-suppress-code-analysis-warnings-for-generated-code"></a>Vorgehensweise: Unterdrücken von Codeanalysewarnungen für generierten Code
Compiler für verwalteten Code generieren häufig Code, der ein Projekt aus, um die schnelle Codeentwicklung zu vereinfachen hinzugefügt wird. Darüber hinaus verwenden Entwickler häufig Drittanbieter-Tools ab, um schnell Anwendungen zu entwickeln. Diese Tools generieren auch Code, der dem Projekt hinzugefügt wird.

 Sie möchten die Verletzungen angezeigt, die Codeanalyse in generiertem Code ermittelt. Möglicherweise möchten Sie nicht angezeigt, wenn Sie nicht anzeigen und verwalten den Code, der den Verstoß enthält.

 Die **Ergebnisse aus generiertem Code unterdrücken** Kontrollkästchen auf der Eigenschaftenseite "Codeanalyse" eines Projekts können Sie auswählen, ob codeanalysewarnungen aus von einem Drittanbieter-Tool generierten Code angezeigt werden sollen.

> [!NOTE]
>  Diese Option unterdrücken, wenn die Fehler und Warnungen in Formularen und Vorlagen werden keine Codeanalysefehler und-Warnungen zu generiertem Code. Der Quellcode für ein Formular oder eine Vorlage kann sowohl angezeigt als auch verwaltet werden.

### <a name="to-suppress-warnings-for-generated-code-in-a-project"></a>So unterdrücken Sie Warnungen für generierten Code in einem Projekt

1.  Mit der rechten Maustaste in des Projekts im Projektmappen-Explorer, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie auf **Codeanalyse**.

3.  Wählen Sie die **Ergebnisse aus generiertem Code unterdrücken** Kontrollkästchen.