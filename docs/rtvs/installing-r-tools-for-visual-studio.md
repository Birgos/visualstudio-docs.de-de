---
title: Installieren der R-Tools
description: Installieren der R-Tools in Visual Studio 2017 und Visual Studio 2015, einschließlich Offlineinstallationen.
ms.date: 01/24/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 9f4c00056c93230d588216ff425dee56d42e0961
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54921093"
---
# <a name="how-to-install-r-tools-for-visual-studio"></a>Installieren von R Tools für Visual Studio

In diesem Artikel:

- [Unterstützte Versionen von Visual Studio](#supported-versions-of-visual-studio)
- [Installieren von RTVS in Visual Studio 2017](#installing-rtvs-in-visual-studio-2017)
- [Installieren von RTVS in Visual Studio 2015](#installing-rtvs-in-visual-studio-2015)
- [Offlineinstallation](#offline-installation-of-visual-studio-and-rtvs)

> [!Note]
> Nach der Installation von R Tools möchten Sie möglicherweise Visual Studio für ein optimiertes Layout für Datenspezialisten konfigurieren, wie im Artikel [Optionen](options-for-r-tools-in-visual-studio.md) beschrieben.

## <a name="supported-versions-of-visual-studio"></a>Unterstützte Versionen von Visual Studio

R Tools für Visual Studio (RTVS) werden unter Windows in den Editionen Community (kostenlos), Professional und Enterprise von [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) sowie [Visual Studio 2015 Update 3 (oder höher)](http://go.microsoft.com/fwlink/?LinkId=691129) (direkter Download) unterstützt.

RTVS wird in Visual Studio für Mac derzeit nicht unterstützt.

RTVS wird nicht installiert, wenn Sie nur über Visual Studio Shell verfügen, was in Produkten wie z.B. Visual Studio Test Professional und SQL Server Management Studio enthalten ist. Visual Studio Shell verfügt nicht über die nötigen Komponenten für RTVS.

## <a name="install-rtvs-in-visual-studio-2017"></a>Installieren von RTVS in Visual Studio 2017

1. Führen Sie den Visual Studio-Installer aus, und wählen Sie die Option **Ändern** aus (weitere Informationen finden Sie unter [Ändern von Visual Studio](../install/modify-visual-studio.md)). Wenn Sie Visual Studio noch nicht installiert haben, finden Sie weitere Informationen unter [Installieren von Visual Studio](../install/install-visual-studio.md). Achten Sie unter Windows 7 darauf, dass Ihr Installer aktualisiert ist und Visual Studio 2017, Version *15.2, Build 26430.12* oder höher anzeigt.

1. Wählen Sie die Workload **Data Science und analytische Anwendungen** aus.

    ![Workload von Data Science und analytischen Anwendungen in VS2017](media/installation-data-science-workload.png)

1. Legen Sie zusätzliche Optionen auf der rechten Seite unter dem gleichen Workloadnamen fest. Diese Workload enthält standardmäßig F#- und Python-Unterstützung. Die Mindestanforderungen für R sind die **R language support** (Unterstützung der Sprache R), **Runtime support for R development** (Laufzeitunterstützung für die R-Entwicklung) , und der **Microsoft R client** (Microsoft R-Client).

RTVS wird installiert unter: *%ProgramFiles(x86)%\Microsoft Visual Studio\<Version>\<Edition>Common7\IDE\Erweiterungen\Microsoft\R-Tools für Visual Studio*, wobei *\<Version>* in der Regel `2017` ist und *\<Edition>* entweder `Community`, `Professional` oder `Enterprise`.

## <a name="install-rtvs-in-visual-studio-2015"></a>Installieren von RTVS in Visual Studio 2015

Mit Visual Studio 2015 müssen Sie einen R-Interpreter und die R Tools separat installieren.

### <a name="install-an-r-interpreter"></a>Installieren eines R-Interpreters

RTVS erfordert eine 64-Bit-Installation der R-Version 3.2.1 oder höher aus mindestens einer der folgenden Quellen:

- [Microsoft R Open](https://mran.microsoft.com/download/)
- [Microsoft R Client](/machine-learning-server/r-client/what-is-microsoft-r-client)
- [CRAN R](https://cran.r-project.org/bin/windows/base/)

Microsoft R Open und CRAN R lassen beide mehrere parallele Versionen zu. Microsoft R Client unterstützt jedoch nur eine Version und verwendet immer die neueste Version, die Sie installiert haben.

### <a name="install-the-r-tools"></a>Installieren der R Tools

Laden Sie die aktuelle RTVS-Erweiterung für Visual Studio 2015 von [https://aka.ms/rtvs-current](https://aka.ms/rtvs-current) herunter. RTVS prüft auf eine geeignete Visual Studio-Version und hilft Ihnen auch dabei, einen R-Interpreter zu installieren, falls Sie dies noch nicht getan haben.

> [!Note]
> Das eigenständige RTVS-Installationsprogramm funktioniert nur mit Visual Studio 2015. Für Visual Studio 2017 ist, wie zuvor beschrieben, die Installation des R-Supports über die [Workload von Data Science und analytischen Anwendungen](#installing-rtvs-in-visual-studio-2017) nötig.

RTVS für Visual Studio 2015 wird hier installiert:`%ProgramFiles(x86)%\Microsoft Visual Studio 14\Common7\IDE\Extensions\Microsoft\R Tools for Visual Studio`

## <a name="offline-installation-of-visual-studio-and-rtvs"></a>Offlineinstallation von Visual Studio und RTVS

Die Offlineinstallation eignet sich für Computer, die keine Internetverbindung besitzen:

1. Wechseln Sie zu [Create an offline installation of Visual Studio 2017 (Erstellen einer Offlineinstallation von Visual Studio 2017)](../install/create-an-offline-installation-of-visual-studio.md).

1. Wenn Sie Visual Studio 2015 verwenden, wählen Sie in der Auswahl oberhalb des Inhaltsverzeichnisses **2015** aus.

1. Führen Sie die Anweisungen zum Erstellen einer Offlineinstallation in der Webseite aus.

1. Laden Sie die RTVS-Offline-Installer für Visual Studio 2015 unter [https://aka.ms/rtvs-current-zip](https://aka.ms/rtvs-current-zip) und [https://aka.ms/rtvs-remote-zip](https://aka.ms/rtvs-remote-zip) herunter.

1. Installieren von Visual Studio und RTVS über die Offlineinstaller.

## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit R](getting-started-with-r.md)
- [R Tools sample projects (R Tools und Beispielprojekte)](getting-started-samples.md)
- [Hilfe in R-Tools](getting-started-help.md)
- [Optionen für R Tools](options-for-r-tools-in-visual-studio.md)
- [Microsoft Machine Learning Server (vorher R Server)](/machine-learning-server/)