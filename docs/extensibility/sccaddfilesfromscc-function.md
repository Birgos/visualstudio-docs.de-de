---
title: SccAddFilesFromSCC-Funktion | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccAddFilesFromSCC
helpviewer_keywords:
- SccAddFilesFromSCC function
ms.assetid: f21a3500-ade8-4dd8-8647-10e2179be9c1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e3837ea9773d9deba089da2f7d9ef2541fdc3c31
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55026931"
---
# <a name="sccaddfilesfromscc-function"></a>SccAddFilesFromSCC-Funktion
Diese Funktion hinzugefügt den aktuell geöffneten Projekt eine Liste von Dateien aus der quellcodeverwaltung.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
SCCRTN SccAddFilesFromSCC(  
   LPVOID  pContext,  
   HWND    hWnd,  
   LPSTR   lpUser,  
   LPSTR   lpAuxProjPath,  
   LONG    cFiles,  
   LPCSTR* lpFilePaths,  
   LPCSTR  lpDestination,  
   LPCSTR  lpComment,  
   LPBOOL  pbResults  
);  
```  
  
### <a name="parameters"></a>Parameter  
 "pContext"  
 [in] Der Datenquellen-Steuerelement-Plug-in Kontextzeiger.  
  
 hWnd  
 [in] Ein Handle für das IDE-Fenster, das das Quellcodeverwaltungs-Plug-in als übergeordnetes Element für alle Dialogfelder verwenden kann, die er bereitstellt.  
  
 lpUser  
 [in, out] Der Benutzername (bis zu SCC_USER_SIZE, einschließlich des null-Abschlusszeichens).  
  
 lpAuxProjPath  
 [in, out] Zusätzliche Zeichenfolge, die zur Identifizierung des Projekts (bis zu `SCC_PRJPATH_`Größe, einschließlich des null-Abschlusszeichens).  
  
 cFiles  
 [in] Anzahl der Dateien, die vom `lpFilePaths`.  
  
 lpFilePaths  
 [in, out] Array von Dateinamen, die dem aktuellen Projekt hinzufügen.  
  
 lpDestination  
 [in] Der Zielpfad, wo sind die Dateien geschrieben werden.  
  
 lpComment  
 [in] Der Kommentar, der auf jede der hinzugefügten Dateien angewendet werden.  
  
 pbResults  
 [in, out] Array von Flags, die auf Erfolg (ungleich NULL oder "true") festgelegt ist oder Fehler (0 (null) oder "false") für jede Datei (Größe des Arrays muss mindestens `cFiles` lang).  
  
## <a name="return-value"></a>Rückgabewert  
 Die Source-Steuerelement-Plug-in-Implementierung dieser Funktion muss einen der folgenden Werte zurückgeben:  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|SCC_E_PROJNOTOPEN|Projekt kann nicht geöffnet werden.|  
|SCC_E_OPNOTPERFORMED|Es ist keine Verbindung zum gleichen Projekt gemäß `lpAuxProjPath.`|  
|SCC_E_NOTAUTHORIZED|Benutzer ist nicht autorisiert, auf die Datenbank zu aktualisieren.|  
|SCC_E_NONSPECIFICERROR|Unbekannter Fehler.|  
|SCC_I_RELOADFILE|Eine Datei oder ein Projekt muss neu geladen werden.|  
  
## <a name="see-also"></a>Siehe auch  
 [Datenquellen-Steuerelement-Plug-in-API-Funktionen](../extensibility/source-control-plug-in-api-functions.md)