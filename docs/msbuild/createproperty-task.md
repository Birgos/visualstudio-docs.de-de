---
title: CreateProperty-Aufgabe | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#CreateProperty
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- CreateProperty task [MSBuild]
- MSBuild, CreateProperty task
ms.assetid: fbc31a88-62d4-43d2-b739-68ef3fac38f5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 684f55b4b660c48c4186755737b3bc64c6e62788
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55042672"
---
# <a name="createproperty-task"></a>CreateProperty-Aufgabe
Füllt Eigenschaften mit den übergebenen Werten auf. Dadurch können Werte aus einer Eigenschaft oder Zeichenfolge in eine andere kopiert werden.  

## <a name="attributes"></a>Attribute  
 In der folgenden Tabelle werden die Parameter der `CreateProperty` -Aufgabe beschrieben.  


| Parameter | Beschreibung |
|------------------| - |
| `Value` | Optionaler `String`-Ausgabeparameter.<br /><br /> Gibt den Wert an, der in die neue Eigenschaft kopiert werden soll |
| `ValueSetByTask` | Optionaler `String`-Ausgabeparameter.<br /><br /> Enthält denselben Wert wie der `Value`-Parameter. Verwenden Sie diesen Parameter nur, wenn die Ausgabeeigenschaft nicht von [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] festgelegt werden soll, wenn es das umschließende Ziel überspringt, weil die Ausgaben auf dem neuesten Stand sind. |

## <a name="remarks"></a>Hinweise  
 Zusätzlich zu den oben aufgeführten Parametern erbt diese Aufgabe Parameter von der <xref:Microsoft.Build.Tasks.TaskExtension>-Klasse, die selbst von der <xref:Microsoft.Build.Utilities.Task>-Klasse erbt. Eine Liste mit diesen zusätzlichen Parametern und ihren Beschreibungen finden Sie unter [TaskExtension-Basisklasse](../msbuild/taskextension-base-class.md).  

## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die `NewFile`-Eigenschaft mit der `CreateProperty`-Aufgabe und der Kombination der Werte der Eigenschaften `SourceFilename` und `SourceFileExtension` erstellt.  

```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  

    <PropertyGroup>  
        <SourceFilename>Module1</SourceFilename>  
        <SourceFileExtension>vb</SourceFileExtension>  
    </PropertyGroup>  

    <Target Name="CreateProperties">  

        <CreateProperty  
            Value="$(SourceFilename).$(SourceFileExtension)">  
            <Output  
                TaskParameter="Value"  
                PropertyName="NewFile" />  
        </CreateProperty>  

    </Target>  

</Project>  
```  

 Nach dem Ausführen des Projekts, ist der Wert der `NewFile`-Eigenschaft *Module1.vb*.  

## <a name="see-also"></a>Siehe auch  
 [Referenz zu MSBuild-Tasks](../msbuild/msbuild-task-reference.md)   
 [Aufgaben](../msbuild/msbuild-tasks.md)