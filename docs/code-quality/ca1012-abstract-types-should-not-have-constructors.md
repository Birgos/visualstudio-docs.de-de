---
title: 'CA1012: Abstrakte Typen dürfen keine Konstruktoren aufweisen.'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- AbstractTypesShouldNotHaveConstructors
- CA1012
helpviewer_keywords:
- CA1012
ms.assetid: 09f458ac-dd88-4cd7-a47f-4106c1e80ece
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: dd35cd7b084deb34b23b49ebc04517733c5478c9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006779"
---
# <a name="ca1012-abstract-types-should-not-have-constructors"></a>CA1012: Abstrakte Typen dürfen keine Konstruktoren aufweisen.

|||
|-|-|
|TypeName|AbstractTypesShouldNotHaveConstructors|
|CheckId|CA1012|
|Kategorie|Microsoft.Design|
|Unterbrechende Änderung|Nicht unterbrechend|

## <a name="cause"></a>Ursache
 Ein öffentlicher Typ ist abstrakt und verfügt über einen öffentlichen Konstruktor.

## <a name="rule-description"></a>Regelbeschreibung
 Konstruktoren von abstrakten Datentypen können nur von abgeleiteten Typen aufgerufen werden. Da öffentliche Konstruktoren Instanzen eines Typs erstellen und Sie keine Instanzen eines abstrakten Datentyps erstellen können, ist ein abstrakter Datentyp mit einem öffentlichen Konstruktor fehlerhaft konzipiert.

## <a name="how-to-fix-violations"></a>Behandeln von Verstößen
 Um einen Verstoß gegen diese Regel zu beheben, dass der geschützte Konstruktor oder den Typ als abstrakt nicht deklarieren.

## <a name="when-to-suppress-warnings"></a>Wenn Sie Warnungen unterdrücken
 Unterdrücken Sie keine Warnung dieser Regel. Der abstrakte Typ verfügt über einen öffentlichen Konstruktor.

## <a name="example"></a>Beispiel
 Das folgende Beispiel enthält einen abstrakten Typ, der gegen diese Regel verstößt.

 [!code-vb[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_1.vb)]
 [!code-csharp[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_1.cs)]

## <a name="example"></a>Beispiel
 Im folgende Beispiel wird der vorherige Verstoß korrigiert, ändern Sie den Zugriff auf den Konstruktor von `public` zu `protected`.

 [!code-csharp[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_2.cs)]
 [!code-vb[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_2.vb)]