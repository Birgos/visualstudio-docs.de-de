---
title: AutoMark | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: c4de965e-0364-4f78-9936-1f509e85df74
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4fb849b43e21010d9183f53e31ccf6bbc70736b6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753465"
---
# <a name="automark"></a>AutoMark
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Die Option **AutoMark** gibt die Zeit in Millisekunden an, die für die Erfassung von Leistungsindikatorereignissen für Windows-Software beansprucht wird. Windows-Leistungsindikatoren werden in der Option **WinCounter** angegeben.  
  
 In der Befehlszeile kann nur eine **AutoMark**-Option angegeben werden. Bitte beachten Sie, dass das von **AutoMark** angegebene Samplingintervall **WinCounter** unabhängig vom Hauptsamplingintervall ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
VSPerfCmd.exe /Start:Method /WinCounter:Path /AutoMark:Milliseconds  
```  
  
#### <a name="parameters"></a>Parameter  
 `Milliseconds`  
 Gibt die Zeit in Millisekunden an, die für die Erfassungen von Windows-Leistungsindikatorereignissen beansprucht wird.  
  
## <a name="required-options"></a>Erforderliche Optionen  
 **WinCounter:** `Path`  
 Gibt den Windows-Leistungsindikator an, der erfasst werden soll. Wenn Sie die Instrumentierungsmethode verwenden, können Sie mehrere Windows-Indikatoren angeben. Wenn Sie die Samplingmethode verwenden, können Sie nur einen Software-Indikator angeben. Die Option **WinCounter** muss in einer Befehlszeile angegeben sein, die die Option **Start** enthält.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel ist ein Samplingintervall von 1000 ms für zwei Windows-Leistungsindikatoren festgelegt.  
  
```  
VSPerfCmd.exe /Start:Trace /Output:TestApp.exe.vsp /WinCounter:"\Process(*)\% Processor Time" /WinCounter:"\ASP.NET\Pages/sec" /AutoMark:1000  
VSPerfCmd.exe /Launch:TestApp.exe  
```  
  
## <a name="see-also"></a>Siehe auch  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profilerstellung für eigenständige Anwendungen](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profilerstellung für ASP.NET-Webanwendungen](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Erstellen von Dienstprofilen](../profiling/command-line-profiling-of-services.md)
