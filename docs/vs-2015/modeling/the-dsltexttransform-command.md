---
title: Der DslTextTransform-Befehl | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Domain-Specific Language, commands
ms.assetid: 7d025d0b-6543-4a49-9f6b-8b8cfcad77ee
caps.latest.revision: 32
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 882d2c8d0dec5e4673b24436067bd6255c2052be
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2018
ms.locfileid: "49853154"
---
# <a name="the-dsltexttransform-command"></a>Der DslTextTransform-Befehl
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

DslTextTransform.cmd ist es sich um ein Skript, das Aufrufe TextTransform.exe mit allgemeinen Optionen ausführt. Können Sie DslTextTransformation.cmd einen nächtlichen Buildvorgang von Automatisieren Ihrer [!INCLUDE[dsl](../includes/dsl-md.md)] Projekte. Weitere Informationen finden Sie unter [Generieren von Dateien mit dem TextTransform-Hilfsprogramm](../modeling/generating-files-with-the-texttransform-utility.md).  
  
 DslTextTransform.cmd befindet sich im folgenden Verzeichnis:  
  
 **\<Visual Studio SDK-Installationspfad > \VisualStudioIntegration\Tools\Bin**  
  
 Sie können die folgenden Argumente als Eingabe für DslTextTransform.cmd angeben:  
  
- Das Ausgabeverzeichnis des modellprojekts Domäne.  
  
- Das Ausgabeverzeichnis des Projekts Designer Definition.  
  
- Der Speicherort der Textvorlagendatei.  
  
  DslTextTransform.cmd verarbeitet die angegebene Vorlage Textdatei mit dem Standard-anweisungsprozessoren und Assemblys. Wenn Sie benutzerdefinierte anweisungsprozessoren erstellen, können Sie Ihre eigenen Batch-Datei erstellen, die TextTransform.exe aufruft. In dieser Batchdatei können Sie Ihre Assemblys und die zugeordnete benutzerdefinierten anweisungsprozessoren angeben.



