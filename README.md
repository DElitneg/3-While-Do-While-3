# 3-While-Do-While-3
 While / Do-While #3

1)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            String opcion;
            int precio, descuento, total;
            descuento = 0; total = 0;
            do
            {
                Console.WriteLine("*Se detiene al precionar 0*");
                Console.WriteLine("Cual es el precio del producto?: ");
                precio = Convert.ToInt32(Console.ReadLine());
                total = total + precio;              
                opcion = Convert.ToString(precio);
            } while (opcion != "0");

            if (total > 15000)
            {
                descuento = total - ((total / 100) * 10);
            }
            Console.WriteLine("El precio es "+total+" con el descuento del 10%("+total/100*10+") seria "+descuento);

        }
    }
}

2)
