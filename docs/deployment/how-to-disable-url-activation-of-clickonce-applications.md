---
title: 'Vorgehensweise: Deaktivieren der URL-Aktivierung von ClickOnce-Anwendungen | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- disallowUrlActivation
- URL activation, ClickOnce applications
- ClickOnce deployment, URL activation
ms.assetid: db31a16b-960f-4264-91d7-c7c40f876068
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 26fdadf92fa94efe0a08fdf090e5a295e2f65096
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999976"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications"></a>Vorgehensweise: Deaktivieren der URL-Aktivierung von ClickOnce-Anwendungen

In der Regel wird eine [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]Anwendung automatisch gestartet, sobald sie von einem Webserver installiert wurde. Aus Gründen der Sicherheit könnten Sie dieses Verhalten deaktivieren und Benutzer dazu auffordern, die Anwendung stattdessen über das Menü **Start** zu öffnen. Das folgende Verfahren beschreibt das Deaktivieren der URL-Aktivierung.

Dieses Verfahren kann nur für [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]-Anwendungen verwendet werden, die von einem Webserver auf dem Computer des Benutzers installiert werden. Es kann nicht für reine Onlineanwendungen verwendet werden, die nur über ihre URL gestartet werden können. Weitere Informationen zu den Unterschieden zwischen reinen Onlineanwendungen und installierten Anwendungen finden Sie unter [Auswählen einer Strategie für die ClickOnce-Bereitstellung](../deployment/choosing-a-clickonce-deployment-strategy.md).

Diese Prozedur verwendet das Windows Software Development Kit (SDK) Tool MageUI.exe. Weitere Informationen zu diesem Tool finden Sie unter [MageUI.exe (Manifest Generation and Editing Tool, Graphical Client)](/dotnet/framework/tools/mageui-exe-manifest-generation-and-editing-tool-graphical-client). Sie können auch dieses Verfahren mithilfe von Visual Studio ausführen.

## <a name="procedure"></a>Prozedur

### <a name="to-disable-url-activation-for-your-application"></a>So deaktivieren Sie die URL-Aktivierung für Ihre Anwendung

1.  Öffnen Sie Ihr Bereitstellungsmanifest in „MageUI.exe“. Wenn Sie noch kein Manifest erstellt haben, führen Sie die Schritte in [Exemplarische Vorgehensweise: Manuelles bereitstellen eine ClickOnce-Anwendung](../deployment/walkthrough-manually-deploying-a-clickonce-application.md).

2.  Wählen Sie die Registerkarte **Bereitstellungsoptionen** aus.

3.  Deaktivieren Sie das Kontrollkästchen **Anwendung nach dem Installieren automatisch ausführen**.

4.  Speichern und signieren Sie das Manifest.

## <a name="see-also"></a>Siehe auch

- [Publish ClickOnce applications (Veröffentlichen von ClickOnce-Anwendungen)](../deployment/publishing-clickonce-applications.md)