---
title: Grafikdiagnosebeispiele | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 45dd86b2-801e-4b07-a8c4-7bd25641d7f8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2509b7e3c373cecfe5cd1554805554afbedd2b3f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999313"
---
# <a name="graphics-diagnostics-examples"></a>Grafikdiagnosebeispiele
In diesen Beispielen wird gezeigt, wie die [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]-Grafikdiagnose verwendet wird, um Renderingprobleme in DirectX-basierten Apps zu debuggen.  
  
## <a name="capturing-graphics-information"></a>Aufzeichnen von Grafikinformationen  
 Bevor Sie die Grafikdiagnose verwenden können, um Renderingprobleme in der App zu diagnostizieren, müssen Sie Grafikinformationen aus der App erfassen, während diese ausgeführt wird. Graphikinformationen können von einer lokal ausgeführten App oder von einer App erfasst werden, die auf einem Remotecomputer oder einem anderen Gerät läuft. In diesen exemplarischen Vorgehensweisen wird demonstriert, wie Sie manuell oder programmgesteuert Graphikinformationen aus einer App abrufen können:  
  
-   [Exemplarische Vorgehensweise: Aufzeichnen von Grafikinformationen](walkthrough-capturing-graphics-information.md)  
  
-   [Exemplarische Vorgehensweise: Programmgesteuertes Erfassen von Grafikinformationen](walkthrough-capturing-graphics-information-programmatically.md)  
  
## <a name="use-graphics-diagnostics-with-an-arm-based-device"></a>Verwendung der Grafikdiagnose mit einem ARM-basierten Gerät  
 Sie können die Grafikdiagnose verwenden, um Ihre Direct3D-App auf einem ARM-basierten Gerät durch Remotedebugging zu debuggen. Weitere Informationen finden Sie unter [Vorgehensweise: Verwenden der Grafikdiagnose mit einem ARM-Gerät](/visualstudio/debugger/graphics/graphics-diagnostics-examples).  
  
## <a name="playing-back-graphics-information"></a>Wiedergeben von Grafikinformationen  
 Wenn Sie Grafikinformationen aus einer ausgeführten App erfasst haben, können Sie die aufgezeichneten Ereignisse wiedergeben, um Renderingprobleme zu diagnostizieren. Für die Wiedergabe können der Entwicklungscomputer oder ein verbundener Remotecomputer bzw. ein verbundenes Remotegerät verwendet werden. Weitere Informationen finden Sie unter [Vorgehensweise: Ändern des Grafikdiagnose-Wiedergabecomputers](how-to-change-the-graphics-diagnostics-playback-machine.md).  
  
## <a name="debugging-missing-objects"></a>Debuggen fehlender Objekte  
 Ein fehlendes Objekt (oder fehlende Objekte) ist eines der häufigsten Renderingprobleme, auf die Grafikentwickler stoßen. Dieses Problems kann zu schwierig diagnostizieren sein, da es verschiedene Arten von Fehlern gibt, die ein scheinbares Verschwinden des Objekts verursachen können. Zu den typischen Ursachen für fehlende Objekts gehören ein falsch konfigurierter Gerätezustand, Probleme beim Transformieren der Objektgeometrie oder eine falsch konfigurierte Grafikpipeline.  
  
 Diese Szenarios veranschaulichen, wie Sie mithilfe der Grafikdiagnose ermitteln können, warum ein Objekt fehlt, und wie Sie den Code finden können, der dies verursacht.  
  
-   [Exemplarische Vorgehensweise: Fehlende Objekte durch Gerätestatus](walkthrough-missing-objects-due-to-device-state.md)  
  
-   [Exemplarische Vorgehensweise: Fehlende Objekte durch Vertex-Shading](walkthrough-missing-objects-due-to-vertex-shading.md)  
  
-   [Exemplarische Vorgehensweise: Fehlende Objekte durch falsch konfigurierte Pipeline](walkthrough-missing-objects-due-to-misconfigured-pipeline.md)  
  
## <a name="debugging-rendering-errors"></a>Debuggen von Renderingfehlern  
 Ein anderes häufiges Problem, auf das Grafikentwickler stoßen, sind Objekte, die nicht korrekt dargestellt werden. Diese Art des Problems kann schwierig zu diagnostizieren sein, da die Ursache für eine falsche Darstellung einerseits zwar sehr offensichtlich sein kann, z. B. die Bindung an eine falsche Textur, manchmal aber auch sehr subtil, z. B. ein Fehler im Shader-Code oder eine unerwartete Interaktion zwischen Shadern. Einige Probleme können durch eine Kombination von Fehlern verursacht werden.  
  
 Das folgende Szenario zeigt, wie Sie mithilfe der Grafikdiagnose nicht ganz so subtile Renderingprobleme finden können, die von einem geringfügigen Shader-Fehler verursacht werden:  
  
-   [Exemplarische Vorgehensweise: Debuggen von Renderingfehlern, die durch Schattierungen entstanden sind](walkthrough-debugging-rendering-errors-due-to-shading.md)  
  
## <a name="debugging-compute-shaders"></a>Debugging von Compute-Shadern  
 Mithilfe der Grafikdiagnose können Sie Compute-Shader-Kernels in DirectCompute debuggen, die falsche Ergebnisse generieren. Mit DirectCompute können Sie die Rechenleistung des GPUs verwenden, um Berechnungen für eine große Anzahl von Datenelementen parallel auszuführen. Bei bestimmten Problemen können Berechnungen durch Verwendung des GPUs sogar sehr viel schneller erfolgen, als durch Verwendung eines gut optimierten CPU-Codes. Herkömmliche Debugger können jedoch Code nicht erkennen, der auf dem GPU ausgeführt wird. Das Debuggen dieser Art von Code erfordert spezielle Tools, die häufig anbieterspezifisch sind, und sich möglicherweise nicht gut in Visual Studio integrieren lassen. Damit Compute-Shader-Debugging eine größere Konsistenz über verschiedene GPUs erzielt, zeichnet die Grafikdiagnose zusätzlich zu Direct3D-Rendereignissen auch DirectCompute-Dispatchereignisse auf. So können Sie Probleme in Ihrem Compute-Shader-Code mit den Ihnen vertrauten Tools debuggen.  
  
 Ein Szenario, das veranschaulicht, wie eine Simulationsproblem Debuggen, die durch einen Fehler im Compute-Shader verursacht wird, finden Sie unter [Exemplarische Vorgehensweise: Verwenden der Grafikdiagnose zum Debuggen eines Compute-Shaders](walkthrough-using-graphics-diagnostics-to-debug-a-compute-shader.md).