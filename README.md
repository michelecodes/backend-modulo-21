# Módulo 21

## O que são Expressões Lamba
Em Java, expressões lambda são uma característica introduzida na versão 8 da linguagem. Elas proporcionam uma maneira concisa e funcional de expressar instâncias de interfaces funcionais (interfaces que têm apenas um método abstrato). As expressões lambda são frequentemente usadas em conjunto com interfaces funcionais para criar implementações mais compactas e elegantes de código.

### Sintaxe básica:

      (parametros) -> expressao

### Exemplo
      // Usando uma expressão lambda para implementar uma interface funcional
      interface OperacaoMatematica {
          int operar(int a, int b);
      }
      
      public class ExemploLambda {
          public static void main(String[] args) {
              // Expressão lambda para uma adição
              OperacaoMatematica adicao = (a, b) -> a + b;
              System.out.println("Soma: " + adicao.operar(5, 3));
      
              // Expressão lambda para uma subtração
              OperacaoMatematica subtracao = (a, b) -> a - b;
              System.out.println("Subtração: " + subtracao.operar(5, 3));
          }
      }

Neste exemplo, a interface funcional OperacaoMatematica possui um único método abstrato chamado operar. Usando expressões lambda, criamos implementações concisas dessa interface para realizar operações de adição e subtração.

As expressões lambda são especialmente úteis quando você precisa passar funcionalidades como argumentos para métodos, como é o caso de muitos métodos das API de Streams introduzidas no Java 8. Elas ajudam a reduzir a verbosidade do código, tornando-o mais legível e expressivo.

Vale ressaltar que as expressões lambda em Java têm algumas regras e restrições, e nem todas as interfaces funcionais são compatíveis com elas. Além disso, desde o Java 8, a linguagem tem evoluído, e novos recursos foram adicionados em versões subsequentes.

