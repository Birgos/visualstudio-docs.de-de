---
title: Installieren von Test-Agents und Testcontrollern
ms.date: 10/24/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- configure test agents, test lab
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e5c0a9078cdbe9ad84b53cd7f667dbd9e3c83d2b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54970486"
---
# <a name="install-test-agents-and-test-controllers"></a>Installieren von Test-Agents und Testcontrollern

Für Testszenarios, in denen Visual Studio und Azure Test Plans oder Team Foundation Server (TFS) verwendet wird, ist kein Testcontroller erforderlich. Agents für Visual Studio führen die Orchestrierung durch Kommunikation mit Azure Test Plans oder TFS aus. Ein mögliches Szenario könnte darin bestehen, dass Sie regelmäßige Tests für Build und Release-Workflows in Azure Test Plans oder TFS durchführen.

Sie könnten auch erwägen, ob es besser wäre, stattdessen [Build- oder Releaseverwaltung](use-build-or-rm-instead-of-lab-management.md) zu verwenden.

## <a name="system-requirements"></a>Systemanforderungen

Die folgende Tabelle zeigt die Systemvoraussetzungen für die Installation des Test-Agent oder Testcontrollers für Visual Studio 2017:

| Element | Anforderungen |
| ---- | ------------ |
| **Agent** | Windows 10<br />Windows 8, Windows 8.1<br />Windows 7 Service Pack 1<br />Windows Server 2016: Standard und Datacenter<br />Windows Server 2012 R2 |
| **Controller** | Windows 10<br />Windows 8, Windows 8.1<br />Windows 7 Service Pack 1<br />Windows Server 2016: Standard und Datacenter<br />Windows Server 2012 R2 |
| **.NET Framework** | .NET Framework 4.5 |

## <a name="install-the-test-controller-and-test-agents"></a>Installieren von Testcontroller und Test-Agents

Sie können über [visualstudio.microsoft.com](https://visualstudio.microsoft.com/downloads/?q=agents) Agents für Visual Studio 2017 herunterladen. Suchen Sie nach *Agents für Visual Studio 2017*, wählen Sie entweder *Agent* oder *Controller* aus, und klicken Sie auf *Herunterladen*. Führen Sie zum Installieren des Test-Agents oder -controllers die ausführbare Datei aus, die Sie heruntergeladen haben.

Sie können Agents für Visual Studio 2015 und Visual Studio 2013 von der Seite mit [älteren Downloads](https://visualstudio.microsoft.com/vs/older-downloads/) herunterladen.

Diese Installer stehen als ISO-Dateien für die unkomplizierte Installation auf virtuellen Computern zur Verfügung.

## <a name="compatible-versions-of-tfs-microsoft-test-manager-the-test-controller-and-test-agent"></a>Kompatible Versionen von TFS, Microsoft Test Manager, Testcontroller und Test-Agent

Sie können verschiedene Versionen von TFS, Microsoft Test Manager, Testcontroller und Test-Agent entsprechend der folgenden Tabelle kombinieren:

| TFS | Microsoft Test Manager mit Lab-Center | Controller | Agent |
| --- | -------------------------------------- | ---------- | ----- |
| 2017: Upgrade von 2015 oder Neuinstallation | 2017 | 2017 | 2017 |
| 2017: Upgrade von 2015 oder Neuinstallation | 2017 | 2013 Update 5 | 2013 Update 5 |
| 2017: Upgrade von 2015 oder Neuinstallation | 2015 | 2013 Update 5 | 2013 Update 5 |
| 2015: Upgrade von 2013 | 2013 | 2013 |2013 |
| 2015: Neuinstallation | 2013 | 2013 | 2013 |
| 2015: Upgrade von 2013 oder Neuinstallation | 2015 | 2013 | 2013 |
| 2013 | 2015 | 2013 | 2013 |

> [!NOTE]
> Lab Management-Szenarien werden in TFS 2018 und Azure DevOps Services nicht mehr unterstützt. Weitere Informationen finden Sie in [Team Foundation Server 2018: Anmerkungen zu dieser Version](/visualstudio/releasenotes/tfs2018-relnotes#--removing-support-for-lab-center-and-automated-testing-flows-in-microsoft-test-manager).

## <a name="upgrade-from-visual-studio-2013-test-agents"></a>Aktualisieren von Visual Studio 2013-Test-Agents

Sie sollten Agents für Visual Studio in allen neuen automatisierten Testszenarios verwenden. Sie können die Aufgabe *Deploy Test Agents* (Test-Agents bereitstellen) in einer Buildpipeline verwenden, um die Test-Agents auf Ihren Computer herunterzuladen und zu installieren.

In der folgenden Tabelle werden die von Agents für Visual Studio 2013 unterstützten Szenarios und die Alternativen für Team Foundation Server (TFS) 2015 und Azure Test Plans dargestellt:

| Szenarios, die von Agents für Visual Studio 2013 unterstützt werden | Alternativen in TFS und Azure Test Plans |
| - | - |
| Erstellen-Bereitstellen-Testen-Workflow in Visual Studio | Benutzer können eine [Buildpipeline](/azure/devops/pipelines/index?view=vsts) (kein XAML-Build) für Szenarios zum Erstellen, Bereitstellen und Testen in TFS verwenden. |
| Auslastungstests (Leistungstests) mit lokalen Remotecomputern | Verwenden Sie das Testcontroller und Test-Agents 2013 Update 5, um Auslastungstests lokal auszuführen. |
| Remoteausführung von automatisierten Tests von Microsoft Test Manager mit einer Laborumgebung | Es gibt aktuell keine Alternative für dieses Szenario. Es wird empfohlen, dass Sie den Task „Funktionstests ausführen“ in Build- und Releasedefinitionen verwenden (nicht in XAML-Builds), um Tests remote auszuführen. |
| Entwickler, die Remotetests in Visual Studio ausführen | Wird nicht mehr unterstützt. |
