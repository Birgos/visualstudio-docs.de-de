---
title: Anpassen von Windows von Code mithilfe der Legacy-API | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - code windows
ms.assetid: 5328ab2f-55cb-4680-9744-ec79f55acd1b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 44ff4fb8a8a2e60b047361624ae805910906c19e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55022052"
---
# <a name="customize-code-windows-by-using-the-legacy-api"></a>Anpassen von Fenstern des Code mit der legacy-API
Ein Codefenster ist ein Dokument Window-Objekt, das eine oder mehrere Textansichten unterstützt. Die exakten Features eines Codefensters hängen von dem Dienst zugeordnete Sprache ab. Im Modus "Multiple Document Interface (MDI)" ist im Code-Fenster den MDI-Child-Rahmen.  
  
 Codefenster mit Sprachdienste gesteuert, und jeder Sprachdienst kann eigene Codefenster-Manager bereitstellen. Dadurch wird den Sprachdienst einen eigenen Zusatzelemente, die im Code-Fenster, z. B. Wellenlinien, Farbgebung und mehr hinzu. Weitere Informationen dazu, wie beim Erstellen eines Fensters Core finden Sie unter [instanziieren Sie die Kern-Editor, indem Sie die legacy-API](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md).  
  
 Ein Codefenster ist ein <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame> -Objekt, das eine Textansicht und alle Zusatzelemente, die im-Objekt positioniert ist. Wenn Sie im Code-Fenster während der Instanziierung des den Kern-Editor erstellen, kann der Sprachdienst Anfügen einer <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager> zum Code-Fenster, wie in der folgenden Abbildung gezeigt wird.  
  
 ![CodeWindow-Grafik](../extensibility/media/vscodewindow.gif "Vscodewindow")  
Codefenster  
  
 Der Sprachdienst den Codefenster-Manager implementiert und ist verantwortlich für die Verwaltung der Zusatzelemente, wie eine Dropdownleiste. Ruft der Code-Fenster die <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager.AddAdornments%2A> Methode während der Initialisierung der Code-Fenster. Wenn dieser Aufruf erfolgt, kann der Sprachdienst hinzufügen, eine Dropdownleiste oder eine Schaltflächenleiste (<xref:Microsoft.VisualStudio.TextManager.Interop.IVsButtonBarClient>) zum Code-Fenster.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 `Customizing Code Windows by Using the Legacy API`  
 Erläutert das Anpassen des Code-Fenster mit der legacy-API.  
  
 [Vorgehensweise: Hosten Sie einen Editor in einem anderen editor](../extensibility/how-to-host-an-editor-in-another-editor.md)  
 Erläutert, wie einen zweiten Redakteur in einem Editor-Fenster zu hosten.  
  
 [Vorgehensweise: Lösen Sie Ereignisse aus, wenn der Editor den Fokus verliert.](../extensibility/how-to-fire-events-when-the-editor-loses-focus.md)  
 Erläutert, wie eine Dokumentenansicht an ein dokumentdatenobjekt angefügt.  
  
## <a name="see-also"></a>Siehe auch  
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>   
 [Instanziieren Sie die Kern-Editor, indem Sie die legacy-API](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md)   
 [Access TheText-Ansicht mit der legacy-API](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)