using System;

class Program
{
    static int LinearSearch(string[] array, string target)
    {
        for (int i = 0; i < array.Length; i++)
        {
            if (array[i].ToLower() == target.ToLower()) // Case-insensitive comparison
            {
                return i; // Returns the index of the target fruit
            }
        }
        return -1; // Returns -1 if the fruit is not found
    }

    static void Main()
    {
        string[] fruits = { "strawberry", "raspberry", "blueberry", "gooseberry", "cherry" };

        Console.Write("enter the fruit you want to search for: ");
        string target = Console.ReadLine();

        int result = LinearSearch(fruits, target);

        if (result != -1)
        {
            Console.WriteLine($"the fruit you chose was found at index {result}");
        }
        else
        {
            Console.WriteLine("the fruit you chose was not found");
        }
    }
}
