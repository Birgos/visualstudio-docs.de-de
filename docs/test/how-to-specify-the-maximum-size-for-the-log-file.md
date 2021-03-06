---
title: Größe der Protokolldatei für Auslastungstests
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, logging
ms.assetid: 417059bf-37ae-4e7a-b9b0-29bd71f1414f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.openlocfilehash: 5b685681444e501ef05b76bea22d2152c3296908
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54973680"
---
# <a name="how-to-specify-the-maximum-size-for-the-log-file-for-load-tests"></a>Vorgehensweise: Angeben der maximalen Größe für die Protokolldatei für Auslastungstests

Standardmäßig wird die maximale Größe der für Auslastungstests verwendeten Protokolldatei auf 20 Megabyte festgelegt. Sie können diesen Wert ändern, indem Sie die dem Controllerdienst zugeordnete Konfigurationsdatei bearbeiten.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="specify-the-maximum-log-file-size-for-load-test"></a>Angeben der maximalen Protokolldateigröße für Auslastungstests

1.  Öffnen Sie die XML-Konfigurationsdatei *QTCcontroller.exe.config* im Verzeichnis *%ProgramFiles(x86)%\Microsoft Visual Studio\2017\Enterprise\Common7\IDE\QTCcontroller.exe.config*.

2.  Suchen Sie den `<add key="LogSizeLimitInMegs" value="20"/>`-Eintrag unter dem `<appSettings>`-Tag.

    ```xml
    <appSettings>
        <add key="LogSizeLimitInMegs" value="20"/>
        <add key="AgentConnectionTimeoutInSeconds" value="120"/>
        <add key="AgentSyncTimeoutInSeconds" value="300"/>
        <add key="ControllerServicePort" value="6901"/>
        <add key="ControllerUsersGroup" value="TeamTestControllerUsers"/>
        <add key="ControllerAdminsGroup" value="TeamTestControllerAdmins"/>
        <add key="CreateTraceListener" value="no"/>
      </appSettings>
    ```

3.  Legen Sie für `value ="20"` die maximal zulässige Größe fest, die Sie für die Protokolldatei angeben möchten.

    > [!NOTE]
    > Durch die Eingabe des Werts "0" wird angegeben, dass die Größe der Protokolldatei nur durch den verfügbaren Speicherplatz auf dem Datenträger beschränkt wird.

## <a name="see-also"></a>Siehe auch

- [Ändern von Einstellungen für die Auslastungstestprotokollierung](../test/modify-load-test-logging-settings.md)
- [Konfigurieren von Ports für Testcontroller und Test-Agents](../test/configure-ports-for-test-controllers-and-test-agents.md)