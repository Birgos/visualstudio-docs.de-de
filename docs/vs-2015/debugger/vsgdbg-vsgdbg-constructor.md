---
title: 'Vsgdbg:: Vsgdbg (Konstruktor) | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 670651e6-5e79-4845-b0c2-671beb7055a8
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 056c5f5e19a4d1e025969aa40ad75f3852b4201b
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2018
ms.locfileid: "51781919"
---
# <a name="vsgdbgvsgdbg-constructor"></a>VsgDbg::VsgDbg (Konstruktor)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Erstellt eine Instanz der `VsgDbg`-Klasse mit oder ohne das Vorbereiten einer In-App-Komponente der Grafikdiagnose, um Grafikinformationen standardmäßig aktiv zu erfassen und aufzuzeichnen, basierend auf dem angegebenen booleschen Parameter.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
VsgDbg(  
  bDefaultInit  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `bDefaultInit`  
 `true`, um anzugeben, dass die In-App-Komponente der Grafikdiagnose vorbereitet werden muss, um aktiv Grafikinformationen zu erfassen und aufzuzeichnen; `false`, um anzugeben, dass die In-App-Komponente der Grafikdiagnose nicht vorbereitet werden soll, um zu diesem Zeitpunkt aktiv Grafikinformationen zu erfassen und aufzuzeichnen.  
  
## <a name="remarks"></a>Hinweise  
 Wenn der Konstruktor aufgerufen wird, mit `bDefaultInit` festgelegt `true`, richtet sich der Dateiname der grafikprotokolldatei an, wie die `DONT_SAVE_VSGLOG_TO_TEMP` und `VSG_DEFAULT_RUN_FILENAME` Präprozessorsymbole definiert sind, bevor `vsgcapture.h` befindet sich in Ihrer app.  
  
 Wenn der Konstruktor mit `bDefaultInit` festgelegt auf `false` aufgerufen wird, kann die In-App-Komponente der Grafikdiagnose vorbereitet werden, um Grafikinformationen zu einem späteren Zeitpunkt aktiv zu erfassen und aufzuzeichnen, indem die `Init`-Funktion aufgerufen wird.  
  
## <a name="see-also"></a>Siehe auch  
 [VsgDbg:: ~ VsgDbg (Destruktor)](../debugger/vsgdbg-tilde-vsgdbg-destructor.md)   
 [Init](../debugger/init.md)   
 [DONT_SAVE_VSGLOG_TO_TEMP](../debugger/dont-save-vsglog-to-temp.md)   
 [VSG_DEFAULT_RUN_FILENAME](../debugger/vsg-default-run-filename.md)



