---
title: Hinzufügen von Namensparametern zu Projekt- und Elementvorlagen
ms.date: 01/02/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- template parameters
- template parameters, substituting
- Visual Studio templates, using parameters
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 93e553338478bcdead9e283323348b02ac73eaac
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55031759"
---
# <a name="how-to-substitute-parameters-in-a-template"></a>Vorgehensweise: Ersetzen von Parametern in einer Vorlage

Mithilfe von Vorlagenparametern können Sie Bezeichner wie Klassennamen und Namespaces ersetzen, wenn Sie eine Datei auf Basis einer Vorlage erstellen. Sie können Vorlagenparameter zu vorhandenen Vorlagen hinzufügen oder Ihre eigene Vorlage mithilfe von Vorlagenparametern erstellen.

Vorlagenparameter werden im Format $*Parameter*$ geschrieben. Eine vollständige Liste der Vorlagenparameter finden Sie unter [Vorlagenparameter](../ide/template-parameters.md).

Im folgenden Abschnitt wird erläutert, wie Sie eine Vorlage ändern, um den Namen eines Namespaces durch den „sicheren Projektnamen“ zu ersetzen.

## <a name="to-use-a-parameter-to-replace-the-namespace-name"></a>Verwenden eines Parameters, um einen Namespacenamen zu ersetzen

1. Fügen Sie den Parameter in eine oder mehrere Codedateien in der Vorlage ein. Beispiel:

    ```csharp
    namespace $safeprojectname$
    ```

1. Suchen Sie in der *VSTEMPLATE*-Datei der Vorlage nach dem `ProjectItem`-Element, in dem diese Datei enthalten ist.

1. Legen Sie das `ReplaceParameters`-Attribut für das `ProjectItem`-Element auf `true` fest:

    ```xml
    <ProjectItem ReplaceParameters="true">Class1.cs</ProjectItem>
    ```

## <a name="see-also"></a>Siehe auch

- [Erstellen von Projekt- und Elementvorlagen](../ide/creating-project-and-item-templates.md)
- [Vorlagenparameter](../ide/template-parameters.md)
- [Schemareferenz zu Visual Studio-Vorlagen](../extensibility/visual-studio-template-schema-reference.md)
- [ProjectItem-Element (Visual Studio-Projektelementvorlagen)](../extensibility/projectitem-element-visual-studio-item-templates.md)