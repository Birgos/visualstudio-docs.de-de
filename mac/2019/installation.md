---
title: Installieren der Vorschauversion von Visual Studio 2019 für Mac
description: Anweisungen zum Installieren der Vorschauversion von Visual Studio 2019 für Mac und zusätzlicher erforderlichen Komponenten für die plattformübergreifende Entwicklung.
author: conceptdev
ms.author: crdun
ms.date: 11/03/2018
ms.technology: vs-ide-install
ms.assetid: 22B1F2CD-32AE-464D-80AC-C8AB4786B015
ms.custom: video
ms.openlocfilehash: 17acdd63b5632cf141cc5407ce8e09be3e3a69a0
ms.sourcegitcommit: a260df15214b3198a28ca4e312263942cf6f4ce7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2019
ms.locfileid: "54443779"
---
# <a name="install-visual-studio-2019-for-mac-preview"></a>Installieren der Vorschauversion von Visual Studio 2019 für Mac

> [!NOTE]
> Die Vorschauversion von Visual Studio 2019 für Mac kann parallel mit dem aktuellen stabilen Release von Visual Studio für Mac installiert werden. Während der Installation werden Sie aufgefordert, Ihre vorhandene Visual Studio-Version zu aktualisieren, falls es sich nicht um die aktuelle stabile Version handelt.

## <a name="requirements-for-the-visual-studio-2019-for-mac-preview"></a>Anforderungen für die Vorschauversion von Visual Studio 2019 für Mac

- Ein Mac mit macOS High Sierra 10.13 oder höher.

Darüber hinaus benötigen Sie zum Erstellen von Xamarin-Apps für iOS oder macOS:

- Xcode 10.0 oder höher. Für gewöhnlich wird die neuste stabile Version empfohlen.
- eine Apple-ID Erstellen Sie eine kostenlose Apple-ID unter https://appleid.apple.com, wenn Sie noch keine besitzen. Dies ist für die Installation von und die Anmeldung bei Xcode erforderlich.

## <a name="installing-the-preview"></a>Installieren der Vorschauversion

1. Laden Sie das Installationsprogramm für die Vorschauversion von der [Seite „Visual Studio für Mac (Vorschau)“](https://aka.ms/vs4mac-preview) herunter.
2. Klicken Sie nach Abschluss des Downloads auf **VisualStudioforMacPreviewInstaller.dmg**, um den Installer einzubinden. Führen Sie ihn anschließend durch Doppelklicken auf das Pfeillogo aus:

    [![Auf großen Pfeil klicken, um die Installation zu starten](media/install-preview-installer-sml.png)](media/install-preview-installer.png#lightbox)

3. Möglicherweise wird Ihnen eine Warnmeldung angezeigt, in der Sie darauf hingewiesen werden, dass die Anwendung aus dem Internet heruntergeladen wird. Klicken Sie auf **Öffnen**.
4. Warten Sie, während das Installationsprogramm Ihr System überprüft:

    [![Das Installationsprogramm überprüft Ihr System auf installierte Komponenten](media/install-preview-checking-sml.png)](media/install-preview-checking.png#lightbox)

5. Ihnen wird eine Warnmeldung angezeigt, in der Sie dazu aufgefordert werden, die Datenschutz- und Lizenzbedingungen zu akzeptieren. Klicken Sie zum Lesen der Bedingungen auf die Links, und klicken Sie auf **Weiter**, wenn Sie die Bedingungen akzeptieren:

    [![Klicken Sie auf die Links zu den Datenschutz- und Lizenzbedingungen, und fahren Sie fort, wenn Sie diese akzeptieren](media/install-preview-privacy-sml.png)](media/install-preview-privacy.png#lightbox)

6. Die Liste der verfügbaren Workloads wird angezeigt. Wählen Sie die Workloads aus, die Sie verwenden möchten:

    [![Wählen Sie aus, welche optionalen Workload-Features Sie gerne installieren würden](media/install-preview-selection-sml.png)](media/install-preview-selection.png#lightbox)

    Wenn Ihre aktuelle Version von Visual Studio 2017 für Mac älter als Version 7.7 ist, werden Sie aufgefordert, ein Upgrade auf die aktuelle stabile Version zu genehmigen (dieses Upgrade unterstützt die parallele Installation). Klicken Sie auf **Weiter**, um das Upgrade zu genehmigen:

    ![Die Durchführung eines Upgrades für die stabile Version auf 7.7 ist erforderlich](media/install-preview-older-upgrade.png)

7. Klicken Sie auf die Schaltfläche **Installieren**, nachdem Sie Ihre Auswahl getroffen haben.
8. Das Installationsprogramm zeigt während des Downloads den Fortschritt an und installiert Visual Studio für Mac sowie die ausgewählten Workloads. Möglicherweise werden Sie dazu aufgefordert, Ihr Kennwort einzugeben, um die für die Installation erforderlichen Berechtigungen zu erteilen.
9. Sie können **Visual Studio (Vorschauversion)** jederzeit verwenden, wenn Sie die Vorschauversion testen möchten, oder für Ihre Produktionsarbeit wieder zur aktuellen stabilen Version von Visual Studio wechseln. Hier werden die beiden Symbole angezeigt:

    ![Unterschiede zwischen den Symbolen für die stabile Version und die Vorschauversion](media/install-preview-icons-sml.png)

Wenn während der Installation in einer Unternehmensumgebung Netzwerkprobleme auftreten, lesen Sie die Anweisungen unter [Installation hinter einer Firewall oder einem Proxy](https://docs.microsoft.com/visualstudio/mac/installation#install-visual-studio-for-mac-behind-a-firewall-or-proxy-server).

Informationen zu den Änderungen in den [Versionshinweisen](https://docs.microsoft.com/visualstudio/releasenotes/vs2019-mac-preview-relnotes).

> [!NOTE]
> Wenn Sie sich während der ursprünglichen Installation gegen die Installation einer Plattform oder eines Tools entschieden haben (indem Sie die Auswahl in Schritt 6 aufgehoben haben), müssen Sie den Installer erneut ausführen, wenn Sie die Komponenten später hinzufügen möchten.

## <a name="install-visual-studio-for-mac-behind-a-firewall-or-proxy-server"></a>Installieren von Visual Studio für Mac hinter einer Firewall oder einem Proxyserver

Für die Installation von Visual Studio für Mac hinter einer Firewall müssen bestimmte Endpunkte zugänglich gemacht werden, um die Downloads der erforderlichen Tools und Updates für Ihre Software zuzulassen.

Konfigurieren Sie Ihr Netzwerk, damit der Zugriff auf die folgenden Speicherorte gewährt wird:

- [Visual Studio-Endpunkte](/visualstudio/install/install-visual-studio-behind-a-firewall-or-proxy-server)

## <a name="next-steps"></a>Nächste Schritte

Die Installation von Visual Studio für Mac ermöglicht Ihnen das Schreiben von Code für Ihre Apps. Hinsichtlich der nächsten Schritte zum Schreiben und Bereitstellen von Projekten werden folgende Leitfäden bereitgestellt:

### <a name="ios"></a>iOS

1. [Hello, iOS](https://developer.xamarin.com/guides/ios/getting_started/hello,_iOS/)
2. [Device Provisioning](https://developer.xamarin.com/guides/ios/getting_started/installation/device_provisioning) (Gerätebereitstellung) (zum Ausführen Ihrer Anwendung auf dem Gerät)

### <a name="android"></a>Android

1. [Using the Xamarin Android SDK Manager (Verwenden des Xamarin.Android SDK-Managers)](https://developer.xamarin.com/guides/android/getting_started/installation/android-sdk/?ide=xs)
2. [Android SDK-Emulator](https://developer.xamarin.com/guides/android/getting_started/installation/android-emulator/)
4. [Set Up Device for Development (Einrichten eines Geräts für die Entwicklung)](https://developer.xamarin.com/guides/android/getting_started/installation/set_up_device_for_development/)

### <a name="net-core-apps-aspnet-core-web-apps-unity-game-development"></a>Entwicklung von .NET Core-Apps, ASP.NET Core-Web-Apps und Unity-Spielen

Informationen zu anderen Workloads finden Sie auf der Seite zu den [Workloads](/visualstudio/mac/workloads).

## <a name="related-video"></a>Zugehörige Videos

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Acquisition/player]

## <a name="see-also"></a>Siehe auch

- [Installieren von Visual Studio 2017 (unter Windows)](/visualstudio/install/install-visual-studio)
