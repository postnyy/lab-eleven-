using System;

namespace ConsoleApplication1
{
    internal class Program
    {
        public static void Main(string[] args)
        {
            System.Console.OutputEncoding = System.Text.Encoding.UTF8;
            Console.WriteLine("Введіть список прізвищ розділених комами.");
            string txt = Console.ReadLine();

            string[] surnames = txt.Split(',');
            Array.Sort(surnames);
            
            Console.WriteLine("Сортований список прізвищ: ");
            foreach (var surname in surnames)
            {
                Console.WriteLine(surname.Trim());
            }
        }
    }
}
