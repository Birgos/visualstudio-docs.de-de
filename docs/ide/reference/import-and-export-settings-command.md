---
title: Befehl Einstellungen importieren und exportieren
ms.date: 11/21/2018
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- Tools.ImportandExportSettings
helpviewer_keywords:
- Tools.ImportandExportSettings
- Import and Export Settings command
ms.assetid: 94a06468-a44d-403d-a931-77bbc9d06e56
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f5c011c1bbaaa66e3da39c7ca8d713099d11e5a4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55041684"
---
# <a name="import-and-export-settings-command"></a>Befehl Einstellungen importieren und exportieren

Importiert oder exportiert Visual Studio-Einstellungen oder setzt diese zurück.

## <a name="syntax"></a>Syntax

```cmd
Tools.ImportandExportSettings [/export:filename | /import:filename | /reset]
```

## <a name="switches"></a>Schalter

/export:`filename`

Dies ist optional. Exportiert die aktuellen Einstellungen in eine angegebene Datei

/import:`filename`

Dies ist optional. Importiert die aktuellen Einstellungen in eine angegebene Datei

/reset

Dies ist optional. Setzt die aktuellen Einstellungen zurück

## <a name="remarks"></a>Hinweise

Wenn Sie diesen Befehl ohne Schalter ausführen, wird der Assistent **Einstellungen importieren und exportieren** geöffnet. Weitere Informationen finden Sie unter [Synchronisieren der Einstellungen](../synchronized-settings-in-visual-studio.md) und [Umgebungseinstellungen](../environment-settings.md).

## <a name="example"></a>Beispiel

Der folgende Befehl exportiert die aktuellen Einstellungen in die Datei `MyFile.vssettings`:

```cmd
Tools.ImportandExportSettings /export:"c:\Files\MyFile.vssettings"
```

## <a name="see-also"></a>Siehe auch

- [Umgebungseinstellungen](../../ide/environment-settings.md)
- [Synchronisieren der Einstellungen](../../ide/synchronized-settings-in-visual-studio.md)
- [Personalisieren der Visual Studio-IDE](../../ide/personalizing-the-visual-studio-ide.md)
- [Visual Studio-Befehle](../../ide/reference/visual-studio-commands.md)