---
title: 'Vorgehensweise: Öffnen von projektspezifischen Editoren | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- project types, opening a project-specific editor
- editors [Visual Studio SDK], opening project-specific editors
- projects [Visual Studio SDK], opening folders
ms.assetid: 83e56d39-c97b-4c6b-86d6-3ffbec97e8d1
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 52d1fda1c3a1c2e8aac116c52afc8bf6738e23ea
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51817671"
---
# <a name="how-to-open-project-specific-editors"></a>Vorgehensweise: Öffnen von projektspezifischen Editoren
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Wenn eine Elementdatei, die von einem Projekt geöffnet wird systemintern auf den bestimmten Editor für das Projekt gebunden ist, muss das Projekt die Datei öffnen, mit einem projektspezifischen-Editor. Die Datei kann nicht auf den Mechanismus der IDE für das Auswählen eines Editors delegiert werden. Anstatt einen standard-Bitmap-Editor zu verwenden, können Sie z. B. diese projektspezifischer Editor-Option verwenden, an einem bestimmten Bitmap-Editor, der Informationen in der Datei, die dem Projekt eindeutig ist, erkennt.  
  
 Die IDE-Aufrufe der <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.OpenItem%2A> Methode, wenn er feststellt, dass eine Datei von einem bestimmten Projekt geöffnet werden soll. Weitere Informationen finden Sie unter [Anzeigen von Dateien mithilfe des Befehls der geöffneten Datei](../extensibility/internals/displaying-files-by-using-the-open-file-command.md). Verwenden Sie die folgenden Richtlinien zum Implementieren der `OpenItem` Methode, um Ihr Projekt eine Datei mit einem projektspezifischen-Editor zu öffnen.  
  
### <a name="to-implement-the-openitem-method-with-a-project-specific-editor"></a>So implementieren Sie die OpenItem-Methode mit einem projektspezifischen editor  
  
1.  Rufen Sie die <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.FindAndLockDocument%2A> Methode (RDT_EditLock), um zu bestimmen, ob die Datei (dokumentdatenobjekt) bereits geöffnet ist.  
  
    > [!NOTE]
    >  Weitere Informationen zu Dokumentdaten und dokumentenansichtsobjekten finden Sie unter [Dokumentdaten und Dokumentansicht in benutzerdefinierten Editoren](../extensibility/document-data-and-document-view-in-custom-editors.md).  
  
2.  Wenn die Datei bereits geöffnet ist, diesem die Datei durch Aufrufen der <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.IsDocumentOpen%2A> -Methode und geben einen Wert von IDO_ActivateIfOpen für den `grfIDO` Parameter.  
  
     Wenn die Datei geöffnet ist, und das Dokument von einem anderen Projekt als dem aufrufenden Projekt gehört, wird eine Warnung, die dem Benutzer angezeigt werden, die der Editor geöffnet wird aus einem anderen Projekt ist. Fenster "Datei" wird dann angezeigt.  
  
3.  Wenn Ihr Textpuffer (dokumentdatenobjekt) bereits geöffnet ist, und Sie eine andere Ansicht anfügen möchten, sind Sie verantwortlich für das Einbinden dieser Ansicht. Die empfohlene Vorgehensweise für das Instanziieren einer Ansicht (dokumentenansichtsobjekt) aus dem Projekt, lautet wie folgt aus:  
  
    1.  Rufen Sie `QueryService` auf die <xref:Microsoft.VisualStudio.Shell.Interop.SLocalRegistry> Dienst um einen Zeiger auf die <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2> Schnittstelle.  
  
    2.  Rufen Sie die <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance%2A> Methode, um eine Instanz der Ansichtsklasse Dokument zu erstellen.  
  
4.  Rufen Sie die <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.CreateDocumentWindow%2A> Methode, geben Sie Ihrem dokumentenansichtsobjekt.  
  
     Diese Methode Standorte das dokumentenansichtsobjekt in einem Dokumentfenster angezeigt.  
  
5.  Führen Sie die entsprechenden Aufrufe an die <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.InitNew%2A> oder <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.Load%2A> Methoden.  
  
     An diesem Punkt sollte die Ansicht vollständig initialisiert und bereit, die geöffnet werden.  
  
6.  Rufen Sie die <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show%2A> Methode zum Anzeigen und öffnen Sie die Ansicht.  
  
## <a name="see-also"></a>Siehe auch  
 [Sie öffnen und Speichern von Projektelementen](../extensibility/internals/opening-and-saving-project-items.md)   
 [Vorgehensweise: Öffnen Sie die Standard-Editoren](../extensibility/how-to-open-standard-editors.md)   
 [Gewusst wie: Öffnen von Editoren für geöffnete Dokumente](../extensibility/how-to-open-editors-for-open-documents.md)

