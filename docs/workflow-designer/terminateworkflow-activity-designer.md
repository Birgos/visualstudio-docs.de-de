---
title: Workflow-Designer - TerminateWorkflow-Aktivitätsdesigner
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.TerminateWorkflow.UI
ms.assetid: 08e632ed-0724-4fb4-9df1-f8d443eaf0ac
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3a065deebe0629cb353acc64d6d40db8a4e00b3d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54993259"
---
# <a name="terminateworkflow-activity-designer"></a>TerminateWorkflow-Aktivitätsdesigner

Die **TerminateWorkflow** Aktivitäts-Designer dient zum Erstellen und Konfigurieren einer <xref:System.Activities.Statements.TerminateWorkflow> Aktivität.

## <a name="the-terminateworkflow-activity"></a>Die TerminateWorkflow-Aktivität

Mit der <xref:System.Activities.Statements.TerminateWorkflow>-Aktivität können Sie die Ausführung eines Workflows beenden.

### <a name="using-the-terminateworkflow-activity-designer"></a>Verwenden des TerminateWorkflow-Aktivitätsdesigners

Die **TerminateWorkflow** Aktivitäts-Designer finden Sie in der **Runtime** Kategorie der **Toolbox**, die erfolgt durch Klicken auf die **Toolbox** Registerkarte (Wählen Sie alternativ **Toolbox** aus der **Ansicht** Menü- oder STRG + ALT + X.)

Die **TerminateWorkflow** Aktivitäts-Designer gezogen werden kann, aus der **Toolbox** und sich der Workflow-Designer-Oberfläche gelöscht werden, wo Aktivitäten normalerweise platziert werden, z. B. in einem <xref:System.Activities.Statements.Sequence>. Dies erstellt eine <xref:System.Activities.Statements.TerminateWorkflow> -Aktivität mit dem standardmäßigen **"DisplayName"** -Standardwert TerminateWorkflow. Die <xref:System.Activities.Activity.DisplayName%2A> kann im Header des bearbeitet werden die **TerminateWorkflow** Aktivitäts-Designer oder in der **"DisplayName"** Feld des Eigenschaftenrasters.

### <a name="the-terminateworkflow-properties"></a>Die TerminateWorkflow-Eigenschaften

In der folgenden Tabelle werden die <xref:System.Activities.Statements.TerminateWorkflow>-Eigenschaften aufgeführt, und es wird beschrieben, wie sie im Designer verwendet werden. Diese Eigenschaften können im Eigenschaftenraster bearbeitet werden, und einige davon können auf die Oberfläche des Workflow-Designer bearbeitet werden.

|Eigenschaftenname|Erforderlich|Verwendung|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Der Anzeigename der <xref:System.Activities.Statements.TerminateWorkflow>-Aktivität. Der Standardwert ist TerminateWorkflow. Obwohl der Anzeigename nicht unbedingt erforderlich ist, wird empfohlen, einen Anzeigenamen zu verwenden.|
|<xref:System.Activities.Statements.TerminateWorkflow.Exception%2A>|False|Die Ausnahme, die beim Beenden des Workflows ausgelöst werden soll. Legen Sie diese Eigenschaft im Eigenschaftenraster fest.|
|<xref:System.Activities.Statements.TerminateWorkflow.Reason%2A>|False|Die Ursache für das Beenden des Workflows. Legen Sie diese Eigenschaft im Eigenschaftenraster fest.|

## <a name="see-also"></a>Siehe auch

- [Laufzeit](../workflow-designer/runtime-activity-designers.md)
- [Persist](../workflow-designer/persist-activity-designer.md)