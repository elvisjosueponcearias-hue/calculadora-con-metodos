# calculadora-con-metodos

namespace Calculadora
{
    class Program
    {
        static double Sumar(double num1, double num2)
        {
            return num1 + num2;
        }
        static double Restar(double num1, double num2)

        {
            return num1 - num2;
        }

        static double Multiplicar(double num1, double num2)
        {
            return num1 * num2;
        }

        static double Dividir(double num1, double num2)
        {
            if (num2 == 0)
            {

                Console.WriteLine("Error: no se puede dividir entre cero.");
                return 0;
            }

            return num1 / num2;
        }

        static double LeerNumero(string mensaje)
        {
            Console.Write(mensaje);
            return double.Parse(Console.ReadLine());
        }

        static void Main()
        {
            Console.WriteLine("===== CALCULADORA =====");

            double num1 = LeerNumero("Ingrese primer número: ");
            double num2 = LeerNumero("Ingrese segundo número: ");

            Console.WriteLine();

            Console.WriteLine("Suma: " + Sumar(num1, num2));
            Console.WriteLine("Resta: " + Restar(num1, num2));
            Console.WriteLine("Multiplicación: " + Multiplicar(num1, num2));
            Console.WriteLine("División: " + Dividir(num1, num2));
        }
    }
}
