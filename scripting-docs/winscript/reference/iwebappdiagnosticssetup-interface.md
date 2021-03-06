---
title: IWebAppDiagnosticsSetup-Schnittstelle | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IWebAppDiagnosticsSetup Interface
ms.assetid: ec7359f2-633e-4d59-b64b-9cab0134dfd0
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fc29282ec9d00ff79131765d2bf294c54fa347c6
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344901"
---
# <a name="iwebappdiagnosticssetup-interface"></a>IWebAppDiagnosticsSetup-Schnittstelle
Diese Schnittstelle wird von einer PDM-Debug-Anwendung zum Erstellen von COM-Objekte in den Prozess, der debuggt wird, und Aktivieren der Diagnose für Web implementiert. Wenn das PDM Anwendung Objekt implementiert Debuggen [IObjectWithSite](http://go.microsoft.com/fwlink/?LinkId=232438), Internet Explorer ruft [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) auf, nachdem es erstellt wurde, und übergibt einen Verweis auf [IWebBrowser2](http://go.microsoft.com/fwlink/?LinkId=232449). Ruft eine WWA-Anwendung [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) und übergibt die WWA Schnittstelle IWebApplicationHost. Wenn [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) mit einem Wert ungleich NULL aufgerufen wurde [IWebAppDiagnosticsSetup::DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) "Wahr" zurückgegeben. Wenn nicht der Fall, gibt "false" zurück und Aufrufe von [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) fehl.  
  
> [!IMPORTANT]
>  `IWebAppDiagnosticsSetup` wird von PDM V11. 0 und höher implementiert. Gefunden in activdbg100.h.  
  
## <a name="methods"></a>Methoden  
 Diese Schnittstelle legt die folgenden Methoden.  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md)|Ruft ab, der Textdokumente, die vom angegebenen Filter ausgeblendet sind.|  
|[IWebAppDiagnosticsSetup::DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md)|Bestimmt, ob das angegebene Dokument zu einem der untergeordneten Knoten dieses Knotens gehört.|