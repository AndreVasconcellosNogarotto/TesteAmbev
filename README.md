# TesteAmbev
Questionários de teste Ambev


Questionário 1 
using System.Globalization;

namespace TesteEntrevista
{
    public class ContaBancaria
    {
        public int Numero { get; private set; }
        public string Titular { get; set; }
        public double Saldo { get; private set; }
        
        private const double TaxaSaque = 3.50;

        public ContaBancaria(int numero, string titular, double depositoInicial = 0.0)
        {
            Numero = numero;
            Titular = titular;
            
            if (depositoInicial > 0)
            {
                Depositar(depositoInicial);
            }
        }
        
        public void Depositar(double valor)
        {
            if (valor > 0)
            {
                Saldo += valor;
            }
        }
        
        public void Sacar(double valor)
        {
            Saldo -= valor + TaxaSaque;
        }
        
        public override string ToString()
        {
            return $"Conta {Numero}, Titular: {Titular}, Saldo: $ {Saldo.ToString("F2", CultureInfo.InvariantCulture)}";
        }
    }
}

Questionário 2 

