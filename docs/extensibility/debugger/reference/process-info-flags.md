---
title: PROCESS_INFO_FLAGS | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- PROCESS_INFO_FLAGS
helpviewer_keywords:
- PROCESS_INFO_FLAGS enumeration
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1d3541355da9ea144129e730efe9876b4e6d642f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009569"
---
# <a name="processinfoflags"></a>PROCESS_INFO_FLAGS

Beschreibt, oder gibt die Eigenschaften eines Prozesses an.

## <a name="syntax"></a>Syntax

```cpp
enum enum_PROCESS_INFO_FLAGS { 
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,
   PIFLAG_PROCESS_STOPPED   = 0x00000004,
   PIFLAG_PROCESS_RUNNING   = 0x00000008,
};
typedef DWORD PROCESS_INFO_FLAGS;
```

```csharp
enum enum_PROCESS_INFO_FLAGS { 
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,
   PIFLAG_PROCESS_STOPPED   = 0x00000004,
   PIFLAG_PROCESS_RUNNING   = 0x00000008,
};
```

## <a name="members"></a>Member

PIFLAG_SYSTEM_PROCESS  
Gibt an, dass der Prozess ein Systemprozess ist.

PIFLAG_DEBUGGER_ATTACHED  
Gibt an, dass der Prozess von einem Debugger debuggt wird. Es ist möglicherweise eine [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] Debugger, oder es möglicherweise einige andere Debugger, z. B. WinDbg.

PIFLAG_PROCESS_STOPPED  
Gibt an, dass der Prozess beendet wird. Nur gültig, wenn `PIFLAG_DEBUGGER_ATTACHED` ist ebenfalls angegeben. In Visual Studio 2005 und höher verfügbar.

PIFLAG_PROCESS_RUNNING  
Gibt an, dass der Prozess ausgeführt wird. Nur gültig, wenn `PIFLAG_DEBUGGER_ATTACHED` ist ebenfalls angegeben. In Visual Studio 2005 und höher verfügbar.

## <a name="remarks"></a>Hinweise

Verwendet für die `Flags` Mitglied der [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) Struktur.

Diese Flags können kombiniert werden, mit einer bitweisen `OR`.

## <a name="requirements"></a>Anforderungen

Header: msdbg.h

Namespace: Microsoft.VisualStudio.Debugger.Interop

Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Siehe auch

[Enumerationen](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)