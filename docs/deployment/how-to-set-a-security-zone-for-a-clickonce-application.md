---
title: 'Vorgehensweise: Festlegen einer Sicherheitszone für eine ClickOnce-Anwendung | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, security settings
- code access security, ClickOnce applications
- security zones, ClickOnce applications
ms.assetid: d3dac454-518a-44d7-a76e-ccb7b9c3a150
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0da7c3d4129102339eaf74fac815f086e027a4f3
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54980673"
---
# <a name="how-to-set-a-security-zone-for-a-clickonce-application"></a>Vorgehensweise: Festlegen einer Sicherheitszone für eine ClickOnce-Anwendung
Beim Festlegen von Codezugriffssicherheits-Berechtigungen für eine ClickOnce-Anwendung müssen Sie mit einem Basissatz von Berechtigungen auf der Seite **Sicherheit** des **Projekt-Designer**beginnen.  
  
 In den meisten Fällen können Sie auch die Zone **Internet** mit einem begrenzten Satz von Berechtigungen oder die Zone **Lokales Intranet** mit einem umfangreicheren Satz von Berechtigungen wählen. Wenn die Anwendung benutzerdefinierte Berechtigungen erfordert, können Sie die Sicherheitszone **Benutzerdefiniert** wählen. Weitere Informationen zum Einstellen von Berechtigungen finden Sie unter [Vorgehensweise: Festlegen benutzerdefinierter Berechtigungen für eine ClickOnce-Anwendung](../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)  
  
### <a name="to-set-a-security-zone"></a>Festlegen eine Sicherheitszone  
  
1.  Klicken Sie bei ausgewähltem Projekt im **Projektmappen-Explorer**im Menü **Projekt** auf **Eigenschaften**.  
  
2.  Klicken Sie auf die Registerkarte **Sicherheit** .  
  
3.  Aktivieren Sie das Kontrollkästchen **ClickOnce-Sicherheitseinstellungen aktivieren** .  
  
4.  Wählen Sie das Optionsfeld **Teilweise vertrauenswürdige Anwendung** aus.  
  
     Die Steuerelemente im Abschnitt **ClickOnce-Sicherheitsberechtigungen** sind aktiviert.  
  
5.  Wählen Sie aus der Dropdownliste **Zone, aus der die Anwendung installiert wird** eine Sicherheitszone.  
  
## <a name="see-also"></a>Siehe auch  
 [Vorgehensweise: Festlegen benutzerdefinierter Berechtigungen für eine ClickOnce-Anwendung](../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)   
 [Sichern von ClickOnce-Anwendungen](../deployment/securing-clickonce-applications.md)   
 [Codezugriffssicherheit für ClickOnce-Anwendungen](../deployment/code-access-security-for-clickonce-applications.md)   
