---
title: Verwenden von Befehlszeilenparametern zum Installieren von Visual Studio 2015 | Microsoft-Dokumentation
titleSuffix: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-ide-install
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- command-line parameters
- switches
- command prompt
ms.assetid: 480f3cb4-d873-434e-a8bf-82cff7401cf2
caps.latest.revision: 10
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: e81e9f7fad5976ad853254e04289d89d09b87ac6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/02/2019
ms.locfileid: "53922173"
---
# <a name="use-command-line-parameters-to-install-visual-studio"></a>Verwenden von Befehlszeilenparametern zum Installieren von Visual Studio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Die neueste Dokumentation für Visual Studio 2017 finden Sie unter [Verwenden von Befehlszeilenparametern zum Installieren von Visual Studio 2017](https://docs.microsoft.com/visualstudio/install/use-command-line-parameters-to-install-visual-studio).

Wenn Sie Visual Studio 2015 von einer Eingabeaufforderung aus installieren, können Sie die folgenden Befehlszeilenparameter (auch als Schalter bezeichnet) verwenden.

> [!NOTE]
>  Stellen Sie sicher, dass Sie der eigentliche Installer und nicht für die Bootstrapperdatei verwenden. Beispielsweise stellen sicher, dass Sie **`vs_enterprise.exe`** statt Vs_enterprise_*GUID*.exe. Sie können ein Installationsprogramm aus [My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015).

## <a name="list-of-command-line-parameters"></a>Liste der Befehlszeilenparameter
 Bei Visual Studio-Befehlszeilenparametern wird nicht zwischen Groß- und Kleinschreibung unterschieden.

|Parameter|Beschreibung|
|---------------|-----------------|
|**/?**<br /><br /> **/help**<br /><br /> **/h**|Zeigt die Befehlszeilenparameter an.|
|**/ AddRemoveFeatures**|Gibt an, welche Funktionen vom installierten Produkt entfernt oder zu diesem hinzugefügt werden.|
|**/ AdminFile** *"admindeployment.xml"*|Installiert Visual Studio mithilfe der von Ihnen für administrative Installation angegebenen Datendatei.|
|**/ ChainingPackage** *BundleName*|Gibt an, welches Bündel dieses Bündel verkettet. Dies kann auch zum Angeben einer Customer Improvement Experience-Gruppe verwendet werden.|
|**/ CreateAdminFile \<Dateiname >**|Gibt den Speicherort an, um eine Kontrolldateien zu erstellen, die mit „/AdminFile“ verwendet werden kann.|
|**/ CustomInstallPath** *InstallationDirectory*|Installiert alle alternativen Pakete in dem von Ihnen angegebenen Verzeichnis.|
|**/ "Forcerestart"**|Startet den Computer nach der Installation immer neu.|
|**/full**|Installiert alle Produktfunktionen.|
|**/ InstallSelectableItems \<Elementname 1 > [;\< Der Elementname 2 >]**|Liste der Auswahlstrukturelemente, die auf dem Auswahlbildschirm des Installations-Assistenten aktiviert werden sollen.|
|**/l**<br /><br /> **/ Melden Sie** *Dateiname*|Gibt einen Speicherort für die Protokolldatei an.|
|**/ Layout** *Verzeichnis*|Kopiert die Dateien auf dem Installationsmedium in das von Ihnen angegebene Verzeichnis.|
|**/NoCacheOnlyMode**|Verhindert, dass der Paket-Cache vorab gefüllt wird.|
|**/NoRefresh**|Verhindert die Überprüfung auf neuere erforderliche oder empfohlene Versionen dieses Produkts.|
|**/norestart**|Hindert die Installationsanwendung während oder nach der Installation am Neustart des Computers. Informationen zu den Rückgabecodes, nach denen Sie suchen müssen, finden Sie im [Administratorhandbuch für Visual Studio](../install/visual-studio-administrator-guide.md) im Abschnitt „Rückgabecodes“.|
|**/noweb**|Verhindert Installation aus dem Internet.|
|**/ OverrideFeedUri \<Pfad zur Feeddatei >**|Pfad zu einem lokalen, externen Feed mit einer Beschreibung der Softwareelemente.|
|**/ProductKey**<br /><br /> *ProductKey*|Legt einen benutzerdefinierten Product Key fest, der keine Bindestriche und nicht mehr als 25 Zeichen enthält.|
|**/PromptRestart**|Fordert vor Neustart des Computers den Benutzer auf.|
|**/q**<br /><br /> **/quiet**<br /><br /> **/s**<br /><br /> **/silent**|Unterdrückt die Benutzeroberfläche (UI) für die Installationsanwendung. Wenn Visual Studio bereits installiert ist und Sie keine weiteren Parameter angeben, wird die Installationsanwendung in Wartungsmodus ausgeführt.|
|**/ qb**<br /><br /> **/passive**|Zeigt den Fortschritt an, erwartet jedoch keine Benutzereingaben.|
|**/repair**|Repariert Visual Studio.|
|**/SuppressRefreshPrompt**|Verhindert die Anzeige des Dialogfeld über verfügbare Updates im Installations-Assistenten. Der Installations-Assistent nimmt automatisch alle erforderlichen und empfohlenen aktualisierten Versionen an.|
|**/u**<br /><br /> **/Uninstall**|Deinstalliert [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].|
|**/ Uninstall/Force**<br /><br /> **/ u/Force**|Deinstalliert Visual Studio und alle Funktionen, die mit anderen Produkten gemeinsam genutzt werden. **Warnung:**  Wenn Sie diesen Parameter verwenden, beeinträchtigt dies möglicherweise die Funktionalität anderer Produkte auf dem Computer.|

## <a name="see-also"></a>Siehe auch
 [Administratorhandbuch für Visual Studio](../install/visual-studio-administrator-guide.md)