---
title: '&lt;Beschreibung&gt; -Element (ClickOnce-Bereitstellung) | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#description
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <description> element [ClickOnce deployment manifest]
ms.assetid: 18f6919e-a3ab-4942-a57d-167fabfac44e
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 8ddba6356ab051dbad27e55eefd53a517b47a21a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "49224769"
---
# <a name="ltdescriptiongt-element-clickonce-deployment"></a>&lt;Beschreibung&gt; -Element (ClickOnce-Bereitstellung)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Identifiziert Anwendungsinformationen, die zum Erstellen eines Shell-Eintrags verwendet und ein **Software** Element in der Systemsteuerung.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      <description   
   publisher   
   product  
   suiteName  
   supportUrl  
/>  
```  
  
## <a name="elements-and-attributes"></a>Elemente und Attribute  
 Das `description` -Element ist erforderlich und befindet sich im `urn:schemas-microsoft-com:asm.v1` -Namespace. Es enthält keine untergeordneten Elemente und weist folgende Attribute.  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|`publisher`|Erforderlich. Identifiziert den Firmennamen, die verwendet werden, für die Platzierung von Symbol in der Windows **starten** Menü und die **Software** Element in der Systemsteuerung, wenn die Bereitstellung für die Installation konfiguriert ist.|  
|`product`|Erforderlich. Identifiziert den Namen der Vollversion des Produkts. Verwendet als Titel für das Symbol, das in der Windows **starten** Menü.|  
|`suiteName`|Dies ist optional. Identifiziert einen Unterordner in der `publisher` Ordner in der Windows **starten** Menü.|  
|`supportUrl`|Dies ist optional. Gibt an, eine Support-URL, die in angezeigt wird der **Software** Element in der Systemsteuerung. Eine Verknüpfung zu dieser URL wird auch erstellt, um Unterstützung in den Windows **starten** Menü, wenn die Bereitstellung für die Installation konfiguriert ist.|  
  
## <a name="remarks"></a>Hinweise  
 Das Description-Element ist in allen Konfigurationen der dienstbereitstellung erforderlich.  
  
## <a name="example"></a>Beispiel  
 Das folgende Codebeispiel veranschaulicht eine `description` Element in einer [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] Bereitstellungsmanifest. Dieses Codebeispiel ist Teil eines umfangreicheren Beispiels für die [ClickOnce-Bereitstellungsmanifest](../deployment/clickonce-deployment-manifest.md) Thema.  
  
```  
<description   
  asmv2:publisher="My Company Name"  
  asmv2:product="My Application"  
  xmlns="urn:schemas-microsoft-com:asm.v1" />  
```  
  
## <a name="see-also"></a>Siehe auch  
 [ClickOnce-Bereitstellungsmanifest](../deployment/clickonce-deployment-manifest.md)



