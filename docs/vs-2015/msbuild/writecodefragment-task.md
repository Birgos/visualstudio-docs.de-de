---
title: WriteCodeFragment-Aufgabe | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, WriteCodeFragment task
- WriteCodeFragment task [MSBuild]
ms.assetid: 1d2514b4-5bef-43bb-bebe-496da8ef063c
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ee0b819d0387ecbd0bec3a460bf3c63d3122b269
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54796940"
---
# <a name="writecodefragment-task"></a>WriteCodeFragment-Aufgabe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Generiert eine temporäre Codedatei aus dem angegebenen generierten Codefragment. Die Datei wird nicht gelöscht.  
  
## <a name="parameters"></a>Parameter  
 In der folgenden Tabelle werden die Parameter der `WriteCodeFragment` -Aufgabe beschrieben.  
  
|Parameter|Beschreibung|  
|---------------|-----------------|  
|`AssemblyAttributes`|Optionaler <xref:Microsoft.Build.Framework.ITaskItem>`[]`-Parameter<br /><br /> Beschreibung der Attribute, die geschrieben werden sollen. Der Wert des Elements `Include` ist der vollständige Typname des Attributs, z.B. „System.AssemblyVersionAttribute“.<br /><br /> Jeder Metadatentyp stellt das Name/Wert-Paar eines Parameters dar, der dem Typ `String` entsprechen muss. Einige Attribute lassen nur positionelle Konstruktorargumente zu. Sie können solche Argumente allerdings in jedem Attribut verwenden. Um positionelle Konstruktorattribute festzulegen, verwenden Sie Metadatennamen, die „_Parameter1“, „_Parameter2“ usw. ähneln.<br /><br /> Ein Parameterindex kann nicht übersprungen werden.|  
|`Language`|Erforderlicher `String` -Parameter.<br /><br /> Gibt die Programmiersprache des zu generierenden Codes an.<br /><br /> `Language` kann jede Sprache sein, für die ein CodeDom-Anbieter verfügbar ist. Dies ist z.B. für „C#“ oder „VisualBasic“ der Fall. Die ausgegebene Datei verfügt dann über das standardmäßige Suffix für diese Sprache.|  
|`OutputDirectory`|Optionaler <xref:Microsoft.Build.Framework.ITaskItem> -Parameter.<br /><br /> Gibt den Zielordner für den generierten Code an. In der Regel ist dies der Zwischenordner.|  
|`OutputFile`|Optionaler <xref:Microsoft.Build.Framework.ITaskItem>-Ausgabeparameter.<br /><br /> Gibt den Pfad der Datei an, die generiert wurde. Wenn dieser Parameter mithilfe eines Dateinamens festgelegt wird, wird dem Dateinamen der Zielordner vorangestellt. Wenn er mit einem Stamm festgelegt wird, wird der Zielordner ignoriert.<br /><br /> Wenn dieser Parameter nicht festgelegt wird, ist der Name der Ausgabedatei der Zielordner, eine willkürliche Datei und das standardmäßige Suffix für die angegebene Sprache.|  
  
## <a name="remarks"></a>Hinweise  
 Zusätzlich zu den in der Tabelle aufgeführten Parametern erbt dieser Task Parameter von der <xref:Microsoft.Build.Tasks.TaskExtension>-Klasse, die selbst von der <xref:Microsoft.Build.Utilities.Task>-Klasse erbt. Eine Liste mit diesen zusätzlichen Parametern und ihren Beschreibungen finden Sie unter [TaskExtension Base Class](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Tasks (Aufgaben)](../msbuild/msbuild-tasks.md)   
 [Aufgabenreferenz](../msbuild/msbuild-task-reference.md)
