---
title: Die Eigenschaft &lt;Eigenschaftennamen&gt; kann nicht gelöscht werden, da sie in der Zuordnung teilnimmt &lt;Zuordnungsname&gt; | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 389873cc-92dd-48da-bfca-0f6c8e0ae3c2
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: cdd2c2ab26709a017801e8ae34e4ee6f2223c2c3
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "49177735"
---
# <a name="the-property-ltproperty-namegt-cannot-be-deleted-because-it-is-participating-in-the-association-ltassociation-namegt"></a>Die Eigenschaft &lt;Eigenschaftennamen&gt; kann nicht gelöscht werden, da sie in der Zuordnung teilnimmt &lt;Zuordnungsname&gt;
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Die ausgewählte Eigenschaft wird festgelegt, als die **Zuordnungseigenschaft** für die Zuordnung zwischen den Klassen, die in der Fehlermeldung angegeben. Eigenschaften können nicht gelöscht werden, wenn sie an einer Zuordnung zwischen Datenklassen beteiligt sind.  
  
 Legen Sie die **Zuordnungseigenschaft** auf eine andere Eigenschaft der Datenklasse fest, damit die gewünschte Eigenschaft gelöscht werden kann.  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
1.  Wählen Sie im O/R-Designer die Zuordnungslinie aus, die die in der Fehlermeldung angegebenen Datenklassen verbindet.  
  
2.  Doppelklicken Sie auf die Zeile zum Öffnen der **Zuordnungs-Editor** Dialogfeld.  
  
3.  Entfernen Sie die Eigenschaft aus der **Zuordnungseigenschaften**.  
  
4.  Versuchen Sie erneut, die Eigenschaft zu löschen.  
  
## <a name="see-also"></a>Siehe auch  
 [LINQ to SQL-Tools in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [Gewusst wie: Erstellen einer Zuordnung (Beziehung) zwischen LINQ to SQL-Klassen (O/R Designer)](../data-tools/how-to-create-an-association-relationship-between-linq-to-sql-classes-o-r-designer.md)   
 [Exemplarische Vorgehensweise: Erstellen von LINQ to SQL-Klassen (O / R-Designer)](http://msdn.microsoft.com/library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)

