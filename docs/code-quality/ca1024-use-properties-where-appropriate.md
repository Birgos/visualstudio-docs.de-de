---
title: 'CA1024: Nach Möglichkeit Eigenschaften verwenden.'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- UsePropertiesWhereAppropriate
- CA1024
helpviewer_keywords:
- CA1024
- UsePropertiesWhereAppropriate
ms.assetid: 3a04f765-af7c-4872-87ad-9cc29e8e657f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 0cc51a046e2b02375f719d5407c2cbaf714dc78c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54984365"
---
# <a name="ca1024-use-properties-where-appropriate"></a>CA1024: Nach Möglichkeit Eigenschaften verwenden.

|||
|-|-|
|TypeName|UsePropertiesWhereAppropriate|
|CheckId|CA1024|
|Kategorie|Microsoft.Design|
|Unterbrechende Änderung|Breaking|

## <a name="cause"></a>Ursache

Eine öffentliche oder geschützte Methode hat einen Namen, die mit beginnt `Get`nimmt keine Parameter und gibt einen Wert, der kein Array ist.

## <a name="rule-description"></a>Regelbeschreibung

Klicken Sie in den meisten Fällen Eigenschaften Daten darstellen, und Methoden Aktionen ausführen. Eigenschaften sind zugegriffen, wie Felder, wodurch sie einfacher zu verwenden. Eine Methode ist, eignet sich für eine Eigenschaft zu werden, wenn eine der folgenden Bedingungen vorliegt:

- Akzeptiert keine Argumente und gibt Informationen über den Zustand eines Objekts.

- Akzeptiert ein einzelnes Argument um einen Teil des Zustands eines Objekts festzulegen.

Eigenschaften sollten Verhalten, als wären sie Felder. Wenn die Methode nicht möglich ist, sollten sie nicht auf eine Eigenschaft geändert werden. Methoden sind besser als Eigenschaften in den folgenden Situationen:

- Die Methode ausführt einen zeitaufwändigen Vorgang. Die Methode ist als die Zeit, die erforderlich sind, um festzulegen, oder rufen Sie den Wert eines Felds beansprucht.

- Die Methode führt eine Konvertierung aus. Zugreifen auf ein Feld gibt keine konvertierte Version der Daten zurück, die sie speichert.

- Die Get-Methode hat es sich um ein Observable Nebeneffekt. Abrufen des Werts eines Felds ergibt keinen keine Nebeneffekte.

- Die Reihenfolge der Ausführung ist wichtig. Festlegen des Werts eines Felds beruht nicht auf das Vorhandensein anderer Vorgänge.

- Aufrufen der Methode zweimal hintereinander führt zu unterschiedlichen Ergebnissen.

- Die Methode ist statisch, aber es gibt ein Objekt, das vom Aufrufer geändert werden kann. Abrufen des Werts eines Felds lässt nicht den Aufrufer so ändern Sie die Daten, die nach dem Feld gespeichert wird.

- Die Methode gibt ein Array zurück.

## <a name="how-to-fix-violations"></a>Behandeln von Verstößen

Um einen Verstoß gegen diese Regel zu beheben, ändern Sie die Methode einer Eigenschaft ein.

## <a name="when-to-suppress-warnings"></a>Wenn Sie Warnungen unterdrücken

Unterdrücken Sie eine Warnung dieser Regel, wenn die Methode, die mindestens eines der zuvor aufgeführten Kriterien erfüllt.

## <a name="controlling-property-expansion-in-the-debugger"></a>Steuern des Eigenschaft-Erweiterung im Debugger

Ein Grund, dass Programmierer vermeiden, verwenden eine Eigenschaft ist, da sie nicht, dass den Debugger automatisch erweitert möchten. Beispielsweise die Eigenschaft wird eventuell ein großes Objekt zuweisen oder P/Invoke aufrufen, aber es möglicherweise nicht tatsächlich keine Observable Nebeneffekte.

Sie können verhindern, dass den Debugger automatisch erweitert Eigenschaften durch Anwenden von <xref:System.Diagnostics.DebuggerBrowsableAttribute?displayProperty=fullName>. Das folgende Beispiel zeigt dieses Attribut auf eine Instance-Eigenschaft angewendet wird.

```vb
Imports System
Imports System.Diagnostics

Namespace Microsoft.Samples

    Public Class TestClass

        ' [...]

        <DebuggerBrowsable(DebuggerBrowsableState.Never)> _
        Public ReadOnly Property LargeObject() As LargeObject
            Get
                ' Allocate large object
                ' [...]
            End Get
        End Property

    End Class

End Namespace
```

```csharp
using System;
using System.Diagnostics;

namespace Microsoft.Samples
{
    publicclass TestClass
    {
        // [...]

        [DebuggerBrowsable(DebuggerBrowsableState.Never)]
        public LargeObject LargeObject
        {
            get
            {
                // Allocate large object
                // [...]
            }
        }
    }
}
```

## <a name="example"></a>Beispiel

Das folgende Beispiel enthält mehrere Methoden, Eigenschaften konvertiert werden sollen, und mehrere Funktionen, sollte nicht verwendet werden, weil sie nicht wie Felder Verhalten.

[!code-csharp[FxCop.Design.MethodsProperties#1](../code-quality/codesnippet/CSharp/ca1024-use-properties-where-appropriate_1.cs)]