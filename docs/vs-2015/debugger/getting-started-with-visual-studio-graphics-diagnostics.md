---
title: Erste Schritte mit Visual Studio-Grafikdiagnose | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 59131181-1caa-4b7f-be4b-e84709634edf
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5f6b6bbb10113ab6bd97767f41991219e014d39a
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51725570"
---
# <a name="getting-started-with-visual-studio-graphics-diagnostics"></a>Erste Schritte mit Visual Studio-Grafikdiagnose
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

In diesem Abschnitt bereiten Sie sich auf die erstmalige Verwendung der Grafikdiagnose vor. Anschließend erfassen Sie Frames aus einer Direct3D-App und untersuchen diese in der Grafikanalyse.  
  
## <a name="requirements"></a>Anforderungen  
 Um die Grafikdiagnose in Visual Studio 2015 zu verwenden, müssen Sie eine dieser Editionen besitzen:  
  
- Visual Studio 2015 Enterprise  
  
- Visual Studio 2015 Professional  
  
- Visual Studio 2015 Community  
  
  [!INCLUDE[downloadvs](../includes/downloadvs-md.md)]  
  
### <a name="windows-10-prerequisites"></a>Erforderliche Komponenten für Windows 10  
 Die optionale Windows-Funktion *Grafiktools* bietet die Infrastruktur, Erfassung und Wiedergabe, die Grafikdiagnose in Windows 10 erforderlich ist.  
  
 Informationen zum Installieren von Grafiktools finden Sie unter [installieren Sie Grafiktools für Windows 10](#InstallGraphicsTools).  
  
### <a name="windows-81-prerequisites"></a>Erforderliche Komponenten für Windows 8.1  
 Das Windows Software Development Kit (SDK) für Windows 8.1 bietet die Infrastruktur für die Erfassung und Wiedergabe, die für die Grafikdiagnose unter Windows 8.1 erforderlich ist, und unterstützt die Entwicklung für Windows 8.1 und Windows 8.  
  
 [Das Windows Software Development Kit (SDK) für Windows 8.1 herunterladen](https://msdn.microsoft.com/windows/desktop/bg162891.aspx)  
  
 Um einen Remotewiedergabecomputer zu verwenden, der Windows 10 in einem Entwicklungscomputer mit Windows 8.1 ausführt, müssen Sie auf dem Entwicklungscomputer das Windows 10-SDK und auf dem Wiedergabecomputer die optionale Grafiktools-Funktion installieren.  
  
##  <a name="InstallGraphicsTools"></a> Installieren von Grafiktools für Windows 10  
 Die Grafikdiagnose-Infrastruktur dient in Windows 10 durch eine optionale Funktion von Windows aufgerufen *Grafiktools*. Diese Funktion ist erforderlich, um Grafikinformationen in Windows 10 zu erfassen und wiederzugeben, unabhängig davon, ob die erfasste App eine frühere Windows-Version als Ziel hat oder welche Direct3D-Version verwendet wird. Sie können die Grafiktools-Funktion auch vorab installieren. Andernfalls wird sie bei Bedarf installiert, wenn Sie das erste Mal eine Grafikdiagnosesitzung in Visual Studio starten.  
  
#### <a name="to-install-graphics-tools-for-windows-10"></a>So installieren Sie Grafiktools für Windows 10  
  
1. Auf der **starten** Menü wählen **Einstellungen**. Die **Einstellungen** Dialogfeld wird angezeigt.  
  
2. In der **Einstellungen** Dialogfeld Wählen Sie **System**, und wählen Sie dann **installierte apps** aus der Liste der Systemeinstellungen.  
  
3. Auf der rechten Seite des der **Einstellungen** Dialogfeld Wählen Sie **optionale Features verwalten** unter **apps und Features installiert**. Die **optionale Features verwalten** Dialogfeld wird angezeigt.  
  
4. In der **optionale Features verwalten** Dialogfeld Wählen Sie **Hinzufügen einer Funktion**. Eine Liste der optionalen Funktionen, die Sie installieren können, wird angezeigt.  
  
5. Wählen Sie **Grafiktools** aus der Liste der Features, und wählen Sie dann **installieren**.  
  
   Die Funktion „Grafiktools“ wird auch automatisch bei der Installation des Windows 10-SDK installiert.  
  
> [!TIP]
>  Die optionale Grafiktools-Funktion von Windows 10 bietet einfache Erfassung und Wiedergabe-Funktionen – wie z. B. das befehlszeilenerfassungsprogramm **dxcap.exe**–, die verwendet werden kann, in der Unterstützung, testen und diagnoseszenarien auf Computer, in dem Entwickler-Tools installiert sind. Weitere Informationen finden Sie unter den [Befehlszeilen-Erfassungs-Tool](../debugger/command-line-capture-tool.md) Thema.  
  
## <a name="using-graphics-diagnostics-for-the-first-time"></a>Erstmaliges Verwenden der Grafikdiagnose  
 Nun, da Sie alles haben, was Sie brauchen, können Sie mit der Verwendung der Grafikdiagnose beginnen. Führen Sie folgende Schritte aus:  
  
### <a name="1---create-a-direct3d-app"></a>1. Erstellen einer Direct3D-App  
 Wenn Sie bereits Ihre eigene Direct3D-App zum Entdecken der Grafikdiagnose haben, ist das eine gute Voraussetzung. Andernfalls können Sie eines der in der Code Gallery verfügbaren Direct3D-Beispiele verwenden.  
  
- Um die Grafikdiagnose mit Direct3D 12 in Windows 10 mithilfe von Visual Studio 2015 zu testen, versuchen Sie es der [Direct3D 12 UAP-Beispiel](https://code.msdn.microsoft.com/Direct3D-12-UAP-Sample-ecb1779f) für Windows 10.  
  
- Um die Grafikdiagnose mit Direct3D 11 unter Windows 10 oder Windows 8.1 zu testen, können Sie die **DirectX-App (Windows universell)** oder **DirectX-App (Windows 8.1)** -Projektvorlagen. Oder, um etwas interessanteres, versuchen Sie es der [DirectX marble Maze-Beispielspiel](https://code.msdn.microsoft.com/windowsapps/DirectX-Marble-Maze-Game-e4806345) für Windows 8.1.  
  
  Stellen Sie sicher, dass Sie die App erstellen können, bevor Sie fortfahren.  
  
### <a name="2---start-a-graphics-diagnostics-session"></a>2. Starten einer Grafikdiagnosesitzung  
 Nun können Sie mit Ihrer ersten Grafikdiagnosesitzung beginnen. Wählen Sie in Visual Studio im Hauptmenü **Debuggen, Grafiken, Diagnose starten**, oder drücken Sie **Alt + F5**. Daraufhin wird Ihre App unter „Grafikdiagnose“ gestartet, und das Fenster für die Diagnosesitzung wird in Visual Studio angezeigt.  
  
> [!IMPORTANT]
>  Wenn Sie Ihre App in Windows 10 ausführen und die optionale Grafiktools-Funktion noch nicht installiert wurde, werden Sie aufgefordert, dies jetzt nachzuholen. Sie müssen diese installieren, bevor Sie die Grafikdiagnose in Windows 10 verwenden können.  
  
### <a name="3---capture-frames"></a>3. Erfassen von Frames  
 Sie können Frames erfassen, sobald die App gestartet wird.  
  
##### <a name="to-capture-single-frames"></a>So erfassen Sie einzelne Frames  
  
-   Wählen Sie in Visual Studio die **Frame erfassen** Schaltfläche der Symbolleiste oder die Diagnose Sitzung Grafikfenster. Oder, wenn Ihre app den Fokus besitzt, drücken Sie einfach **Druck**.  
  
##### <a name="to-capture-a-sequence-of-frames"></a>So erfassen Sie eine Sequenz von Frames  
  
- Legen Sie in Visual Studio im Fenster diagnosesitzung **zu erfassende Frames** auf die Anzahl der Frames, die Sie in einer Sequenz erfassen möchten, erfassen Sie Sie anschließend die Sequenz mit einer der oben zum Erfassen einzelner Frames beschriebenen Methoden.  
  
   Um einzelne Frames erneut zu erfassen, legen Sie **zu erfassende Frames** zu `1`.  
  
  Wenn Sie nur Erfassen von Frames fertig sind, beenden Sie die app, oder wählen Sie die **beenden** Schaltfläche aus der Grafik-Symbolleiste oder im Fenster diagnosesitzung.  
  
### <a name="4--examine-captured-frames-in-the-graphics-analyzer"></a>4. Untersuchen von erfassten Frames in der Grafikanalyse  
 Sie können nun die Frames überprüfen, die Sie gerade erfasst haben. Um die Analyse eines Frames zu starten, wählen Sie im Fenster für die Diagnosesitzung die Framenummer des Frames aus, den Sie untersuchen möchten. Daraufhin wird den Frame in der **Grafikanalyse**, können die Grafikdiagnose-Tools verwenden, überprüfen Sie, wie Ihre app Direct3D verwendet, um Renderingprobleme, oder verwenden Sie die **Frame-Analyse** Tools Verstehen der Leistung.  
  
 Wenn Sie im Fenster für die Diagnosesitzung den falschen Frame ausgewählt haben oder Sie einen anderen Frame untersuchen möchten, können Sie einen neuen Frame in der Grafikanalyse auswählen. Auf der **Renderziel** Registerkarte des grafikprotokollfensters unter dem renderzielbild, erweitern Sie die **Frameliste** und wählen Sie dann auf einen anderen Frame untersuchen.  
  
 Weitere Informationen zur Verwendung der Grafikanalyse-Tools zusammen verwenden, finden Sie unter den [Beispiele](../debugger/graphics-diagnostics-examples.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Direct3D 12-Grafiken](http://msdn.microsoft.com/en-us/52094ae3-3b44-4689-9ee7-1ba1b3a779cb)






