---
title: Lokalisieren von ClickOnce-Anwendungen | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- WPF, ClickOnce applications
- ClickOnce deployment, globalization
- deploying applications [ClickOnce], localizing ClickOnce applications
- localization, ClickOnce deployment
- ClickOnce deployment, download on-demand
- ClickOnce deployment, localization
- Windows Forms, ClickOnce applications
- console applications, ClickOnce applications
ms.assetid: c92b193b-054d-4923-834b-d4226a4c7a1a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 784d4b6df24a5f4327a87c638b9624a0e4cec46c
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "53893596"
---
# <a name="localize-clickonce-applications"></a>Lokalisieren von ClickOnce-Anwendungen
Lokalisierung ist der Prozess, mit dem Sie die Anwendung an eine bestimmte Kultur anpassen. Dieser Prozess umfasst die Übersetzung des Textes der Benutzeroberfläche in eine regionsspezifische Sprache, die Verwendung der richtigen Datums- und Währungsformate, die Anpassung der Größe von Steuerelementen in einem Formular und, sofern erforderlich, die Spiegelung von Steuerelementen von rechts nach links.  
  
 Das Lokalisieren Ihrer Anwendung führt zur Erstellung von einer oder mehreren Satellitenassemblys. Jede Assembly enthält Benutzeroberflächenzeichenfolgen, Bilder und andere spezielle Ressourcen für eine bestimmte Kultur. (Die zentrale ausführbare Datei der Anwendung enthält die Zeichenfolgen für die Standardkultur für die Anwendung.)  
  
 In diesem Thema werden drei Möglichkeiten beschrieben, eine [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]-Anwendung für andere Kulturen bereitzustellen:  
  
-   Aufnehmen aller Satellitenassemblys in eine einzelne Bereitstellung.  
  
-   Generieren einer Bereitstellung für jede Kultur, mit jeweils einer einzelnen darin enthaltenen Satellitenassembly.  
  
-   Herunterladen von Satellitenassemblys bei Bedarf.  
  
## <a name="including-all-satellite-assemblies-in-a-deployment"></a>Aufnehmen aller Satellitenassemblys in eine einzelne Bereitstellung.  
 Anstatt mehrere [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]-Bereitstellungen zu veröffentlichen, können Sie eine einzelne [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]-Bereitstellung veröffentlichen, in der alle Satellitenassemblys enthalten sind.  
  
 Diese Methode ist die Standardmethode in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Um diese Methode in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] zu verwenden, sind keine weiteren Schritte erforderlich.  
  
 Zur Verwendung dieser Methode mit *MageUI.exe* müssen Sie die Kultur für die Anwendung in *MageUI.exe* auf **neutral** festlegen. Danach müssen alle Satellitenassemblys manuell in die Bereitstellung eingeschlossen werden. In *MageUI.exe* können Sie die Satellitenassemblys über die Schaltfläche **Auffüllen** auf der Registerkarte **Dateien** Ihres Anwendungsmanifests hinzufügen.  
  
 Der Vorteil dieses Ansatzes besteht darin, dass mit ihm eine einzelne Bereitstellung erstellt und der Verlauf der lokalisierten Bereitstellung vereinfacht wird. Zur Laufzeit wird die richtige Satellitenassembly verwendet, und zwar basierend auf der vom Benutzer für das Windows-Betriebssystem angegebenen Standardkultur. Ein Nachteil dieses Ansatzes besteht darin, dass bei jeder Installation oder jedem Update der Anwendung auf einem Clientcomputer alle Satellitenassemblys heruntergeladen werden. Wenn Ihre Anwendung eine große Zahl von Zeichenfolgen aufweist oder Ihre Kunden nur über eine langsame Netzwerkverbindung verfügen, kann dieser Prozess während des Anwendungsupdates zu Leistungseinbußen führen.  
  
> [!NOTE]
>  Für diesen Ansatz wird davon ausgegangen, dass Ihre Anwendung die Höhe, Breite und Position von Steuerelementen automatisch anpasst, um Textzeichenfolgen aufzunehmen, die in verschiedenen Kulturen unterschiedlich lang sind. Windows Forms enthält eine Vielzahl von Steuerelementen und Technologien, mit denen Sie Ihr Formular so entwerfen können, dass es problemlos lokalisiert werden kann. Dazu gehören die Steuerelemente <xref:System.Windows.Forms.FlowLayoutPanel> und <xref:System.Windows.Forms.TableLayoutPanel> sowie die <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft.  Weitere Informationen hierzu finden Sie auch unter [Gewusst wie: Unterstützen der Lokalisierung in Windows Forms mithilfe von AutoSize und dem TableLayoutPanel-Steuerelement](/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100)).  
  
## <a name="generate-one-deployment-for-each-culture"></a>Generieren einer Bereitstellung für jede Kultur  
 In dieser Bereitstellungsstrategie generieren Sie mehrere Bereitstellungen. Sie nehmen in jede Bereitstellung nur die Satellitenassembly auf, die für eine bestimmte Kultur benötigt wird, und kennzeichnen die Bereitstellung als die für diese Kultur spezifische Bereitstellung.  
  
 Um diese Methode in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] zu verwenden, legen Sie auf der Registerkarte **Veröffentlichen** die Eigenschaft **Sprache für Veröffentlichung** auf die gewünschte Region fest. [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] schließt automatisch die für die ausgewählte Region erforderliche Satellitenassembly ein und schließt alle anderen Satellitenassemblys aus der Bereitstellung aus.  
  
 Sie können die gleiche Aufgabe auch mit dem Tool *MageUI.exe* in Microsoft [!INCLUDE[winsdklong](../deployment/includes/winsdklong_md.md)] ausführen. Mit der Schaltfläche **Auffüllen** auf der Registerkarte **Dateien** des Anwendungsmanifests können Sie alle anderen Satellitenassemblys aus dem Anwendungsverzeichnis ausschließen. Anschließend legen Sie in *MageUI.exe* das Feld **Kultur** auf der Registerkarte **Name** für das Bereitstellungsmanifest fest. Auf diese Weise wird nicht nur die richtige Satellitenassembly eingeschlossen, sondern es wird auch das `language`-Attribut im `assemblyIdentity`-Element für das Bereitstellungsmanifest auf die entsprechende Kultur festgelegt.  
  
 Nachdem Sie die Anwendung veröffentlicht haben, müssen Sie diesen Schritt für jede zusätzliche Kultur wiederholen, die die Anwendung unterstützt. Achten Sie darauf, dass Sie jeweils in einem anderen Webserververzeichnis oder Dateifreigabeverzeichnis veröffentlichen, denn jedes Anwendungsmanifest verweist auf eine andere Satellitenassembly, und jedes Bereitstellungsmanifest hat einen anderen Wert für das `language`-Attribut.  
  
## <a name="download-satellite-assemblies-on-demand"></a>Herunterladen von Satellitenassemblys bei Bedarf  
 Wenn Sie alle Satellitenassemblys in eine einzelne Bereitstellung aufnehmen möchten, können Sie die Leistung mit Herunterladen bei Bedarf verbessern. Damit können Sie Assemblys als optional kennzeichnen. Die gekennzeichneten Assemblys werden nicht heruntergeladen, wenn die Anwendung installiert oder aktualisiert wird. Wenn Sie die Assemblys benötigen, können Sie sie durch Aufruf der <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroup%2A>-Methode in der <xref:System.Deployment.Application.ApplicationDeployment>-Klasse installieren.  
  
 Das Herunterladen von Satellitenassemblys bei Bedarf unterscheidet sich geringfügig vom Herunterladen anderer Typen von Assemblys bei Bedarf. Weitere Informationen und Codebeispiele zum Aktivieren dieses Szenarios mit dem [!INCLUDE[winsdkshort](../debugger/debug-interface-access/includes/winsdkshort_md.md)] -tools für [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)], finden Sie unter [Exemplarische Vorgehensweise: Herunterladen von Satellitenassemblys bei Bedarf mit der API für die ClickOnce-Bereitstellung  
  
 Sie können dieses Szenario auch in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] aktivieren.  Siehe auch [Exemplarische Vorgehensweise: Herunterladen von Satellitenassemblys bei Bedarf mit der API, die mithilfe des Designers für die ClickOnce-Bereitstellung](/previous-versions/visualstudio/visual-studio-2012/ms366788(v=vs.110)) oder [Exemplarische Vorgehensweise: Bedarfsgerechtes Herunterladen von Satellitenassemblys mit der API für die ClickOnce-Bereitstellung unter Verwendung des Designers  
  
## <a name="testing-localized-clickonce-applications-before-deployment"></a>Testen von lokalisierten ClickOnce-Anwendungen vor der Bereitstellung  
 Eine Satellitenassembly wird nur dann für eine Windows Forms-Anwendung verwendet, wenn für die <xref:System.Threading.Thread.CurrentUICulture%2A>-Eigenschaft für den Hauptthread der Anwendung die Kultur der Satellitenassembly festgelegt ist. Kunden auf den lokalen Märkten führen wahrscheinlich bereits eine lokalisierte Version von Windows aus, für deren Kultur der entsprechende Standardwert festgelegt ist.  
  
 Sie haben drei Optionen zum Testen lokalisierter Bereitstellungen, bevor Sie die Anwendung Kunden zur Verfügung stellen:  
  
- Sie können die [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]-Anwendung unter den entsprechenden lokalisierten Versionen von Windows ausführen.  
  
- Sie können die <xref:System.Threading.Thread.CurrentUICulture%2A>-Eigenschaft programmgesteuert in der Anwendung festlegen. (Diese Eigenschaft muss vor dem Aufrufen der <xref:System.Windows.Forms.Application.Run%2A>-Methode festgelegt werden.)  
  
## <a name="see-also"></a>Siehe auch  
 [\<AssemblyIdentity >-Element](../deployment/assemblyidentity-element-clickonce-deployment.md)   
 [ClickOnce-Sicherheit und -Bereitstellung](../deployment/clickonce-security-and-deployment.md)   
 [Globalisieren von Windows forms](/dotnet/framework/winforms/advanced/globalizing-windows-forms)