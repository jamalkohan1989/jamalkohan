using System;

namespace ReverseDecimalNumber
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a decimal number: ");
            double num = double.Parse(Console.ReadLine());

            // Convert the decimal number to a string
            string numString = num.ToString();

            // Split the string at the decimal point
            string[] parts = numString.Split('.');

            // Reverse the string before the decimal point
            char[] beforeDecimal = parts[0].ToCharArray();
            Array.Reverse(beforeDecimal);
            string beforeDecimalString = new string(beforeDecimal);

            // Reverse the string after the decimal point
            char[] afterDecimal = parts[1].ToCharArray();
            Array.Reverse(afterDecimal);
            string afterDecimalString = new string(afterDecimal);

            // Combine the two reversed strings with a decimal point in between
            string result = beforeDecimalString + "." + afterDecimalString;

            Console.WriteLine("The reverse of the decimal number is: " + result);
        }
    }
}
