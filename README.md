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

            Double mayores, menores, total, promedio, opcion;
            mayores = 0; menores = 0; 
          
           
            do
            {
                Console.WriteLine("Ingrese la edad de la persona");
                Console.Write("Respuesta: ");
                opcion = Convert.ToInt32(Console.ReadLine());
                if (opcion >= 18)
                {
                    mayores += 1;
                }
                else if (opcion < 18)
                {
                    menores += 1;
                }
                if(opcion < 0)
                {
                    break;
                }
            } while (true);
            promedio = (menores + mayores) / 100;
            Console.WriteLine("Mayores: "+mayores+", Menores: "+menores+", Promedio: "+promedio);
        }
    }
}
RESVISAR EL 3


// 4) "9"
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

            Double opcion, menor;
            menor = 99999;


            do
            {
                Console.WriteLine("Ingrese numeros enteros positivos, el programa se cierra al ingresar un negativo");
                Console.Write("Respuesta: ");
                opcion = Convert.ToInt32(Console.ReadLine());


                if (opcion < menor && opcion > 0)
                {
                    menor = opcion;
                }
            } while (opcion > 0);

            Console.WriteLine("El menor numero fue:"+menor);

        }
    }
}

// 5) "10"

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

            Double creditos, menor, apuesta,dadoUno,dadoDos;
            creditos = 100;


            do
            {
                Console.WriteLine("LET'S GO GAMBLING!: ");
                Console.Write("Apuesta: ");
                apuesta = Convert.ToInt32(Console.ReadLine());

                if (apuesta != 0)
                {
                    Console.WriteLine("Los dados tienen 6 puntos:");
                    Console.Write("Primer dado:");
                    dadoUno = Convert.ToInt32(Console.ReadLine());

                    Console.Write("Segundo dado:");
                    dadoDos = Convert.ToInt32(Console.ReadLine());

                    if (apuesta > creditos || apuesta < 0)
                    {
                        Console.WriteLine("Invalida");
                    }

                    if (dadoUno + dadoDos == 11 || dadoUno + dadoDos == 7)
                    {
                        creditos *= 2;
                        Console.WriteLine("En hora buena, has ganado! (apostado se duplica("+creditos+"))");                        
                    }
                    else
                    {
                        Console.WriteLine("Oh dang it! Has perdido todo lo apostado!");
                        apuesta = 0;
                    }
                }

            } while (apuesta != 0 || creditos < 1);
            if (creditos < 1)
            {
                Console.WriteLine("Perdiste todos tus creditos!");
            }
            else
            {
                Console.WriteLine("Dejaste de apostar, y te fuiste con "+creditos+" creditos en tus bolsillos");
            }

        }
    }
}
