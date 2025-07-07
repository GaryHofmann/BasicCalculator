//BasicCalculator
using System;

public class Program
{
    public static void Main()
    {
        int userInput1 = 0;
        int userInput2 = 0;
        int userInput3;
        string operation; 
        string operationChoice;
        bool continueCalc = true;
        bool userValidateInput;
        bool userValidateInput2;
        bool userValidateInput3;

        while (continueCalc)// while loop #1 (Exception handling for user selection)
        {
            userValidateInput = false;
            while (!userValidateInput)// while loop #2 (Exception handling for user selection)
            {
                Console.WriteLine("\nPlease enter two numbers:");
                Console.Write("\nFirst number:");
                string input1 = Console.ReadLine();

                Console.Write("\nSecond number:");
                string input2 = Console.ReadLine();

                if (int.TryParse(input1, out userInput1) && int.TryParse(input2, out userInput2))
                {
                    userValidateInput = true;
                }
                else
                {
                    Console.WriteLine("\nThis input is invalid. Please enter numbers only...\n");
                }
            }
            userValidateInput2 = false;
            while (!userValidateInput2)// while loop #3 (Exception handling for user selection)
            {
                Console.WriteLine("\nPlease choose the operation you'd like to preform:");
                Console.WriteLine("[+] - Addition");
                Console.WriteLine("[-] - Subtraction");
                Console.WriteLine("[x] - Multiplication");
                Console.WriteLine("[/] - Division");

                Console.Write("\nEnter operation:");
                operation = Console.ReadLine();

                if (operation != "+" && operation != "-" && operation != "x" && operation != "/")
                {
                    Console.WriteLine($"\nInvalid selection, please try again");
                }
                else
                {
                    userValidateInput2 = true;
                    switch (operation)// switch block #1 (to allow user to select the operation they'd like to use)
                    {
                        case "+":
                            Console.WriteLine($"\nAnswer: {userInput1} + {userInput2} = {userInput1 + userInput2}");
                            break;
                        case "-":
                            Console.WriteLine($"\nAnswer: {userInput1} - {userInput2} = {userInput1 - userInput2}");
                            break;
                        case "x":
                            Console.WriteLine($"\nAnswer: {userInput1} * {userInput2} = {userInput1 * userInput2}");
                            break;
                        case "/":
                            if (userInput2 != 0)
                                Console.WriteLine($"\nAnswer: {userInput1} / {userInput2} = {(double)userInput1 / userInput2}\n");
                            else
                                Console.WriteLine($"\nAnswer: Invalid input! You cannot divide {userInput1} by {userInput2}.\n");
                            break;
                    }
                }
            }
            userValidateInput3 = false;
            while (!userValidateInput3)// while loop #4 (Exception handling for user selection)
            {
                Console.WriteLine("\n[1] - Do another calculation");
                Console.WriteLine("[2] - Exit application");
                Console.Write("\n\nEnter selection: ");
                string input3 = Console.ReadLine();

                if (int.TryParse(input3, out userInput3))
                {
                    if (userInput3 == 1)
                    {
                        userValidateInput3 = true;
                        continue;
                    }
                    else if (userInput3 == 2)
                    {
                        Console.WriteLine("\nExiting application...\n");
                        return;
                    }
                    else
                    {
                        Console.WriteLine("\nThis input is invalid. Please enter either a [1] or a [2] to select either option from the list...\n");
                    }
                }
                else
                {
                    Console.WriteLine("\nThis input is invalid. Please enter either a [1] or a [2] to select either option from the list...\n");
                }
            }
        }
    }
}
