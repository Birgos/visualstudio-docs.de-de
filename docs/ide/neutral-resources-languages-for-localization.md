---
title: Neutrale Ressourcensprachen für die Lokalisierung
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- localization [Visual Studio], resources
- NeutralResourcesLanguageAttribute class
- globalization [Visual Studio], resources
- resources [Visual Studio], fallback system
- culture, locating resources
- neutral resources
ms.assetid: ef064995-3b84-4698-a708-9689b7723533
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 513cd8295a3e25a171de6623ba706ce7dfb2a2e6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962104"
---
# <a name="neutral-resources-languages-for-localization"></a>Neutrale Ressourcensprachen für die Lokalisierung

Die Klasse <xref:System.Resources.NeutralResourcesLanguageAttribute> gibt die Kultur der Ressourcen an, die in der Hauptassembly enthalten sind. Mit diesem Attribut wird die Leistung optimiert, sodass das <xref:System.Resources.ResourceManager>-Objekt nicht nach Ressourcen sucht, die in der Hauptassembly enthalten sind.

 Im folgenden Codebeispiel wird veranschaulicht, wie neutrale Sprachressourcen festgelegt werden. Der Code kann in ein Buildskript, die AssemblyInfo.vb-Datei oder die AssemblyInfo.cs-Datei eingefügt werden.

```vb
' Set neutral resources language for assembly.
<Assembly: NeutralResourcesLanguageAttribute("en")>
```

```csharp
// Set neutral resources language for assembly.
[assembly: NeutralResourcesLanguageAttribute("en")]
```

## <a name="see-also"></a>Siehe auch

- <xref:System.Resources.ResourceManager>
- [Einführung in internationale Anwendungen basierend auf .NET Framework](../ide/introduction-to-international-applications-based-on-the-dotnet-framework.md)
- [Hierarchische Organisation der Ressourcen für die Lokalisierung](../ide/hierarchical-organization-of-resources-for-localization.md)
- [Lokalisieren von Anwendungen](../ide/localizing-applications.md)
- [Globalisieren und Lokalisieren von Anwendungen](../ide/globalizing-and-localizing-applications.md)