---
title: 'CA1050: Typen in Namespaces deklarieren.'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1050
- DeclareTypesInNamespaces
helpviewer_keywords:
- DeclareTypesInNamespaces
- CA1050
ms.assetid: 1002748d-ac8d-404f-85dd-7a12d1ad3e05
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 97cc36e7b454484f4fcdfb3d3be499e48af9c407
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55018838"
---
# <a name="ca1050-declare-types-in-namespaces"></a>CA1050: Typen in Namespaces deklarieren.

|||
|-|-|
|TypeName|DeclareTypesInNamespaces|
|CheckId|CA1050|
|Kategorie|Microsoft.Design|
|Unterbrechende Änderung|Breaking|

## <a name="cause"></a>Ursache
 Ein öffentlicher oder geschützter Typ ist außerhalb des Bereichs eines benannten Namespaces definiert.

## <a name="rule-description"></a>Regelbeschreibung
 Typen werden in Namespaces, um Namenskonflikte zu verhindern und als eine Möglichkeit zum Organisieren verwandter Typen in einer Objekthierarchie deklariert. Typen, die außerhalb eines benannten Namespaces sind in einem globalen Namespace, der nicht im Code verwiesen werden kann.

## <a name="how-to-fix-violations"></a>Behandeln von Verstößen
 Um einen Verstoß gegen diese Regel zu beheben, platzieren Sie den Typ in einem Namespace.

## <a name="when-to-suppress-warnings"></a>Wenn Sie Warnungen unterdrücken
 Obwohl Sie nie eine Warnung dieser Regel unterdrücken verfügen, ist es sicher ist, die dies tun, wenn die Assembly nicht zusammen mit anderen Assemblys verwendet werden soll.

## <a name="example"></a>Beispiel
 Das folgende Beispiel zeigt eine Bibliothek, die ein Typ, der falsch außerhalb eines Namespaces deklariert hat, und ein Typ, der den gleichen Namen, die in einem Namespace deklariert hat.

 [!code-csharp[FxCop.Design.TypesLiveInNamespaces#1](../code-quality/codesnippet/CSharp/ca1050-declare-types-in-namespaces_1.cs)]
 [!code-vb[FxCop.Design.TypesLiveInNamespaces#1](../code-quality/codesnippet/VisualBasic/ca1050-declare-types-in-namespaces_1.vb)]

## <a name="example"></a>Beispiel
 Die folgende Anwendung verwendet die Bibliothek, die zuvor definiert wurde. Beachten Sie, dass der Typ, der außerhalb eines Namespace deklariert wird, wenn erstellt wird der Name `Test` wird nicht durch einen Namespace gekennzeichnet. Beachten Sie außerdem, den Zugriff auf die `Test` geben `Goodspace`, der Namespacename ist erforderlich.

 [!code-csharp[FxCop.Design.TestTypesLive#1](../code-quality/codesnippet/CSharp/ca1050-declare-types-in-namespaces_2.cs)]
 [!code-vb[FxCop.Design.TestTypesLive#1](../code-quality/codesnippet/VisualBasic/ca1050-declare-types-in-namespaces_2.vb)]