---
title: 'Tutorial: Erstellen einer einfachen C#-Konsolen-App'
description: Erfahren Sie anhand einer exemplarischen Vorgehensweise, wie Sie eine C#-Konsolen-App in Visual Studio erstellen.
ms.custom: seodec18, get-started
ms.date: 01/25/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-dev15
ms.topic: tutorial
ms.devlang: CSharp
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 856c20175fd444c7acf83bdf02526c907a28b92f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "54936956"
---
# <a name="tutorial-create-a-simple-c-console-app-in-visual-studio"></a>Tutorial: Erstellen einer einfachen C#-Konsolen-App in Visual Studio

In diesem Tutorial für C# verwenden Sie Visual Studio, um eine Konsolen-App zu erstellen und auszuführen sowie einige Funktionen der integrierten Visual Studio-Entwicklungsumgebung (IDE) zu untersuchen, während Sie diese Aufgaben ausführen.

Wenn Sie Visual Studio noch nicht installiert haben, können Sie es auf der Seite [Visual Studio-Downloads](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) kostenlos herunterladen.

## <a name="create-a-project"></a>Erstellen eines Projekts

Zunächst müssen Sie ein Projekt für die C#-Anwendung erstellen. Der Projekttyp enthält, schon bevor Sie mit der Bearbeitung beginnen, alle Vorlagendateien, die Sie benötigen.

1. Öffnen Sie Visual Studio 2017.

2. Klicken Sie in der Menüleiste im oberen Bereich auf **Datei** > **Neu** > **Projekt**.

3. Erweitern Sie im linken Dialogfeld **Neues Projekt** den Eintrag **C#**, und klicken Sie auf **.NET Core**. Wählen Sie im mittleren Bereich die Option **Konsolenanwendung (.NET Core)** aus. Nennen Sie die Datei *Calculator*.

   ![Projektvorlage „Console App (.NET Core)“ im Dialogfeld „Neues Projekt“ in der Visual Studio-IDE](./media/new-project-csharp-calculator-console-app.png)

### <a name="add-a-workgroup-optional"></a>Hinzufügen einer Workgroup (optional)

Wenn Ihnen die Projektvorlage **Console App (.NET Core)** (Konsolen-App (.NET Core)) fehlt, fügen Sie einfach die Workload **Plattformübergreifende .NET Core-Entwicklung** hinzu. Gehen Sie folgendermaßen vor:

#### <a name="option-1-use-the-new-project-dialog-box"></a>Option 1: Verwenden des Dialogfelds „Neues Projekt“

1. Wählen Sie im Dialogfeld **Neues Projekt** im linken Bereich den Link **Visual Studio-Installer öffnen** aus.

   ![Auswählen des Links „Visual Studio-Installer öffnen“ im Dialogfeld „Neues Projekt“](./media/csharp-open-visual-studio-installer-generic-dark.png)

1. Der Visual Studio-Installer wird gestartet. Wählen Sie die Workload **Plattformübergreifende .NET Core-Entwicklung** aus, und klicken Sie dann auf **Anpassen**.

   ![Workload für die plattformübergreifende .NET Core-Entwicklung im Visual Studio-Installer](./media/dot-net-core-xplat-dev-workload.png)

#### <a name="option-2-use-the-tools-menu-bar"></a>Option 2: Verwenden der Menüleiste „Extras“

1. Schließen Sie das Dialogfeld **Neues Projekt**, und klicken Sie in der Menüleiste oben auf **Extras** > **Tools und Features abrufen…**.

1. Der Visual Studio-Installer wird gestartet. Wählen Sie die Workload **Plattformübergreifende .NET Core-Entwicklung** aus, und klicken Sie dann auf **Anpassen**.

## <a name="create-the-app"></a>Erstellen der App

Zunächst befassen Sie sich mit grundlegenden Berechnungen von Integern in C#. Daraufhin fügen Sie Code hinzu, um einen einfachen Rechner zu erstellen. Dann wird erläutert, wie der Code optimiert werden muss, um Funktionen hinzuzufügen. Anschließend erhalten Sie Informationen zum Debuggen Ihrer App, damit Sie Fehler finden und beheben können. Zuletzt erfahren Sie, wie Sie den Code effizienter machen können.

Beginnen Sie mit der Berechnung von Integern in C#.

1. Löschen Sie im Code-Editor den „Hallo Welt“-Standardcode.

    ![Löschen des „Hallo Welt“-Standardcodes aus der neuen Rechner-App](./media/csharp-console-calculator-deletehelloworld.png)

   Löschen Sie die Zeile, die `Console.WriteLine("Hello World!");` beinhaltet.

1. Geben Sie stattdessen folgenden Code in diese Zeile ein:

    ```csharp
            int a = 42;
            int b = 119;
            int c = a + b;
            Console.WriteLine(c);
            Console.ReadKey();
    ```
1. Wählen Sie **Calculator** aus, um das Programm auszuführen, oder drücken Sie **F5**.

   ![Auswählen der Schaltfläche „Calculator“ zum Ausführen der App aus der Symbolleiste](./media/csharp-console-calculator-button.png)

   Ein neues Konsolenfenster wird geöffnet, das die Summe von 42 + 119 zeigt.

1. Versuchen Sie jetzt, die Codezeile `int c = a + b;` zu ändern, indem Sie einen anderen Operator verwenden, z. B. `-` für die Subtraktion, `*` für die Multiplikation oder */* für die Division.

    Beachten Sie, dass das Ergebnis sich ebenfalls ändert, wenn Sie den Operator ändern und das Programm ausführen.

Als Nächstes fügen Sie Ihrem Projekt komplexeren Rechnercode hinzu.

1. Löschen Sie den gesamten Code im Code-Editor.

1. Geben oder fügen Sie den folgenden neuen Code in den Code-Editor ein:

    ```csharp
    using System;

    namespace Calculator
    {
        class Program
        {
            static void Main(string[] args)
            {
                // Declare variables and then initialize to zero
                int num1 = 0; int num2 = 0;

                // Display title as the C# console calculator app
                Console.WriteLine("Console Calculator in C#\r");
                Console.WriteLine("------------------------\n");

                // Ask the user to type the first number
                Console.WriteLine("Type a number, and then press Enter");
                num1 = Convert.ToInt32(Console.ReadLine());

                // Ask the user to type the second number
                Console.WriteLine("Type another number, and then press Enter");
                num2 = Convert.ToInt32(Console.ReadLine());

                // Ask the user to choose an option
                Console.WriteLine("Choose an option from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                // Use a switch statement to do the math
                switch (Console.ReadLine())
                {
                    case "a":
                        Console.WriteLine($"Your result: {num1} + {num2} = " + (num1 + num2));
                        break;
                    case "s":
                        Console.WriteLine($"Your result: {num1} - {num2} = " + (num1 - num2));
                        break;
                    case "m":
                        Console.WriteLine($"Your result: {num1} * {num2} = " + (num1 * num2));
                        break;
                    case "d":
                        Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                        break;
                }
                // Wait for the user to respond before closing
                Console.Write("Press any key to close the Calculator console app...");
                Console.ReadKey();
            }
        }
    }
    ```
1. Wählen Sie **Calculator** aus, um das Programm auszuführen, oder drücken Sie **F5**.

   ![Auswählen der Schaltfläche „Calculator“ zum Ausführen der App aus der Symbolleiste](./media/csharp-console-calculator-button.png)

   Dann wird ein Konsolenfenster geöffnet.

1. Rufen Sie Ihre App in dem Konsolenfenster auf, und befolgen Sie dann die Anweisungen, um die Zahlen **42** und **119** hinzuzufügen.

   Die App sollte in etwa wie auf dem folgenden Screenshot dargestellt aussehen:

    ![Konsolenfenster mit der Rechner-App und Anweisungen zu den auszuführenden Aktionen](./media/csharp-console-calculator.png)

### <a name="add-decimals"></a>Hinzufügen von Dezimalzahlen

Die Rechner-App akzeptiert derzeit nur ganze Zahlen und gibt auch keine Dezimalzahlen zurück. Dies können Sie ändern, indem Sie Code hinzufügen, der die Angabe von Dezimalzahlen zulässt.

Wie Sie auf dem folgenden Screenshot sehen, erhalten Sie die Zahl 0 (null) als Ergebnis, wenn Sie 42 durch 119 dividieren. Dieses Ergebnis ist allerdings zu ungenau.

![Konsolenfenster mit der Rechner-App, die keine Dezimalzahlen als Ergebnis zurückgibt](./media/csharp-console-calculator-nodecimal.png)

Gehen Sie daher wie folgt vor, um den Code für die Verarbeitung von Dezimalzahlen anzupassen.

1. Drücken Sie **STRG** + **F**, um das Steuerelement **Suchen und Ersetzen** zu öffnen.

1. Ändern Sie sämtliche Instanzen der `int`-Variablen in `float`.

    ![Animation des Steuerelements „Suchen und Ersetzen“, die zeigt, wie die Variable „int“ in „float“ geändert wird.](./media/find-replace-control-animation.gif)

1. Führen Sie Ihre Rechner-App erneut aus, und dividieren Sie **42** durch **119**.

   Jetzt sollte die App anstelle der Zahl 0 eine Dezimalzahl zurückgeben.

    ![Konsolenfenster mit der Rechner-App, die jetzt Dezimalzahlen als Ergebnis zurückgibt](./media/csharp-console-calculator-decimal.png)

Die App gibt allerdings nur Dezimalzahlen als Ergebnis zurück. Gehen Sie daher wie folgt vor, damit die App auch mit Dezimalzahlen rechnen kann.

1. Verwenden Sie das Steuerelement **Suchen und Ersetzen** (**STRG** + **F**), um jede Instanz der Variablen `float` in `double` und jede Instanz der Methode `Convert.ToInt32` in `Convert.ToDouble` zu ändern.

1. Führen Sie Ihre Rechner-App aus, und dividieren Sie **42,5** durch **119,75**.

   Nun sollte die App auch Dezimalwerte akzeptieren und mehr Dezimalstellen als Ergebnis zurückgeben.

    ![Konsolenfenster mit der Rechner-App, die jetzt Dezimalzahlen akzeptiert und mehr Dezimalstellen als Ergebnis zurückgibt](./media/csharp-console-calculator-usedecimals.png)

    (Im Abschnitt [Überarbeiten des Codes](#revise-the-code) erfahren Sie, wie Sie das Problem mit der Anzahl der Dezimalstellen beheben.)

## <a name="debug-the-app"></a>Debuggen der App

Sie haben nun bereits Ihre einfache App verbessert, allerdings fehlen noch Optionen zur Ausfallsicherheit, um Ausnahmen wie durch den Benutzer verursachte Eingabefehler zu verarbeiten.

Wenn Sie beispielsweise versuchen, eine Zahl durch 0 zu dividieren oder einen Buchstaben eingeben, obwohl die App eine Zahl erwartet (oder umgekehrt), funktioniert die App nicht mehr und gibt einen Fehler zurück.

Nachfolgend werden einige häufige durch den Benutzer verursachte Eingabefehler erläutert, und Sie erfahren, wie Sie diese im Debugger finden und im Code beheben.

>[!TIP]
>Weitere Informationen zum Debugger und dessen Funktionsweise finden Sie auf der Seite [Ein erster Blick auf den Visual Studio-Debugger](../../debugger/debugger-feature-tour.md).

### <a name="fix-the-divide-by-zero-error"></a>Beheben des Fehlers „Division durch Null“

Wenn Sie versuchen, eine Zahl durch 0 zu dividieren, friert die Konsolen-App ein. Dann zeigt Ihnen Visual Studio an, welcher Fehler im Code-Editor aufgetreten ist.

   ![Der Visual Studio-Code-Editor zeigt den Fehler „Division durch Null“ an](./media/csharp-console-calculator-dividebyzero-error.png)

Sie müssen den Code wie folgt bearbeiten, damit dieser Fehler verarbeitet werden kann.

1. Löschen Sie den Code, der zwischen `case "d":` und dem Kommentar `// Wait for the user to respond before closing` (Vor dem Schließen auf eine Reaktion des Benutzers warten) angezeigt wird.

1. Ersetzen Sie den Code durch folgenden Code:

   ```csharp
            // Ask the user to enter a non-zero divisor until they do so
                while (num2 == 0)
                {
                    Console.WriteLine("Enter a non-zero divisor: ");
                    num2 = Convert.ToInt32(Console.ReadLine());
                }
                Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                break;
        }
    ```

   Wenn Sie den Code hinzugefügt haben, sollte der Bereich mit der `switch`-Anweisung in etwa wie auf dem folgenden Screenshot aussehen:

   ![Der überarbeitete „switch“-Bereich im Visual Studio-Code-Editor](./media/csharp-console-calculator-switch-code.png)

Die App sollte Sie nun zur Eingabe einer anderen Zahl auffordern, wenn Sie versuchen, durch 0 zu dividieren. Diese Aufforderung wird so lange angezeigt, bis Sie eine andere Zahl als 0 eingeben.

   ![Der Visual Studio-Code-Editor zeigt den Fehler „Division durch Null“ an](./media/csharp-console-calculator-dividebyzero.png)

### <a name="fix-the-format-error"></a>Beheben des Fehlers „Format“

Wenn Sie einen Buchstaben eingeben, obwohl die App die Eingabe einer Zahl erwartet (oder umgekehrt), friert die Konsolen-App ein. Dann zeigt Ihnen Visual Studio an, welcher Fehler im Code-Editor aufgetreten ist.

   ![Der Visual Studio-Code-Editor zeigt einen Formatfehler an](./media/csharp-console-calculator-format-error.png)

Damit dieser Fehler behoben werden kann, muss der zuvor eingegebene Code umgestaltet werden.

#### <a name="revise-the-code"></a>Überarbeiten des Codes

Damit Sie nicht davon abhängig sind, dass die `program`-Klasse den gesamten Code verarbeitet, sollten Sie Ihre App in zwei Klassen (`calculator` und `program`) aufteilen.

Die `calculator`-Klasse soll einen Großteil der Rechenarbeit übernehmen, während die `program`-Klasse die Benutzeroberfläche und das Erfassen von Fehlern handhabt.

Fangen wir also an.

1. Löschen Sie sämtliche Eingaben *nach* dem folgenden Codeblock:

    ```csharp

    using System;

    namespace Calculator
    {

    ```

1. Gehen Sie dann wie folgt vor, um eine neue `calculator`-Klasse hinzuzufügen:

    ```csharp
    class Calculator
    {
        public static double DoOperation(double num1, double num2, string op)
        {
            double result = double.NaN; // Default value is "not-a-number" which we use if an operation, such as division, could result in an error

            // Use a switch statement to do the math
            switch (op)
            {
                case "a":
                    result = num1 + num2;
                    break;
                case "s":
                    result = num1 - num2;
                    break;
                case "m":
                    result = num1 * num2;
                    break;
                case "d":
                    // Ask the user to enter a non-zero divisor
                    if (num2 != 0)
                    {
                        result = num1 / num2;
                    }
                    break;
                // Return text for an incorrect option entry
                default:
                    break;
            }
            return result;
        }
    }

    ```

1. Gehen Sie anschließend wie folgt vor, um eine neue `program`-Klasse hinzuzufügen:

    ```csharp
    class Program
    {
        static void Main(string[] args)
        {
            bool endApp = false;
            // Display title as the C# console calculator app
            Console.WriteLine("Console Calculator in C#\r");
            Console.WriteLine("------------------------\n");

            while (!endApp)
            {
                // Declare variables and set to empty
                string numInput1 = "";
                string numInput2 = "";
                double result = 0;

                // Ask the user to type the first number
                Console.Write("Type a number, and then press Enter: ");
                numInput1 = Console.ReadLine();

                double cleanNum1 = 0;
                while (!double.TryParse(numInput1, out cleanNum1))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput1 = Console.ReadLine();
                }

                // Ask the user to type the second number
                Console.Write("Type another number, and then press Enter: ");
                numInput2 = Console.ReadLine();

                double cleanNum2 = 0;
                while (!double.TryParse(numInput2, out cleanNum2))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput2 = Console.ReadLine();
                }

                // Ask the user to choose an operator
                Console.WriteLine("Choose an operator from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                string op = Console.ReadLine();

                try
                {
                    result = Calculator.DoOperation(cleanNum1, cleanNum2, op);
                    if (double.IsNaN(result))
                    {
                        Console.WriteLine("This operation will result in a mathematical error.\n");
                    }
                    else Console.WriteLine("Your result: {0:0.##}\n", result);
                }
                catch (Exception e)
                {
                    Console.WriteLine("Oh no! An exception occurred trying to do the math.\n - Details: " + e.Message);
                }

                Console.WriteLine("------------------------\n");

                // Wait for the user to respond before closing
                Console.Write("Press 'n' and Enter to close the app, or press any other key and Enter to continue: ");
                if (Console.ReadLine() == "n") endApp = true;

                Console.WriteLine("\n"); // Friendly linespacing
            }
            return;
        }
    }
    ```
1. Wählen Sie **Calculator** aus, um das Programm auszuführen, oder drücken Sie **F5**.

1. Befolgen Sie die Anweisungen, und dividieren Sie die Zahl **42** durch **119**. Ihre App sollte dann in etwa wie folgt aussehen:

    ![Konsolenfenster mit der umgestalteten Rechner-App und Anweisungen zu den auszuführenden Aktionen und zur Fehlerbehandlung bei falschen Eingaben](./media/csharp-console-calculator-refactored.png)

    Sie können so lange weitere Gleichungen hinzufügen, bis Sie die Konsolen-App schließen. Außerdem haben Sie die Anzahl der Dezimalstellen im Ergebnis reduziert.

## <a name="close-the-app"></a>Schließen der App

1. Schließen Sie die App, falls noch nicht geschehen.

1. Schließen Sie den Bereich **Output** (Ausgabe) in Visual Studio.

   ![Schließen des Ausgabebereichs in Visual Studio](./media/csharp-calculator-close-output-pane.png)

1. Drücken Sie in Visual Studio **STRG**+**S**, um die App zu speichern.

1. Schließen Sie Visual Studio.

## <a name="code-complete"></a>Vollständiger Code

Im Rahmen dieses Tutorials haben Sie einige Änderungen an der Rechner-App vorgenommen. Die App kann jetzt Rechenressourcen effizienter handhaben und die meisten durch den Benutzer verursachten Eingabefehler verarbeiten.

Nachfolgend finden Sie den vollständigen Code:

```csharp

using System;

namespace Calculator
{
    class Calculator
    {
        public static double DoOperation(double num1, double num2, string op)
        {
            double result = double.NaN; // Default value is "not-a-number" which we use if an operation, such as division, could result in an error

            // Use a switch statement to do the math
            switch (op)
            {
                case "a":
                    result = num1 + num2;
                    break;
                case "s":
                    result = num1 - num2;
                    break;
                case "m":
                    result = num1 * num2;
                    break;
                case "d":
                    // Ask the user to enter a non-zero divisor
                    if (num2 != 0)
                    {
                        result = num1 / num2;
                    }
                    break;
                // Return text for an incorrect option entry
                default:
                    break;
            }
            return result;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            bool endApp = false;
            // Display title as the C# console calculator app
            Console.WriteLine("Console Calculator in C#\r");
            Console.WriteLine("------------------------\n");

            while (!endApp)
            {
                // Declare variables and set to empty
                string numInput1 = "";
                string numInput2 = "";
                double result = 0;

                // Ask the user to type the first number
                Console.Write("Type a number, and then press Enter: ");
                numInput1 = Console.ReadLine();

                double cleanNum1 = 0;
                while (!double.TryParse(numInput1, out cleanNum1))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput1 = Console.ReadLine();
                }

                // Ask the user to type the second number
                Console.Write("Type another number, and then press Enter: ");
                numInput2 = Console.ReadLine();

                double cleanNum2 = 0;
                while (!double.TryParse(numInput2, out cleanNum2))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput2 = Console.ReadLine();
                }

                // Ask the user to choose an operator
                Console.WriteLine("Choose an operator from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                string op = Console.ReadLine();

                try
                {
                    result = Calculator.DoOperation(cleanNum1, cleanNum2, op);
                    if (double.IsNaN(result))
                    {
                        Console.WriteLine("This operation will result in a mathematical error.\n");
                    }
                    else Console.WriteLine("Your result: {0:0.##}\n", result);
                }
                catch (Exception e)
                {
                    Console.WriteLine("Oh no! An exception occurred trying to do the math.\n - Details: " + e.Message);
                }

                Console.WriteLine("------------------------\n");

                // Wait for the user to respond before closing
                Console.Write("Press 'n' and Enter to close the app, or press any other key and Enter to continue: ");
                if (Console.ReadLine() == "n") endApp = true;

                Console.WriteLine("\n"); // Friendly linespacing
            }
            return;
        }
    }
}

```

## <a name="next-steps"></a>Nächste Schritte

Damit haben Sie das Tutorial erfolgreich abgeschlossen. Wenn Sie weitere Informationen erhalten möchten, fahren Sie mit den folgenden Tutorials fort.

> [!div class="nextstepaction"]
> [C#-Tutorials](/dotnet/csharp/tutorials/)

## <a name="see-also"></a>Siehe auch

* [Video course: C# Fundamentals for Absolute Beginners (Videokurs: C#-Grundlagen für Einsteiger)](https://mva.microsoft.com/en-us/training-courses/c-fundamentals-for-absolute-beginners-16169)
* [Tutorial: Debuggen von C#-Code mit Visual Studio](tutorial-debugger.md)