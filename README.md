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

## Parênteses e Colchetes nas Expressões Lamba

Em expressões lambda em Java, os parênteses e colchetes são usados de maneiras específicas e podem afetar o comportamento da lambda, especialmente quando se trata de parâmetros e referências de métodos.

### Parênteses:

- Com parâmetros: Se uma expressão lambda tem zero ou mais de um parâmetro, você deve usar parênteses em torno dos parâmetros, a menos que haja exatamente um parâmetro sem tipo, nesse caso, os parênteses são opcionais.
- Por exemplo:

              // Com parâmetros
            (a, b) -> a + b
            (String s) -> System.out.println(s)
            
            // Sem parâmetros
            () -> System.out.println("Sem parâmetros")
  - Sem parâmetros: Quando não há parâmetros, você ainda precisa usar parênteses vazios () para indicar a lista de parâmetros.

### Colchetes:

- Corpo da expressão lambda: O corpo de uma expressão lambda pode ser uma única expressão ou um bloco de código. Se o corpo contiver mais de uma expressão, você deve usar colchetes {} para envolver o bloco e explicitamente usar a palavra-chave return se o valor de retorno for necessário.
            // Uma única expressão
            (a, b) -> a + b
            
            // Bloco de código com mais de uma expressão
            (a, b) -> {
                int result = a + b;
                return result;
            }
  ### Referências de Método:

Em vez de usar expressões lambda, você pode usar referências de método quando estiver chamando um método existente. Existem quatro tipos de referências de método:
- Referência para um método estático:
            // Sintaxe: NomeDaClasse::metodoEstatico
            Math::max
- Referência para um método de instância de um objeto particular:
            // Sintaxe: instancia::metodoDeInstancia
            String::length
- Referência para um método de instância de um tipo particular:
            // Sintaxe: NomeDaClasse::metodoDeInstancia
            String::toUpperCase
- Referência para um construtor:
            // Sintaxe: NomeDaClasse::new
            ArrayList::new

As referências de método ajudam a simplificar a sintaxe quando você está chamando métodos existentes. Elas são uma alternativa concisa e legível às expressões lambda, especialmente quando a lambda apenas chama um método existente sem adicionar lógica adicional.

### Exemplo
            // Usando referência de método para um método estático
            OperacaoMatematica adicao = Integer::sum;
            
            // Usando referência de método para um método de instância de um objeto particular
            StringConverter converter = String::toUpperCase;
            
            // Usando referência de método para um construtor
            List<String> lista = ArrayList::new;

Em resumo, parênteses, colchetes e referências de método são elementos importantes ao trabalhar com expressões lambda em Java. Eles fornecem flexibilidade e concisão ao expressar comportamentos funcionais de maneira mais elegante.










