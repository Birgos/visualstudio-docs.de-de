---
title: Verwenden des Managed Package Framework für einen Projekttyp (c#) | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], creating with MPF
- MPF projects
- managed package framework, creating projects
ms.assetid: 926de536-eead-415b-9451-f1ddc8c44630
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e82bf87d946c7aa5fcf9ad23185782563325c7c1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55017331"
---
# <a name="using-the-managed-package-framework-to-implement-a-project-type-c"></a>Verwenden des Managed Package Framework zum Implementieren eines Projekttyps (C#)
Das Managed Package Framework (MPF) stellt die Klassen in c#, die können Sie verwenden oder erben, implementieren Sie eigene Projekttypen, bereit. Das MPF implementiert viele der Schnittstellen, die Visual Studio ein Projekt bereitgestellt werden, erwartet, dadurch können Sie die Konzentration auf die Einzelheiten der Art Ihres Projekts implementieren.  
  
## <a name="using-the-mpf-project-source-code"></a>Verwenden den Quellcode des MPF-Projekts  
 Das Managed Package Framework for Projects (MPFProj) stellt Hilfsklassen zum Erstellen und Verwalten von neuen Projektsystem bereit. Im Gegensatz zu anderen Klassen in das MPF sind die Projektklassen in den Assemblys, die im Lieferumfang von Visual Studio nicht enthalten. Stattdessen werden die Projektklassen bereitgestellt, als Quellcode auf [MPF für Projekte 2013](https://github.com/tunnelvisionlabs/MPFProj10).  
  
 Um Ihre VSPackage-Projektmappe das Projekt hinzuzufügen, führen Sie folgende Schritte aus:  
  
1.  Herunterladen der Dateien MPFProj, *MPFProjectDir*.  
  
2.  In der *MPFProjectDir*\Dev10\Src\CSharp\ProjectBase.file, ändern Sie den folgenden Block:  
  
```  
<!-- Provide a default value for $(ProjectBasePath) -->  
  <PropertyGroup>  
    <ProjectBasePath >MPFProjDir\Dev10\Src\CSharp</ProjectBasePath>  
  </PropertyGroup>  
```  
  
1.  Erstellen Sie ein VSPackage-Projekt.  
  
2.  Entladen Sie das VSPackage-Projekt.  
  
3.  Bearbeiten Sie die VSPackage-CSPROJ-Datei durch Hinzufügen des folgenden Blocks vor den anderen `<Import>` Blöcken:  
  
```  
<Import Project="MPFProjectDir\Dev10\Src\CSharp\ProjectBase.files" />  
  <PropertyGroup>  
    <!--To specify a different registry root to register your package, uncomment the TargetRegistryRoot tag and specify a registry root in it.  
    <TargetRegistryRoot></TargetRegistryRoot>-->  
    <RegisterOutputPackage>true</RegisterOutputPackage>  
    <RegisterWithCodebase>true</RegisterWithCodebase>  
  </PropertyGroup>  
```  
  
1.  Speichern Sie das Projekt.  
  
2.  Schließen Sie und öffnen Sie die VSPackage-Projektmappe.  
  
3.  Öffnen Sie erneut das VSPackage-Projekt. Ein neues Verzeichnis namens ProjectBase sollte angezeigt werden.  
  
4.  Fügen Sie den folgenden Verweis auf das VSPackage-Projekt hinzu:  
  
     Microsoft.Build.Tasks.4.0  
  
5.  Erstellen Sie das Projekt.  
  
## <a name="hierarchy-classes"></a>Hierarchie-Klassen  
 Die folgende Tabelle enthält die Klassen in der MPFProj, die projekthierarchien zu unterstützen. Weitere Informationen finden Sie unter [Hierarchien und Auswahl](../../extensibility/internals/hierarchies-and-selection.md).  
  
|Klassenname|  
|----------------|  
|`Microsoft.VisualStudio.Package.HierarchyNode`|  
|`Microsoft.VisualStudio.Package.ProjectNode`|  
|`Microsoft.VisualStudio.Package.ProjectContainerNode`|  
|`Microsoft.VisualStudio.Package.FileNode`|  
|`Microsoft.VisualStudio.Package.FolderNode`|  
|`Microsoft.VisualStudio.Package.ReferenceContainerNode`|  
|`Microsoft.VisualStudio.Package.ReferenceNode`|  
|`Microsoft.VisualStudio.Package.ProjectReferenceNode`|  
|`Microsoft.VisualStudio.Package.ComReferenceNode`|  
|`Microsoft.VisualStudio.Package.AssemblyReferenceNode`|  
|`Microsoft.VisualStudio.Package.BuildDependency`|  
  
## <a name="document-handling-classes"></a>Handhabung Klassen  
 Die folgende Tabelle enthält die Klassen in das MPF, Dokumenten zu unterstützen. Weitere Informationen finden Sie unter [öffnen und Speichern von Projektelementen](../../extensibility/internals/opening-and-saving-project-items.md).  
  
|Klassenname|  
|----------------|  
|`Microsoft.VisualStudio.Package.DocumentManager`|  
|`Microsoft.VisualStudio.Package.FileDocumentManager`|  
  
## <a name="configuration-and-output-classes"></a>Konfiguration und Klassen für die Ausgabe  
 Die folgende Tabelle enthält die Klassen in das MPF, mit denen unterstützt mehrere Konfigurationen, z.B. Debug und Release und Auflistungen der Projektausgabe Projekttypen zur Verfügung. Weitere Informationen finden Sie unter [Konfigurationsoptionen verwalten](../../extensibility/internals/managing-configuration-options.md).  
  
|Klassenname|  
|----------------|  
|`Microsoft.VisualStudio.Package.ConfigProvider`|  
|`Microsoft.VisualStudio.Package.ProjectConfig`|  
|`Microsoft.VisualStudio.Package.BuildableProjectConfig`|  
|`Microsoft.VisualStudio.Package.OutputGroup`|  
|`Microsoft.VisualStudio.Package.ProjectElement`|  
  
## <a name="automation-support-classes"></a>Automatisierungsunterstützung Klassen  
 Die folgende Tabelle enthält die Klassen in das MPF, die die Automatisierung unterstützen, damit Benutzer von Ihren Projekttyp-add-ins schreiben können.  
  
|Klassenname|  
|----------------|  
|`Microsoft.VisualStudio.Package.Automation.OAProject`|  
|`Microsoft.VisualStudio.Package.Automation.OANavigableProjectItems`|  
|`Microsoft.VisualStudio.Package.Automation.OAProjectItems`|  
|`Microsoft.VisualStudio.Package.Automation.OAProjectItem`|  
|`Microsoft.VisualStudio.Package.Automation.OANestedProjectItem`|  
  
## <a name="properties-classes"></a>Eigenschaften von Klassen  
 Die folgende Tabelle enthält hinzufügen die Klassen in das MPF, mit denen Projekttypen können Eigenschaften, die Benutzer durchsuchen und in einem Eigenschaftenbrowser ändern können.  
  
|Klassenname|  
|----------------|  
|`Microsoft.VisualStudio.Package.LocalizableProperties`|  
|`Microsoft.VisualStudio.Package.NodeProperties`|  
|`Microsoft.VisualStudio.Package.FileNodeProperties`|  
|`Microsoft.VisualStudio.Package.ProjectNodeProperties`|  
|`Microsoft.VisualStudio.Package.FolderNodeProperties`|  
|`Microsoft.VisualStudio.Package.ReferenceNodeProperties`|