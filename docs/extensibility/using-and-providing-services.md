---
title: Verwenden und Bereitstellen von Diensten | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- examples [Visual Studio SDK], services
- Visual Studio, services
- services
ms.assetid: c0b415ba-b825-4da0-9faf-8a60a663e302
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e58ace81dbf3b39ed9e7707a50c1f7beae35e88f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54989272"
---
# <a name="using-and-providing-services"></a>Verwenden und Bereitstellen von Diensten
Ein Dienst ist ein Vertrag zwischen zwei VSPackages. Ein VSPackage bietet es sich um einen bestimmten Satz von Schnittstellen für einen anderen VSPackage zu nutzen. Z. B. [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] bietet die <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> service jedem VSPackage lädt. Dieser Dienst stellt die <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog> -Schnittstelle, die zum Schreiben in das Aktivitätsprotokoll verwendet werden kann. Weitere Informationen finden Sie unter [Vorgehensweise: Verwenden des Aktivitätsprotokolls](../extensibility/how-to-use-the-activity-log.md).  
  
 VSPackages können anbieten von Diensten, die Ihre eigenen durch die <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService> Schnittstelle...  
  
 Visual Studio bietet wichtige Dienste wie z. B. Folgendes an:  
  
|IDE-Dienst|Beschreibung|  
|-----------------|-----------------|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsShell>|Bietet Zugriff auf IDE Umgang mit grundlegenden Funktionen, die VSPackages und der Registrierung services.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell>|Bietet grundlegende fensterverwaltungsfunktionalität und UI-bezogene Funktionen in der IDE, z. B. die Fähigkeit zum Erstellen von Tools und Dokumentfenstern.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsSolution>|Bietet grundlegende Lösung bezogenen Funktionen, z.B. die Möglichkeit, Projekte auflisten, neue Projekte erstellen und Überwachen von Projekt wird geändert.|  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Dienstgrundlagen](../extensibility/internals/service-essentials.md)  
 Zeigt die wichtigen Elemente von Visual Studio-Dienst.  
  
 [Vorgehensweise: Abrufen eines Diensts](../extensibility/how-to-get-a-service.md)  
 Behandelt das anfordern (nutzen) eines Diensts.  
  
 [Vorgehensweise: Geben Sie einen Dienst](../extensibility/how-to-provide-a-service.md)  
 Erläutert, wie Sie einen Dienst bereitstellen.  
  
 [Vorgehensweise: Geben Sie einen asynchronen Visual Studio-Dienst](../extensibility/how-to-provide-an-asynchronous-visual-studio-service.md)  
 Erläutert, wie einen asynchronen Dienst bereitstellen.  
  
 [Vorgehensweise: Problembehandlung bei Diensten](../extensibility/how-to-troubleshoot-services.md)  
 Behandelt häufige Probleme und Lösungen dafür bietet.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Visual Studio SDK](../extensibility/visual-studio-sdk.md)