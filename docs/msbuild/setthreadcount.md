---
title: SetThreadCount | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
apiname:
- SetThreadCount
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- SetThreadCount
ms.assetid: 335335a5-8ca0-4e18-95f5-62aa6a691386
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2b4bfb8e1f60ed668039011841e12021e0f0702f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54942008"
---
# <a name="setthreadcount"></a>SetThreadCount
Legt die Anzahl der globalen Threads fest, und weist diese Anzahl für dem aktuellen Thread zu.  
  
## <a name="syntax"></a>Syntax  
  
```cmd  
HRESULT WINAPI SetThreadCount(int threadCount);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in] `threadCount`  
 Die Anzahl der zu verwendenden Threads.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein **HRESULT**, bei dem **SUCCEEDED** festgelegt ist, wenn die Anzahl der Threads aktualisiert wurde.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** *FileTracker.h*