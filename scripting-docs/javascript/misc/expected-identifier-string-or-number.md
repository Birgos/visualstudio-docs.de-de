---
title: Bezeichner, Zeichenfolge oder Zahl erwartet | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT1028
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: f6bb8398-4fd6-4312-b4be-9617a2834cc4
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0ea67835a0c60d45d9e79f552183e0a4d6b677ac
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345239"
---
# <a name="expected-identifier-string-or-number"></a>Es wurde ein Bezeichner, eine Zeichenfolge oder eine Zahl erwartet
Sie verwendet falsche literalen Syntax zum Deklarieren eines Objekts in Literalen. Die Eigenschaften eines Objekts, das literal müssen es sich um einen Bezeichner, eine Zeichenfolge oder eine Zahl sein. Ein Objektliteral (auch als einen "Objektinitialisierer" bezeichnet) besteht aus einer durch Trennzeichen getrennte Liste von Eigenschaft-Wert-Paaren, die alle in Klammern eingeschlossen. Zum Beispiel:  
  
```JavaScript  
var point = {x:1.2, y:-3.4};  
```  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Stellen Sie sicher, dass Sie die richtige Syntax für Literale verwenden.  
  
## <a name="see-also"></a>Siehe auch  
 [Kommaoperator (,)](../../javascript/reference/comma-operator-decrement-javascript.md)