---
title: Übersicht über N-Tier-Datenanwendungen
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- presentation tier
- middle tier
- data tier
- n-tier applications, about n-tier applications
ms.assetid: 1020581d-eaaa-41a2-aca4-bf4c212895f6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 41728d6a2070cfa58a7d94cc8c129720b97ea92f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54952651"
---
# <a name="n-tier-data-applications-overview"></a>Übersicht über n-schichtige Datenanwendungen
*N-schichtige* -datenanwendungen sind datenanwendungen, die in mehrere voneinander *Ebenen*. Sie werden auch "verteilte Anwendungen" oder "Anwendungen mit mehreren Ebenen" genannt, da die Verarbeitung auf voneinander unabhängige, auf Client und Server verteilte Ebenen aufgeteilt wird. Beim Entwickeln einer Anwendung, die auf Daten zugreift, sollten die verschiedenen Ebenen, aus denen die Anwendung besteht, klar getrennt sein.

Eine typische N-Tier-Anwendung besteht aus einer Präsentationsebene, einer mittleren Ebene und einer Datenebene. Die einfachste Möglichkeit zum Trennen der verschiedenen Ebenen einer N-Tier-Anwendung besteht im Erstellen separater Projekte für jede Ebene, die in der Anwendung enthalten sein soll. Beispielsweise könnte die Präsentationsebene eine Windows Forms-Anwendung sein, während die Datenzugriffslogik eine in der mittleren Ebene angesiedelte Klassenbibliothek ist. Weiterhin könnte die Präsentationslogik in der mittleren Ebene über einen Dienst mit der Datenzugriffsebene kommunizieren. Die Aufteilung der Anwendungskomponenten in verschiedene Ebenen erhöht die Verwaltbarkeit und die Skalierbarkeit der Anwendung.  Auf diese Weise wird das Einarbeiten neuer, eine einzelne Ebene betreffender Technologien vereinfacht, ein erneutes Entwerfen der Anwendung ist nicht notwendig. Außerdem werden vertrauliche Informationen von N-Tier-Anwendungen in der Regel in der mittleren Ebene gespeichert, die von der Präsentationsebene getrennt ist.

Visual Studio enthält zahlreiche Funktionen, die Entwicklern das Erstellen von N-Tier-Anwendungen erleichtern.

-   Das Dataset enthält eine **DataSet-Projekt** -Eigenschaft, die Ihnen ermöglicht, die das Dataset (Datenentitätsebene) und TableAdaptern (Datenzugriffsebene) in einzelne Projekte.

-   Die [LINQ to SQL-tools in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md) enthält Einstellungen, um den DataContext und Datenklassen in separaten Namespaces zu generieren. Dies ermöglicht eine logische Trennung von Datenzugriffs- und Datenentitätsebenen.

-   [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index) bietet die <xref:System.Data.Linq.Table%601.Attach%2A> -Methode, die Ihnen ermöglicht, der ein DataContext aus unterschiedlichen Ebenen in einer Anwendung vereinigt. Weitere Informationen finden Sie unter [N-schichtige und Remoteanwendungen mit LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql).

## <a name="presentation-tier"></a>Präsentationsebene
Die *Präsentationsebene* ist die Ebene, auf der Benutzer mit einer Anwendung interagieren. Sie enthält oft auch zusätzliche Anwendungslogik. Zu den typischen Komponenten einer Präsentationsebene gehören:

-   Komponenten zur Datenbindung, etwa <xref:System.Windows.Forms.BindingSource> und <xref:System.Windows.Forms.BindingNavigator>.

-   Objektdarstellungen von Daten, z. B. [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index) Entitätsklassen für die Verwendung in der Präsentationsebene.

Die Präsentationsebene greift der mittleren Ebene in der Regel mithilfe eines Dienstverweises auf (z. B. eine [Windows Communication Foundation-Dienste und WCF Data Services in Visual Studio](../data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio.md) Anwendung). Die Präsentationsschicht greift nicht direkt auf die Datenschicht zu. Sie kommuniziert mit der Datenschicht unter Verwendung der Datenzugriffskomponenten der mittleren Ebene.

## <a name="middle-tier"></a>Mittlere Ebene
Die *mittlere Ebene* ist die Ebene, über die Präsentationsebene und Datenebene miteinander kommunizieren. Zu den typischen Komponenten einer mittleren Ebene gehören:

-   Geschäftslogik, z. B. Geschäftsregeln und Datenvalidierung.

-   Komponenten und Logik für den Datenzugriff, wie beispielsweise:

    -   [TableAdapters](create-and-configure-tableadapters.md) und ["DataAdapters" und "DataReaders"](/dotnet/framework/data/adonet/dataadapters-and-datareaders).

    -   Objektdarstellungen von Daten, z. B. [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index) Entitätsklassen.

    -   Allgemeine Anwendungsdienste wie Authentifizierung, Autorisierung und Personalisierung.

In der folgenden Abbildung werden die in Visual Studio zur Verfügung stehenden Funktionen und Technologien und deren mögliche Verwendung in der mittleren Ebene einer N-Tier-Anwendung dargestellt.

![Mittlere Ebene Komponenten](../data-tools/media/ntiermid.png) mittleren Ebene

Die mittlere Ebene stellt in der Regel mithilfe einer Datenverbindung eine Verbindung mit der Datenschicht her. Diese Datenverbindung wird üblicherweise in der Datenzugriffskomponente gespeichert.

## <a name="data-tier"></a>Datenschicht
Die *Datenebene* ist im Grunde der Server, die Daten einer Anwendung (z. B. ein Server mit SQL Server) gespeichert.

In der folgenden Abbildung werden die in Visual Studio zur Verfügung stehenden Funktionen und Technologien und deren mögliche Verwendung in der Datenebene einer N-Tier-Anwendung dargestellt.

![Komponenten der Datenschicht](../data-tools/media/ntierdatatier.png) Datenebene

Vom Client in der Präsentationsebene kann nicht direkt auf die Datenschicht zugegriffen werden. Stattdessen fungiert die mittlere Ebene als Datenzugriffskomponente und dient zur Kommunikation zwischen der Präsentations- und der Datenschicht.

## <a name="help-for-n-tier-development"></a>Hilfe zur n-schichtigen Entwicklung
In den folgenden Themen finden Sie Informationen über die Arbeit mit N-Tier-Anwendungen:

[Gewusst wie: DataSets und TableAdapters in verschiedene Projekte aufteilen](../data-tools/separate-datasets-and-tableadapters-into-different-projects.md)

[Exemplarische Vorgehensweise: Erstellen einer n-schichtigen Datenanwendung](../data-tools/walkthrough-creating-an-n-tier-data-application.md)

[N-schichtige Anwendungen und Remoteanwendungen mit LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql)

## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: Erstellen einer n-schichtigen Datenanwendung](../data-tools/walkthrough-creating-an-n-tier-data-application.md)
- [Hierarchische Aktualisierung](../data-tools/hierarchical-update.md)
- [Datasettools in Visual Studio](../data-tools/dataset-tools-in-visual-studio.md)
- [Zugreifen auf Daten in Visual Studio](../data-tools/accessing-data-in-visual-studio.md)