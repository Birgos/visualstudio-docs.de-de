---
title: 'Schritt 4: Hinzufügen der CheckTheAnswer()-Methode | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: c66f3831-b4a0-40bc-a109-8f46f4db35ed
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8ce0a3f35001c468f887c1a595cd37231b38cb72
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54802502"
---
# <a name="step-4-add-the-checktheanswer-method"></a>Schritt 4: Hinzufügen der CheckTheAnswer()-Methode
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Im vierten Teil dieses Lernprogramms schreiben Sie eine Methode, `CheckTheAnswer()`, die bestimmt, ob die Antworten auf die Mathematikaufgaben korrekt sind. Dieses Thema ist Teil einer Reihe von Lernprogrammen zu grundlegenden Konzepte der Codierung. Eine Übersicht über das Tutorial finden Sie unter [Tutorial 2: Erstellen eines Mathequiz mit Zeitmessung](../ide/tutorial-2-create-a-timed-math-quiz.md).  
  
> [!NOTE]
>  Wenn Sie weiterhin in Visual Basic arbeiten, verwenden Sie das Schlüsselwort `Function` anstelle des üblichen Schlüsselworts `Sub`, da diese Methode einen Wert zurückgibt. Es ist wirklich ganz einfach: Ein Sub-Schlüsselwort gibt keinen Wert zurück, aber ein Function-Schlüsselwort gibt einen Wert zurück.  
  
### <a name="to-verify-whether-the-answers-are-correct"></a>So überprüfen Sie, ob die Antworten richtig sind  
  
1.  Fügen Sie die `CheckTheAnswer()`-Methode hinzu.  
  
     Wenn diese Methode aufgerufen wird, werden die Werte von „addend1“ und „addend2“ hinzugefügt und das Ergebnis mit dem Wert im `NumericUpDown`-Summensteuerelement verglichen. Wenn die Werte gleich sind, gibt die Methode den Wert `true` zurück. Anderenfalls gibt die Methode den Wert `false` zurück. Der Code sollte wie folgt aussehen.  
  
     [!code-csharp[VbExpressTutorial3Step4#8](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step4/cs/form1.cs#8)]
     [!code-vb[VbExpressTutorial3Step4#8](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step4/vb/form1.vb#8)]  
  
     Nun überprüfen Sie die Antwort, indem Sie die Code in der Methode aktualisieren, damit der Tick-Ereignishandler des Zeitgebers die neue `CheckTheAnswer()`-Methode aufruft.  
  
2.  Fügen Sie der `if else`-Anweisung folgenden Code hinzu.  
  
     [!code-csharp[VbExpressTutorial3Step4#10](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step4/cs/form1.cs#10)]
     [!code-vb[VbExpressTutorial3Step4#10](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step4/vb/form1.vb#10)]  
  
     Wenn die Antwort richtig ist, gibt `CheckTheAnswer()` `true` zurück. Der Ereignishandler beendet den Timer, zeigt eine Glückwunschmeldung an, und macht anschließend die Schaltfläche **Start** erneut verfügbar. Anderenfalls wird das Quiz fortgesetzt.  
  
3.  Speichern Sie das Programm, führen Sie es aus, starten Sie ein Quiz, und geben Sie eine richtige Antwort für die Additionsaufgabe an.  
  
    > [!NOTE]
    >  Bevor Sie die Antwort eingeben, müssen Sie entweder den Standardwert auswählen, oder Sie müssen die Null manuell löschen. Später in diesem Lernprogramm wird dieses Verhalten korrigiert.  
  
     Wenn Sie eine richtige Antwort angeben, wird ein Meldungsfeld geöffnet, die Schaltfläche **Start** wird verfügbar, und der Timer wird angehalten.  
  
### <a name="to-continue-or-review"></a>So fahren Sie fort oder überprüfen die Angaben  
  
-   Den nächsten Schritt des Tutorials finden Sie unter [Schritt 5: Hinzufügen von Enter-Ereignishandlern für die NumericUpDown-Steuerelemente](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)  
  
-   Den vorherigen Schritt des Tutorials finden Sie unter [Schritt 3: Hinzufügen eines Countdowntimers](../ide/step-3-add-a-countdown-timer.md)
