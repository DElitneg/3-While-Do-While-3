# 3-While-Do-While-3
 While / Do-While #3

1) "6"
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

2) "7"
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

            Double presentes, ausentes, total, porcentaje;
            ausentes = 0; presentes = 0; 
            String opcion, desicion;
            Console.WriteLine("Ingrese el presente del alumno (A.Ausente, P.Presente");
            do
            {
                Console.Write("Respuesta: ");
                opcion = Convert.ToString(Console.ReadLine());
                if (opcion == "A" || opcion == "a")
                {
                    ausentes += 1;
                }
                else if (opcion == "P" || opcion == "p")
                {
                    presentes += 1;
                }
                Console.Write("Desea cargar otro?: (SI/NO)");
                desicion = Convert.ToString(Console.ReadLine());
                if(desicion == "NO" || desicion == "no" || desicion == "No")
                {
                    break;
                }
            } while (true);
            total = presentes + ausentes;
            porcentaje = presentes / total*100;
            Console.WriteLine("Presentes: " + presentes + ", Ausentes: " + ausentes+", el porcentaje de presentismo fue del "+porcentaje+"% sobre "+total);
        }
    }
}

// 3) "8"
