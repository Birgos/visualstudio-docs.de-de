---
title: Remotedebugger-download
description: Downloadlinks für den Remotedebugger
services: ''
author: mikejo5000
ms.service: ''
ms.topic: include
ms.date: 05/23/2018
ms.author: mikejo
ms.custom: include file
ms.openlocfilehash: 6c429614a094ceefc4f9a1e358ebc8ee26c40773
ms.sourcegitcommit: 1df0ae74af03bcf0244129a29fd6bd605efc9f61
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "50915170"
---
Klicken Sie auf dem Remotegerät oder Server, die Sie debuggen möchten, anstatt Visual Studio-Computers, herunterladen Sie und installieren Sie die richtige Version der Remotetools, über die Links in der folgenden Tabelle.

- Laden Sie die neuesten Remoteserver-Verwaltungstools für Ihre Version von Visual Studio herunter. Die neueste Version der Remotetools ist kompatibel mit früheren Versionen von Visual Studio, jedoch frühere Versionen der Remotetools nicht mit späteren Versionen von Visual Studio kompatibel sind. 
- Laden Sie die Remoteserver-Verwaltungstools mit derselben Architektur wie der Computer, der Sie sie auf installieren. Wenn Sie eine 32-Bit-app auf einem Remotecomputer unter einem 64-Bit-Betriebssystem debuggen möchten, installieren Sie z. B. die 64-Bit-Remoteserver-Verwaltungstools. 

|Version|Link|Hinweise|
|-|-|-|
|Visual Studio 2017 (neueste Version)|[Remotetools](https://visualstudio.microsoft.com/downloads/?q=remote+tools#remote-tools-for-visual-studio-2017)|Kompatibel mit allen Versionen von Visual Studio 2017. Laden Sie die Version, die übereinstimmende Ihr Betriebssystems des Geräts (x 86, X64 oder ARM64). Unter Windows Server finden Sie unter [entsperren Sie den Dateidownload](../../debugger/remote-debugging-unblock-file-download.md) Hilfe Herunterladen der Remoteserver-Verwaltungstools.|
|Visual Studio 2015|[Remotetools](https://my.visualstudio.com/Downloads?q=remote%20tools%20visual%20studio%202015)|Remotetools für Visual Studio 2015 sind My.VisualStudio.com verfügbar. Wenn Sie dazu aufgefordert werden, verknüpfen Sie die kostenlose [Visual Studio Dev Essentials](https://visualstudio.microsoft.com/dev-essentials/) -Programm, oder melden Sie sich mit Ihrem Visual Studio-Abonnement-ID. Unter Windows Server finden Sie unter [entsperren Sie den Dateidownload](../../debugger/remote-debugging-unblock-file-download.md) Hilfe Herunterladen der Remoteserver-Verwaltungstools.|
|Visual Studio 2013|[Remotetools](/previous-versions/visualstudio/visual-studio-2013/bt727f1t(v=vs.120)#Installing_the_Remote_Tools)|Download-Seite in Visual Studio 2013-Dokumentation|
|Visual Studio 2012|[Remotetools](/previous-versions/visualstudio/visual-studio-2012/bt727f1t(v=vs.110)#BKMK_Installing_the_Remote_Tools)|Download-Seite in Visual Studio 2012-Dokumentation|

Sie können den Remotedebugger ausführen, durch Kopieren *msvsmon.exe* auf dem Remotecomputer, anstatt die Remoteserver-Verwaltungstools installieren. Allerdings die Konfigurations-Assistenten (*rdbgwiz.exe*) steht nur, wenn Sie die Remoteserver-Verwaltungstools installieren. Sie müssen möglicherweise den Assistenten für die Konfiguration verwenden, wenn der Remotedebugger als Dienst ausgeführt werden sollen. Weitere Informationen finden Sie unter [(Optional) Konfigurieren des Remotedebuggers als Dienst](../../debugger/remote-debugging.md#bkmk_configureService).

>[!NOTE]
>- Verwenden Sie zum Debuggen von Windows 10-apps auf ARM-Geräten ARM64, die mit der neuesten Version der Remotetools verfügbar ist.  
>- Verwenden Sie zum Debuggen von Windows 10-apps auf Windows RT-Geräten, ARM, die nur in Visual Studio 2015 verfügbar ist, die zum Herunterladen der Remoteserver-Verwaltungstools.

