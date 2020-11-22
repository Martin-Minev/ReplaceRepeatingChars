//# ReplaceRepeatingChars
using System;
using System.Text;

namespace ReplaceRepeatingChars
{
    class Program
    {
        static void Main(string[] args)
        {
            string input = Console.ReadLine();
            int startIndex = 0;
            var sb = new StringBuilder();

            for (int i = 0; i < input.Length; i++)
            {
                if (startIndex == input.Length - 1)
                {
                    sb.Append(input[input.Length - 1]);
                    Console.WriteLine(sb.ToString());
                    return;
                }

                if (input[startIndex] != input[startIndex + 1])
                {
                    sb.Append(input[startIndex]);
                    startIndex++;
                }
                else
                {
                    startIndex++;
                }
            }
            
        }
    }
}
