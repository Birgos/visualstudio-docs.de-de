---
title: Punkt-, bilineare, trilineare und anisotrope Texturfiltervarianten | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 57d14fc9-b5f7-45ee-9717-48086886742d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 26f258290b457493a9e17f4bcdab3ffe06160d74
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55025932"
---
# <a name="point-bilinear-trilinear-and-anisotropic-texture-filtering-variants"></a>Punkt-, bilineare, trilineare und anisotrope Texturfiltervarianten
Überschreibt den Filterungsmodus auf passenden Textursamplern.  
  
## <a name="interpretation"></a>Interpretation  
 Verschiedene Textursampling-Methoden bringen verschiedene Leistungskosten und Bildqualitäten. Folgende Filtermodi sind mit steigenden Kosten und höherer Bildqualität verbunden:  
  
1. Punktfilterung (am günstigen, schlechteste visuelle Qualität)  
  
2. Bilineare Filterung  
  
3. Trilineare Filterung  
  
4. Anisotrope Filterung (am teuersten, höchste visuelle Qualität)  
  
   Wenn die Leistungskosten jeder Variante mit intensiveren Filterungsmodi deutlich steigen, können Sie die Kosten gegen die höhere Bildqualität abwägen. Anhand dieser Bewertung können Sie dann höhere Leistungskosten für eine höhere visuelle Qualität oder eine niedrigere visuelle Qualität für eine höhere Rahmenrate oder für eine Leistung, die auf andere Weise nicht zu erreichen ist, akzeptieren.  
  
   Wenn die Leistungskosten keine Rolle spielen oder unabhängig vom Filtermodus gleich bleiben – z. B., wenn die GPU, die Sie anzielen, einen redundant hohen Shader-Durchsatz und eine hohe Bandbreite hat –, können Sie die anisotrope Filterung verwenden, um die beste Bildqualität in Ihrer App zu erreichen.  
  
## <a name="remarks"></a>Hinweise  
 Diese Varianten überschreiben die Samplerstatus in Aufrufen von `ID3D11DeviceContext::PSSetSamplers`, in denen eine der folgenden Filtermethoden für den von der Anwendung bereitgestellten Sampler verwendet wird:  
  
- `D3D11_FILTER_MIN_MAG_MIP_POINT`  
  
- `D3D11_FILTER_MIN_MAG_POINT_MIP_LINEAR`  
  
- `D3D11_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT`  
  
- `D3D11_FILTER_MIN_POINT_MAG_MIP_LINEAR`  
  
- `D3D11_FILTER_MIN_LINEAR_MAG_MIP_POINT`  
  
- `D3D11_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR`  
  
- `D3D11_FILTER_MIN_MAG_LINEAR_MIP_POINT`  
  
- `D3D11_FILTER_MIN_MAG_MIP_LINEAR`  
  
- `D3D11_FILTER_ANISOTROPIC`  
  
  In der Variante **Punkttexturfilterung** wird der von der Anwendung bereitgestellte Filtermodus durch `D3D11_FILTER_MIN_MAG_MIP_POINT` ersetzt, in der Variante **Bilineare Texturfilterung** wird er durch `D3D11_FILTER_MIN_MAG_LINEAR_MIP_POINT` ersetzt, und in der Variante **Trilineare Texturfilterung** wird er durch `D3D11_FILTER_MIN_MAG_MIP_LINEAR` ersetzt.  
  
  In der **anisotropen Texturfilterung** wird der von der Anwendung bereitgestellte Filtermodus durch `D3D11_FILTER_ANISOTROPIC` ersetzt, und die maximale Anisotropie wird auf 16 gesetzt.  
  
## <a name="restrictions-and-limitations"></a>Einschränkungen  
 In Direct3D bedeutet die Funktionsebene 9.1 eine maximale Anisotropie von 2x. Da die Variante **Anisotrope Texturfilterung** versucht, die 16-fache Anisotropie exklusiv zu verwenden, ist die Wiedergabe nicht möglich, wenn die Frameanalyse auf einem Gerät mit dem Funktionslevel 9.1 durchgeführt wird. Zu den heutigen Geräten, die von dieser Einschränkung betroffen sind, gehören die ARM-basierten Windows-Tablets Surface RT und Surface 2. Ältere GPUs, die auf einigen Computern immer noch zu finden sind, können ebenso betroffen sein, aber dies gilt hauptsächlich für Computer, die als veraltet betrachtet werden und immer weniger in Gebrauch sind.  
  
## <a name="example"></a>Beispiel  
 Die Variante **Punkttexturfilterung** kann durch Verwendung eines Codes reproduziert werden, der dem folgenden ähnlich ist:  
  
```cpp
D3D11_SAMPLER_DESC sampler_description;  
  
// ... other sampler description setup ...  
  
sampler_description.Filter = D3D11_FILTER_MIN_MAG_MIP_POINT;  
  
d3d_device->CreateSamplerState(&sampler_desc, &sampler);  
d3d_context->PSSetSamplers(0, 1, &sampler  
```  
  
## <a name="example"></a>Beispiel  
 Die Variante **Bilineare Texturfilterung** kann durch Verwendung eines Codes reproduziert werden, der dem folgenden ähnlich ist:  
  
```cpp
D3D11_SAMPLER_DESC sampler_description;   
  
// ... other sampler description setup ...  
  
sampler_description.Filter = D3D11_FILTER_MIN_MAG_LINEAR_MIP_POINT;  
  
d3d_device->CreateSamplerState(&sampler_desc, &sampler);  
d3d_context->PSSetSamplers(0, 1, &sampler  
```  
  
## <a name="example"></a>Beispiel  
 Die Variante **Trilineare Texturfilterung** kann durch Verwendung eines Codes reproduziert werden, der dem folgenden ähnlich ist:  
  
```cpp
D3D11_SAMPLER_DESC sampler_description;   
  
// ... other sampler description setup ...  
  
sampler_description.Filter = D3D11_FILTER_MIN_MAG_MIP_LINEAR;  
  
d3d_device->CreateSamplerState(&sampler_desc, &sampler);  
d3d_context->PSSetSamplers(0, 1, &sampler  
```  
  
## <a name="example"></a>Beispiel  
 Die Variante **Anisotrope Texturfilterung** kann durch Verwendung eines Codes reproduziert werden, der dem folgenden ähnlich ist:  
  
```cpp
D3D11_SAMPLER_DESC sampler_description;   
  
// ... other sampler description setup ...  
  
sampler_description.Filter = D3D11_FILTER_ANISOTROPIC;  
sampler_description.MaxAnisotropy = 16;  
  
d3d_device->CreateSamplerState(&sampler_desc, &sampler);  
d3d_context->PSSetSamplers(0, 1, &sampler  
```
