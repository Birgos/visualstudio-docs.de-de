---
title: 'CA1049: Typen, die native Ressourcen besitzen, müssen gelöscht werden können.'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1049
- TypesThatOwnNativeResourcesShouldBeDisposable
helpviewer_keywords:
- TypesThatOwnNativeResourcesShouldBeDisposable
- CA1049
ms.assetid: 084e587d-0e45-4092-b767-49eed30d6a35
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- cplusplus
ms.openlocfilehash: 37bd88e00ed8663be974bbc6ba78d5ce3ae45662
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54960268"
---
# <a name="ca1049-types-that-own-native-resources-should-be-disposable"></a>CA1049: Typen, die native Ressourcen besitzen, müssen gelöscht werden können.

|||
|-|-|
|TypeName|TypesThatOwnNativeResourcesShouldBeDisposable|
|CheckId|CA1049|
|Kategorie|Microsoft.Design|
|Unterbrechende Änderung|Nicht unterbrechend|

## <a name="cause"></a>Ursache

Auf einen Typ verweist eine <xref:System.IntPtr?displayProperty=fullName> Feld eine <xref:System.UIntPtr?displayProperty=fullName> Feld oder eine <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName> Feld, implementiert aber nicht <xref:System.IDisposable?displayProperty=fullName>.

## <a name="rule-description"></a>Regelbeschreibung

Mit dieser Regel wird vorausgesetzt, dass <xref:System.IntPtr>, <xref:System.UIntPtr>, und <xref:System.Runtime.InteropServices.HandleRef> Felder Speichern von Zeigern in nicht verwalteten Ressourcen. Typen, die nicht verwaltete Ressourcen zuordnen müssen implementieren <xref:System.IDisposable> können Aufrufer, um diese Ressourcen bei Bedarf freigeben und verkürzen die Lebensdauer der Objekte, die die Ressourcen enthalten.

Das empfohlene Entwurfsmuster zum Bereinigen von nicht verwalteten Ressourcen ist sowohl eine implizite als auch eine explizite Möglichkeit, um die Ressourcen freizugeben, mit der <xref:System.Object.Finalize%2A?displayProperty=fullName> Methode und die <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> -Methode, bzw. Der Garbage Collector Ruft die <xref:System.Object.Finalize%2A> Methode eines Objekts zu einem unbestimmten Zeitpunkt nach dem das Objekt festgestellt wird, dass Sie nicht mehr erreichbar ist. Nach dem <xref:System.Object.Finalize%2A> aufgerufen wird, eine zusätzliche automatische speicherbereinigung ist erforderlich, um das Objekt freigeben. Die <xref:System.IDisposable.Dispose%2A> Methode ermöglicht dem Aufrufer, Ressourcen bei Bedarf, früher als die Ressourcen freigegeben werden sollen, wenn der Garbage Collector überlassen explizit freizugeben. Nachdem sie die nicht verwalteten Ressourcen bereinigt <xref:System.IDisposable.Dispose%2A> sollten aufrufen, die <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> Methode, um dem Garbage Collector mitzuteilen, dass <xref:System.Object.Finalize%2A> ist nicht mehr aufgerufen werden muss; Dadurch entfällt die Notwendigkeit für die zusätzliche Garbagecollection und verkürzt die die Lebensdauer des Objekts.

## <a name="how-to-fix-violations"></a>Behandeln von Verstößen
 Um einen Verstoß gegen diese Regel zu beheben, implementieren <xref:System.IDisposable>.

## <a name="when-to-suppress-warnings"></a>Wenn Sie Warnungen unterdrücken
 Es ist sicher eine Warnung dieser Regel zu unterdrücken, wenn der Typ nicht über eine nicht verwaltete Ressource verweist. Andernfalls, unterdrücken Sie keine Warnung dieser Regel da Fehler implementieren <xref:System.IDisposable> kann dazu führen, dass nicht verwaltete Ressourcen nicht verfügbar oder nicht verwendet werden.

## <a name="example"></a>Beispiel
 Das folgende Beispiel zeigt einen Typ, der implementiert <xref:System.IDisposable> , um eine nicht verwaltete Ressource zu bereinigen.

 [!code-csharp[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/CSharp/ca1049-types-that-own-native-resources-should-be-disposable_1.cs)]
 [!code-vb[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/VisualBasic/ca1049-types-that-own-native-resources-should-be-disposable_1.vb)]

## <a name="related-rules"></a>Verwandte Regeln
 [CA2115: Rufen Sie GC. KeepAlive beim Verwenden systemeigener Ressourcen](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)

 [CA1816: Rufen Sie GC. SuppressFinalize ordnungsgemäß](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)

 [CA2216: Verwerfbare Typen sollten einen Finalizer deklarieren](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

 [CA1001: Typen, die löschbare Felder besitzen, müssen gelöscht werden können](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)

## <a name="see-also"></a>Siehe auch

- [Bereinigen von nicht verwalteten Ressourcen](/dotnet/standard/garbage-collection/unmanaged)
- [Dispose-Muster](/dotnet/standard/design-guidelines/dispose-pattern)