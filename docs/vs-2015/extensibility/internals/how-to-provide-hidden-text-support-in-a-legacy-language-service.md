---
title: 'Vorgehensweise: unterstützen der ausgeblendeten Text in einem Legacysprachdienst | Microsoft-Dokumentation'
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
- hidden text, supporting
- editors [Visual Studio SDK], hidden text
- language services, implementing hidden text regions
ms.assetid: 1c1dce9f-bbe2-4fc3-a736-5f78a237f4cc
caps.latest.revision: 22
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5d5451576115dcada98f6b8f7daaf1cca5a86f95
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51727241"
---
# <a name="how-to-provide-hidden-text-support-in-a-legacy-language-service"></a>Vorgehensweise: unterstützen der ausgeblendeten Text in einem Legacysprachdienst
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Sie können Regionen ausgeblendetem Text, zusätzlich zur konturenbereiche erstellen. Ausgeblendeten Text Regionen können Client-gesteuert oder Editor-gesteuert werden und werden verwendet, um einen Bereich des Texts ganz ausblenden. Der Editor zeigt einen ausgeblendeten Bereich als horizontale Linien an. Ein Beispiel hierfür ist, die nur Skript-Ansicht im HTML-Editor.  
  
## <a name="procedure"></a>Prozedur  
  
#### <a name="to-implement-a-hidden-text-region"></a>Um einen Bereich des ausgeblendeten Textes zu implementieren.  
  
1.  Rufen Sie `QueryService` für <xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager>.  
  
     Gibt einen Zeiger auf <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager>.  
  
2.  Rufen Sie <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession%2A>, und übergeben Sie einen Zeiger für einen angegebenen Textpuffer. Dadurch wird bestimmt, ob bereits eine Sitzung des ausgeblendeten Textes für den Puffer vorhanden ist.  
  
3.  Wenn bereits eine vorhanden ist, Sie müssen nicht zum Erstellen einer und einen Zeiger auf die vorhandene <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> Objekt zurückgegeben. Verwenden Sie diesen Zeiger, aufzulisten und zu ausgeblendeten Textbereiche erstellen. Rufen Sie andernfalls <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession%2A> um eine Sitzung des ausgeblendeten Textes für den Puffer zu erstellen.  
  
     Ein Zeiger auf die <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> Objekt zurückgegeben.  
  
    > [!NOTE]
    >  Beim Aufruf `CreateHiddenTextSession`, Sie können einen ausgeblendeten textclient angeben (d. h. <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextClient>). Der verborgene textclient benachrichtigt Sie ausgeblendeten Text oder Gliederung erweitert oder wird, durch den Benutzer reduziert.  
  
4.  Rufen Sie <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions%2A> , fügen Sie eine oder mehrere neue Kontur Regionen zu einem Zeitpunkt angeben der folgenden Informationen in den `reHidReg` (<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion>) Parameter:  
  
    1.  Geben Sie den Wert `hrtConcealed` in die `iType` Mitglied der <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> Struktur, um anzugeben, dass Sie einen Gliederungsbereich, anstatt einen ausgeblendeten Bereich erstellen.  
  
        > [!NOTE]
        >  Wenn verdeckten Regionen ausgeblendet sind, zeigt der Editor automatisch Zeilen in der ausgeblendeten Bereiche an, dass ihr Vorhandensein aus.  
  
    2.  Gibt an, ob der Bereich ist die Client-gesteuert oder Editor gesteuert werden, in der `dwBehavior` Mitglied der <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> Struktur. Die intelligente Gliederung Implementierung kann eine Mischung aus und Client-editorgesteuert Gliederung und ausgeblendeter Text Regionen enthalten.

