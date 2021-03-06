---
title: Deaktivieren oder Verschieben des Paketcaches
description: Informationen zum Deaktivieren, Aktivieren oder Verschieben des Paketcaches für Visual Studio-Bereitstellungen.
ms.date: 04/14/2017
ms.custom: seodec18
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- cache
- nocache
helpviewer_keywords:
- '{{PLACEHOLDER}}'
- '{{PLACEHOLDER}}'
ms.assetid: 2429993A-3F0E-41C5-9562-FEA6AE994440
author: heaths
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 06234ab61bc77f9d52e18b479f05f145e850d0ba
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54924151"
---
# <a name="disable-or-move-the-package-cache"></a>Deaktivieren oder Verschieben des Paketcaches

Der Paketcache stellt eine Quelle für installierte Pakete für den Fall zur Verfügung, dass Sie Visual Studio oder dazugehörige Produkte reparieren müssen, wenn keine Internetverbindung vorhanden ist. Bei einigen Laufwerken oder Systemeinrichtungen möchten Sie jedoch ggf. nicht alle diese Pakete aufbewahren.
Das Installationsprogramm lädt diese bei Bedarf herunter, sodass Sie den Paketcache deaktivieren oder verschieben können, wenn Sie Speicherplatz einsparen oder freigeben möchten.

## <a name="disable-the-package-cache"></a>Deaktivieren des Paketcaches

Ehe Sie Visual Studio oder andere Produkte mit dem neuen Installationsprogramm installieren, ändern oder reparieren, können Sie das Installationsprogramm mit dem Schalter `--nocache` starten.

```cmd
"%ProgramFiles(x86)%\Microsoft Visual Studio\Installer\vs_installer.exe" --nocache
```

Bei Vorgängen, die Sie auf Produkte anwenden, werden vorhandene Pakete für das jeweilige Produkt entfernt, wodurch das Speichern von Paketen vermieden wird, nachdem diese installiert wurden. Wenn Sie Visual Studio ändern oder reparieren und Pakete erforderlich sind, werden sie automatisch heruntergeladen und entfernt, nachdem sie installiert wurden.

Wenn Sie den Cache erneut aktivieren möchten, übergeben Sie stattdessen `--cache`. Nur erforderliche Pakete werden zwischengespeichert. Wenn Sie also alle Pakete wiederherstellen müssen, sollten Sie Visual Studio reparieren, ehe Sie die Verbindung mit dem Netzwerk trennen.

```cmd
"%ProgramFiles(x86)%\Microsoft Visual Studio\Installer\vs_installer.exe" repair --passive --norestart --cache
```

Sie können auch die [Registrierungsrichtlinie](set-defaults-for-enterprise-deployments.md) `KeepDownloadedPayloads` festlegen, um die Cache zu deaktivieren, bevor Sie Visual Studio installieren, ändern oder reparieren.

## <a name="move-the-package-cache"></a>Verschieben des Paketcaches

Eine gängige Systemkonfiguration ist die Installation von Windows auf einem SSD-Datenträger mit einer (oder mehreren) größeren Festplatten für Entwicklungszwecke, z. B. Quellcode, Programmbinärdateien usw. Wenn Sie offline arbeiten möchten, können Sie stattdessen den Paketcache verschieben.

Derzeit ist dies nur möglich, wenn Sie die [Registrierungsrichtlinie ](set-defaults-for-enterprise-deployments.md) `CachePath` festlegen, bevor Sie Visual Studio installieren, ändern oder reparieren.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Siehe auch

* [Installieren von Visual Studio](install-visual-studio.md)
* [Festlegen von Standardeinstellungen für Unternehmensbereitstellungen](set-defaults-for-enterprise-deployments.md)
* [Verwenden von Befehlszeilenparametern zum Installieren von Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
