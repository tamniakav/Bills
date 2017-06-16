using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam4
{
    class Exam4
    {
        static void Main(string[] args)
        {
            int months = int.Parse(Console.ReadLine());

            double electro = 0;
            double water = months * 20;
            double internet = months * 15;
            double other = 0;

            for (int i = 0; i < months; i++)
            {
                double electricity = double.Parse(Console.ReadLine());

                electro = electro + electricity;
                double think = electricity + 20 + 15;
                double percentage = (think * 20) / 100;
                other = other + (think + percentage);
            }

            double average = (electro + water + internet + other) / months;

            Console.WriteLine("Electricity: {0:f2} lv", electro);
            Console.WriteLine("Water: {0:f2} lv", water);
            Console.WriteLine("Internet: {0:f2} lv", internet);
            Console.WriteLine("Other: {0:f2} lv", other);
            Console.WriteLine("Average: {0:f2} lv", average);
        }
    }
}
