# tohmeegGuessGame
a code to a number guessing game
using System.Globalization;
using System;

namespace GuessGame
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Welcome to TEE'S number guess game, please select a level!");
            Console.WriteLine("The levels are: Easy(E), Medium(M) and Hard(H) ");

            var input = Console.ReadLine().ToUpper();
            char input2;
            if (char.TryParse(input, out input2))
            {
                if (input == "E")
                {
                    Console.WriteLine("You picked easy! you have six guesses");
                    Console.WriteLine("Please pick a number between 1 - 10");
                    
                    var random = new Random();
                    var numberRange = random.Next(1, 10);
                    var numberofguessesleft = 6;
                    var Guess = 0;

                    while (Guess != numberRange)
                    {
                        numberofguessesleft--;
                        var input3 = Console.ReadLine();
                        Guess = int.Parse(input3);
                        if (Guess != numberRange)
                        {
                            Console.WriteLine("Sorry, that was wrong");
                            Console.WriteLine($"You have {numberofguessesleft} guess left ");
                        }
                        if (numberofguessesleft == 0)
                        {
                            Console.WriteLine("GAME OVER!");
                            break;
                        }
                    }
                    if (Guess == numberRange)
                    {
                        Console.WriteLine("Congratulations! you got it right");
                    }
                }

                else if (input == "M")
                {
                    Console.WriteLine("You picked medium! you have four guesses");
                    Console.WriteLine("Please pick a number between 1 - 20");
                    
                    var random = new Random();
                    var numberRange = random.Next(1, 20);
                    var numberofguessesleft = 4;
                    var Guess = 0;

                    while (Guess != numberRange)
                    {
                        numberofguessesleft--;
                        var input3 = Console.ReadLine();
                        Guess = int.Parse(input3);
                        if (Guess != numberRange)
                        {
                            Console.WriteLine("Sorry, that was wrong");
                            Console.WriteLine($"You have {numberofguessesleft} guess left ");
                        }
                        if (numberofguessesleft == 0)
                        {
                            Console.WriteLine("GAME OVER!");
                            break;
                        }
                    }
                    if (Guess == numberRange)
                    {
                        Console.WriteLine("Congratulations! you got it right");
                    }
                }

                else if (input == "H")
                {
                    Console.WriteLine("You picked hard! you have three guesses");
                    Console.WriteLine("Please pick a number between 1 - 50");
                    
                    var random = new Random();
                    var numberRange = random.Next(1, 50);
                    var numberofguessesleft = 3;
                    var Guess = 0;

                    while (Guess != numberRange)
                    {
                        numberofguessesleft--;
                        var input3 = Console.ReadLine();
                        Guess = int.Parse(input3);
                        if (Guess != numberRange)
                        {
                            Console.WriteLine("Sorry, that was wrong");
                            Console.WriteLine($"You have {numberofguessesleft} guess left ");
                        }
                        if (numberofguessesleft == 0)
                        {
                            Console.WriteLine("GAME OVER!");
                            break;
                        }
                    }
                    if (Guess == numberRange)
                    {
                        Console.WriteLine("Congratulations! you got it right");
                    }
                }

            }


        }
    }
}
