# Matheus-Fernandes-da-Silva
calculadora console
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;

namespace Calculadora_Console
{
    class Program //Calculadora 
    {
        static void Main(string[] args)
        {
        inicio:
            Console.WriteLine("Digite o primeiro número: ");
            float numero1 = float.Parse(Console.ReadLine());

            Console.WriteLine("Digite a operação");
            string operação = Console.ReadLine();

            Console.WriteLine("Digite o segundo número: ");
            float numero2 = float.Parse(Console.ReadLine());

            float resultado = 0;
            string nomeDaOperacao = "";

            if (operação == "+")
            {
                resultado = numero1 + numero2;
                nomeDaOperacao = "Soma";
            }
            else if (operação == "-")
            {
                resultado = numero1 - numero2;
                nomeDaOperacao = "subtração";
            }
            else if (operação == "/")
            {
                resultado = numero1 / numero2;
                nomeDaOperacao = "Divisão";
            }
            else if (operação == "x")
            {

                resultado = numero1 * numero2;
                nomeDaOperacao = "mutiplicação";
            }
            else
            {
                Console.WriteLine("operação Inválida");
            }
            Console.WriteLine("O resultado da operação  " + nomeDaOperacao + " é = " + resultado);


            Thread.Sleep(3000);
            goto inicio; // voltar para o inicio

        }
    }
}
