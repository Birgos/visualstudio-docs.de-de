---
title: Automatisieren der Installation mit einer Antwortdatei
description: Erfahren Sie mehr über das Erstellen einer JSON-Antwortdatei, mit der Sie Ihre Visual Studio-Installation automatisieren können.
ms.date: 08/14/2017
ms.custom: seodec18
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- response file
- automate
- installation
- command-line
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8ae0fb990ee9c7aa6168420a5b5f5144a216165e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54975282"
---
# <a name="how-to-define-settings-in-a-response-file"></a>Gewusst wie: Definieren von Einstellungen in einer Antwortdatei

Administratoren, die Visual Studio bereitstellen, können eine Antwortdatei mit dem `--in`-Parameter angeben, wie im folgenden Beispiel gezeigt:

```cmd
vs_enterprise.exe --in customInstall.json
```

Antwortdateien sind [JSON](http://json-schema.org/)-Dateien, deren Inhalt die Befehlszeilenargumente wiedergibt.  Allgemein gilt: Wenn ein Befehlszeilenparameter keine Argumente verwendet (z.B. `--quiet`, `--passive` usw.), muss der Wert in der Antwortdatei TRUE oder FALSE sein.  Wenn er ein Argument verwendet (z.B. `--installPath <dir>`), muss der Wert in der Antwortdatei eine Zeichenfolge sein.  Wenn er ein Argument verwendet und mehrmals in der Befehlszeile vorkommen kann (z.B. `--add <id>`), muss es sich um Array aus Zeichenfolgen handeln.

Parameter, die in der Befehlszeile angegeben werden, überschreiben Einstellungen aus der Antwortdatei, es sei denn, Parameter übernehmen mehrere Eingaben (z.B. `--add`). Wenn Sie mehrere Eingaben haben, werden die in der Befehlszeile angegebenen Eingaben mit den Einstellungen aus der Antwortdatei zusammengeführt.

## <a name="setting-a-default-configuration-for-visual-studio"></a>Festlegen einer Standardkonfiguration für Visual Studio

Wenn Sie mit `--layout` einen Cache des Netzwerklayouts erstellt haben, wird im Layout eine anfängliche Datei namens `response.json` erstellt. Wenn Sie ein Teillayout erstellen, enthält diese Antwortdatei die Workloads und Sprachen, die im Layout enthalten sind.  Beim Ausführen des Setups über dieses Layout wird automatisch diese Datei „response.json“ verwendet, die Workloads und Komponenten auswählt, die im Layout enthalten sind.  Benutzer können weiterhin alle Workloads auf der Setupbenutzeroberfläche vor der Installation von Visual Studio auswählen oder ausschließen.

Administratoren, die ein Layout erstellen, können die Datei `response.json` im Layout ändern, um die Standardeinstellungen zu steuern, die ihren Benutzern angezeigt werden, wenn sie Visual Studio über das Layout installieren.  Wenn ein Administrator beispielsweise möchte, dass bestimmte Workloads und Komponenten standardmäßig installiert werden, kann die Datei `response.json` so konfiguriert werden, dass diese hinzugefügt werden.

Wenn das Visual Studio-Setup aus einem Layoutordner erfolgt, wird die Antwortdatei im Layoutordner _automatisch_ verwendet.  Sie müssen die Option `--in` nicht verwenden.

Sie können die Datei `response.json` aktualisieren, die in einem Offlinelayoutordner erstellt wird, um die Standardeinstellung für Benutzer festzulegen, die die Installation mithilfe dieses Layouts vornehmen.

> [!WARNING]
> Es ist wichtig, dass Sie die vorhandenen Eigenschaften unverändert lassen, die beim Erstellen des Layouts festgelegt wurden.

Die `response.json`-Basisdatei in einem Layout sollte dem folgenden Beispiel ähneln, es sei denn, sie enthält den Wert für das Produkt und den Kanal, die bzw. den Sie installieren möchten:

```json
{
  "installChannelUri": ".\\ChannelManifest.json",
  "channelUri": "https://aka.ms/vs/15/release/channel",
  "installCatalogUri": ".\\Catalog.json",
  "channelId": "VisualStudio.15.Release",
  "productId": "Microsoft.VisualStudio.Product.Enterprise"
}
```

Beim Erstellen oder Aktualisieren eines Layouts wird auch eine „response.template.json“-Datei erstellt.  Diese Datei enthält alle Workloads, Komponenten und die Sprachen-IDs, die verwendet werden können.  Diese Datei wird als Vorlage für all das bereitgestellt, was in einer benutzerdefinierten Installation einbezogen werden kann.  Administratoren können diese Datei als Ausgangspunkt für eine benutzerdefinierte Antwortdatei verwenden.  Entfernen Sie einfach all die IDs, die Sie nicht installieren möchten, und speichern Sie das Ergebnis in Ihrer eigenen Antwortdatei.  Passen Sie die Datei „response.template.json“ nicht an. Andernfalls gehen die Änderungen bei dem nächsten Layoutupdate verloren.

## <a name="example-layout-response-file-content"></a>Beispiel des Inhalts einer Layoutantwortdatei

Bei folgenden Beispiel wird Visual Studio Enterprise mit sechs allgemeinen Workloads und Komponenten sowie den Benutzeroberflächensprachen Englisch und Französisch installiert. Sie können dieses Beispiel als Vorlage nutzen. Ändern Sie dazu lediglich die Workloads und Komponenten in diejenigen, die Sie installieren möchten:

```json
{
  "installChannelUri": ".\\ChannelManifest.json",
  "channelUri": "https://aka.ms/vs/15/release/channel",
  "installCatalogUri": ".\\Catalog.json",
  "channelId": "VisualStudio.15.Release",
  "productId": "Microsoft.VisualStudio.Product.Enterprise",

  "installPath": "C:\\VS2017",
  "quiet": false,
  "passive": false,
  "includeRecommended": true,
  "norestart": false,

  "addProductLang": [
    "en-US",
    "fr-FR"
    ],

    "add": [
        "Microsoft.VisualStudio.Workload.ManagedDesktop",
        "Microsoft.VisualStudio.Workload.Data",
        "Microsoft.VisualStudio.Workload.NativeDesktop",
        "Microsoft.VisualStudio.Workload.NetWeb",
        "Microsoft.VisualStudio.Workload.Office",
        "Microsoft.VisualStudio.Workload.Universal",
        "Component.GitHub.VisualStudio"
    ]
}
```

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Siehe auch

* [Arbeitsauslastungs- und Komponenten-IDs von Visual Studio 2017](workload-and-component-ids.md)
