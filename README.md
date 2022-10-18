
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/115932830-19b66200-a464-11eb-8578-5a9249c16268.png">
</div>  
<br>
<img src="https://img.shields.io/static/v1?label=CSHARP&message=Language&color=purple&style=for-the-badge&logo="/>


Desenvolvida e mantida pela Microsoft, C# é uma linguagem de programação moderna, orientada a objetos e fortemente tipada. A linguagem permite a criação de unúmeros tipos de aplicações robustas e seguras que serão executadas no ambiente .Net. Sendo fortemente inspirada na família C de linguagens, o C# é imediatamente familiar a desenvolvedores C, C++, Java e JavaScript.

Criada com o intuito de compor o ambiente .Net e ser executada no próprio, este sendo um sistema de execução virtual composto por uma common language runtime (CRL) e um conjuto de bibliotecas de classes. A CRL é a implementação de uma common language infrastructure (CLI) desenvolvida pela Microsoft. A CLI, por sua vez, é a base para a criação, execução e desenvolvimento do ambiente no qual lianguagens e suas bibliotecas trabalham em conjunto.

<h1>.NET</h1>

Entender a plataforma na qual a linguagem em questão opera, se e como esta é compilada e quais recursos são disponibilizados para cumprir este propósito, é essecial para se obter proficiência na mesma. Portanto, antes de destrincharmos os meandros da C#, iremos entender o básico sobre o ambiente .NET.

Descrevendo de forma simplória, o .NET é uma plataforma de desenvolvimento de aplicações de diversas proporções e tipos, que se estendem de <i>console apps</i> a <i>API's</i> robustas, mobile apps, ou mesmo <i>games</i>. A plataforma ainda conta com inúmeras features que são constantemente atualizadas para permitir que os desenvolvedores escrevam de forma produtiva códigos confiáveis ​​e de alto desempenho. Alugmas delas são:

- [Asynchronous code](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/)
- [Attributes](https://learn.microsoft.com/en-us/dotnet/standard/attributes/)
- [Reflection](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/reflection)
- [Code analyzers](https://learn.microsoft.com/en-us/dotnet/fundamentals/code-analysis/overview)
- [Delegates and lambdas](https://learn.microsoft.com/en-us/dotnet/standard/delegates-lambdas)
- [Events](https://learn.microsoft.com/en-us/dotnet/standard/events/)
- [Exceptions](https://learn.microsoft.com/en-us/dotnet/standard/exceptions/)
- [Garbage collection](https://learn.microsoft.com/en-us/dotnet/standard/automatic-memory-management)
- [Generic types](https://learn.microsoft.com/en-us/dotnet/standard/generics)
- [LINQ (Language Integrated Query).](https://learn.microsoft.com/en-us/dotnet/standard/linq/)
- [Parallel programming](https://learn.microsoft.com/en-us/dotnet/standard/parallel-programming/)
- [Type system](https://learn.microsoft.com/en-us/dotnet/standard/base-types/common-type-system)
- [Unsafe code](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/unsafe-code)

<h2>Arquitetura .NET</h2>

O código fonte escrito em C# é compilado em uma [intermediate language](https://learn.microsoft.com/en-us/dotnet/standard/managed-code)(IL) que está em conformidade com as especificações da CLI. O código IL e seus recursos, tais como bitmaps e strings, são armazenados em um assembly(conjunto), normalmente sendo um arquivo <i>.dll</i>. Esse arquivo ainda contém um manifesto que descreve informações sobre o tipo de assembly, sua versão e cultura.

Quando um programa em C# é executado, o assembly é carregado na CLR. Com isso, a CLR performa a conversão da intermediate language através do  Just-in-time compilation process para obter código nativo. A CLR ainda provê outros serviços relacionados com a coleta automática de lixo (ou garbage collection), manipulação de exceções e gerenciamento de recursos. O código que é executado pela CLR é por vezes chamado de "managed code", já o "unmanaged code" é compilado em código nativo correspondente a plataforma especificada.

<h2>Using .NET</h2>

Aplicações e bibliotecas .NET são desenvolvidas a partir de um código fonte ([C#](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/#specifying-types-in-variable-declarations), [F#](https://learn.microsoft.com/en-us/dotnet/fsharp/language-reference/type-inference) ou [Visual Basic](https://learn.microsoft.com/en-us/dotnet/visual-basic/programming-guide/language-features/variables/local-type-inference)) e um arquivo de projeto, utilizando a [.NET CLI](https://learn.microsoft.com/en-us/dotnet/core/tools/) ou um ambiente de desenvolvimento integrado (IDE), como o [Visual Studio](https://visualstudio.microsoft.com/). 

para que seja possível prosseguir nos meandros da linguagem da qual esta documentação se trata, é preciso ter instalado o ambiente de criação mínimo, sendo neste caso uma IDE.


<h1>Hellow World</h1>

Um dos primeiros passos ao iniciar em uma nova tecnologia é o clássico Hello World, bastante eficaz para enter a estrutura básica de uma linguagem. Sendo assim, abaixo está um exemplo de Hellow World em C#:


      using System;

      class Hello
      {
          static void Main()
          {
              Console.WriteLine("Hello, World");
          }
      }

O "Hello World" começa com a diretiva <strong>using</strong> que referencia o namespace <strong>System</strong>. O namespace nada mais é que uma definição de acesso hierárquico aos recursos dos programas e bibliotecas C#, sendo o Console um dos vários recursos do sistema. A classe criada e chamada de Hello possui apenas o método Main() como seu recurso. Sendo definido como static, fazendo com que o método não precise ser referenciado, ele assume a caracterítica de entry da classe Hello. Com a definição de acesso aos recursos do System é possível usar a classe Console, que por sua vez possui o método WriteLine(). Esse método é o responsável por fazer o binding da string "Hello, World" no Console.

<h1>Tipos e Variáveis</h1>

Sendo uma linguagem orientada a objetos, ```component-oriented```, o C# provê estruturas de desenvolvimento para suprir diretamente estes conceitos


Os tipos se manifestam de duas formas no C#: value types e reference types;


<h2>Value Types</h2>


Variáveis de value types cotém diretamente seus valores. Os tipos internos do Value Types são divididos em simple types, enum types, structure
types, nullable value types, e tuple value types. 


<h2>Tipos numéricos integrais (Simple Types)</h2>


Os tipos numéricos integrais representam números inteiros. Todos os tipos numéricos integrais são tipos de valor. Eles também são tipos
simples e podem ser inicializados com literais. Todos os tipos numéricos integrais suportam operadores aritméticos, lógicos bit a bit,
de comparação e de igualdade.

O C# suporta os seguintes tipos integrais predefinidos:

| C# Tipo/Palavra-chave  |                      Alcance                            |            Tamanho                |   .NET type   |
| ---------------------- | ------------------------------------------------------  | --------------------------------- | ------------- | 
| sbyte                  | -128 to 127                                             | Unsigned 8-bit integer            | System.SByte  |
| byte                   |  0 to 255                                               | Signed 8-bit integer              | System.Byte   |
| short                  | -32,768 to 32,767                                       | Signed 16-bit integer             | System.Int16  |
| ushort                 | 0 to 65,535                                             | Unsigned 16-bit integer           | System.UInt16 |
| int                    | -2,147,483,648 to 2,147,483,647                         | Signed 32-bit integer             | System.Int32  |
| uint                   | 0 to 4,294,967,295                                      | Unsigned 32-bit integer           | System.UInt32 |
| long                   | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | Signed 64-bit integer             | System.Int64  |
| ulong                  | 0 to 18,446,744,073,709,551,615                         | Unsigned 64-bit integer           | System.UInt64 |
| nint                   | Depends on platform                                     | Signed 32-bit or 64-bit integer   | System.IntPtr |
| nuint                  | Depends on platform                                     | Unsigned 32-bit or 64-bit integer | System.UIntPtr|


<h2>Tipos numéricos de ponto flutuante (Simple Types)</h2>


Os tipos numéricos de ponto flutuante representam números reais. Todos os tipos numéricos de ponto flutuante são tipos de valor. Eles também
são tipos simples e podem ser inicializados com literais. Todos os tipos numéricos de ponto flutuante oferecem suporte a operadores aritméticos,
de comparação e de igualdade.

O C# oferece suporte aos seguintes tipos de ponto flutuante predefinidos:


|  C# Tipo/Palavra-chave  |         Alcance Aproxiamdo         |   Precisão   |   Tamanho   |     .NET type      |
| ----------------------- | ---------------------------------- | ------------- | ----------- | ------------------ | 
| float	                  | ±1.5 x 10(−45) to ±3.4 x 10(38)	   | ~6-9 digits   |   4 bytes   | System.Singlesbyte |
| double	                | ±5.0 × 10(−324) to ±1.7 × 10(308)  | ~15-17 digits |   8 bytes   | System.Double      |
| decimal	                | ±1.0 x 10(-28) to ±7.9228 x 10(28) | 28-29 digits  |   16 bytes  | System.Decimal     |


<h2>bool (Simple Types)</h2>


A palavra-chave bool type é um alias para o tipo de estrutura .NET System.Boolean que representa um valor booleano, que pode ser true ou false.

Para realizar operações lógicas com valores do tipo booleano, usa-se operadores lógicos booleanos. O tipo bool é o tipo de resultado dos operadores
de comparação e igualdade. Uma expressão booleana pode ser uma expressão condicional de controle nas instruções if, do, while e for e no operador
condicional ?:.

O valor padrão do tipo bool é falso.


    bool check = true;
    Console.WriteLine(check ? "Checked" : "Not checked");  // output: Checked
    
    Console.WriteLine(false ? "Checked" : "Not checked");  // output: Not checked


<h2>char (Simple Types)</h2>


A palavra-chave char type é um alias para o tipo de estrutura .NET System.Char que representa um caractere Unicode UTF-16.


  |  Tipo  |      Alcance	    |   Tamanho   |  .NET type  |
  | ------ | ---------------- | ----------- | ----------- |
  |  char  | U+0000 to U+FFFF	|   16 bit    | System.Char |


O tipo char oferece suporte a operadores de comparação, igualdade, incremento e decremento. Além disso, para operandos char, os operadores
lógicos aritméticos e bit a bit executam uma operação nos códigos de caracteres correspondentes e produzem o resultado do tipo int.

O tipo string representa texto através de uma sequência de valores char.

O valor padrão de um char é \0, que equivale a U+0000.


<h2>Enumeration types</h2>


Um tipo de enumeração (ou tipo enum) é um tipo de valor definido por um conjunto de constantes nomeadas do tipo numérico. Para definir um tipo
de enumeração, usa-se a palavra-chave enum e especifica-se os nomes dos membros de enum:


    enum Season
    {
        Spring,
        Summer,
        Autumn,
        Winter
    }


Por padrão, os valores constantes associados de membros enum são do tipo int; eles começam com zero e aumentam em 1 seguindo a ordem do texto
de definição. É possível especificar explicitamente qualquer outro tipo numérico integral como um tipo subjacente de um tipo de enumeração.
Também é possível especificar explicitamente os valores constantes associados, como mostra o exemplo a seguir:


    enum ErrorCode : ushort
    {
        None = 0,
        Unknown = 1,
        ConnectionLost = 100,
        OutlierReading = 200
    }


<h2>Structure types</h2>


Um Structure type (ou tipo de estrutura) é um tipo de valor que pode encapsular dados e funcionalidades relacionadas. Nele usa-se a palavra-chave
struct para definir um tipo de estrutura:


    public struct Coords
    {
        public Coords(double x, double y)
        {
            X = x;
            Y = y;
        }
    
        public double X { get; }
        public double Y { get; }
    
        public override string ToString() => $"({X}, {Y})";
    }


Os tipos de estrutura têm semântica de valor. Ou seja, uma variável de um tipo de estrutura contém uma instância do tipo. Por padrão, os valores
das variáveis são copiados na atribuição, passando um argumento para um método ou retornando um resultado do método. No caso de uma variável do
tipo de estrutura, uma instância do tipo é copiada. 


<h2>Nullable value types</h2>


Um tipo de valor nullable T? representa todos os valores de seu tipo de valor subjacente T e um valor nulo adicional. Por exemplo, é possível
atribuir qualquer um dos três valores a seguir a um bool? variável: verdadeiro, falso ou nulo. Um tipo de valor subjacente T não pode ser um
tipo de valor nullable em si.

Qualquer tipo de valor nullable é uma instância da estrutura genérica System.Nullable<T>. É possível se referir a um tipo de valor nullable com um
tipo subjacente T em qualquer uma das seguintes formas intercambiáveis: <strong>nullable<T></strong> ou <strong>T ?.</strong>

Normalmente, usa-se um tipo de valor nullable quando é preciso representar o valor indefinido de um tipo de valor subjacente. Por exemplo, uma
variável booleana só pode ser verdadeira ou falsa. No entanto, em algumas aplicações, um valor de variável pode ser indefinido ou ausente. Por
exemplo, um campo de banco de dados pode conter verdadeiro ou falso ou pode não conter nenhum valor, ou seja, NULL. Nesse cenário é possível
usar o <strong>bool?</strong> como definição. 


<h2>Declaração e Atribuição</h2>


Como um valor é implicitamente conversível para nullable, é possível atribuir um valor a uma variável de um tipo de valor nullable como se a mesma
fosse seu tipo de valor subjacente. Sendo possível atribuir o valor nulo a mesma. Por exemplo:


    double? pi = 3.14;
    char? letter = 'a';
    
    int m2 = 10;
    int? m = m2;
    
    bool? flag = null;
    
    // An array of a nullable value type:

    int?[] arr = new int?[10];
    

O valor padrão de um nullable representa nulo, ou seja, é uma instância cuja propriedade <strong>Nullable<T></strong>.HasValue retorna falso.


<h2>Tuple types</h2>


Disponível no C# 7.0 e versões posteriores, o recurso de tuplas fornece sintaxe concisa para agrupar vários elementos de dados em uma estrutura de
dados leve. O exemplo a seguir mostra como é possível declarar uma variável de tupla, inicializá-la e acessar seus dados:


    (double, int) t1 = (4.5, 3);
    Console.WriteLine($"Tuple with elements {t1.Item1} and {t1.Item2}.");

    // Output:

    // Tuple with elements 4.5 and 3.
    
    (double Sum, int Count) t2 = (4.5, 3);
    Console.WriteLine($"Sum of {t2.Count} elements is {t2.Sum}.");

    // Output:

    // Sum of 3 elements is 4.5.


<h2>Reference types</h2>


Os tipos de dados internos do reference type são divididos em: 

|  C# type keyword	|   .NET type   |
| ----------------- | ------------- |
| object	          | System.Object |
| string	          | System.String |
| dynamic	          | System.Object |


<h2>Object</h2>


O tipo de objeto é um alias para System.Object em .NET. No sistema de tipo unificado do C#, todos os tipos, predefinidos e definidos pelo usuário,
tipos de referência e tipos de valor, herdam direta ou indiretamente de System.Object. É possível atribuir valores de qualquer tipo a variáveis do
tipo de objeto. Qualquer variável de objeto pode ser atribuída a seu valor padrão usando o nulo literal. Quando uma variável de um tipo de valor é
convertida em objeto, é dito que esta está em uma caixa. Quando uma variável do tipo objeto é convertida em um tipo de valor, é dito que ela foi
removida da caixa. 


<h2>String</h2>


O tipo de string representa uma sequência de zero ou mais caracteres(char) Unicode. string é um apelido para System.String em .NET.


    string a = "hello";
    string b = "h";
    

<h2>Dynamic</h2>


O tipo dinâmico indica que o uso da variável e as referências a seus membros ignoram a verificação de tipo em tempo de compilação. Em vez disso, 
essas operações são resolvidas em tempo de execução. 

<br>

<div align="center">
   <h1>Variáveis e Constantes</h1>
</div>

Uma variável é uma unidade de armazenamento de dados. No C# há formas distintas de declar uma variável, elas são: 


<h2>Implicitamente Tipada</h2>


    //Sintaxe:
    
     var <identificador> = <valor/expressão>;
     
     //Exemplos
     
     var quantidade = 18;
     var preco = 14.73;
     var valorTotal = quantidade * preco;
     
     
Durante a compilação o tipo da variável é determinado pelo valor atribuído ou pelo resultado da expressão.
Posteriormente não poderá ser atribuído um valor de tipo diferente à variável.


<h2>Explicitamente Tipada</h2>


    //Sintaxe:

    <tipo> <identificador> = <valor/expressão>;

    //Exemplos

    int idade = 18;
    double precoCusto = 8.50;
    double precoVenda = 12.30d;
    double valorLucro = precoVenda - precoCusto;
    float percentual = 12.5f;


Um valor ou uma expressão pode ser atribuído durante a declaração da variável.

Obs.: Variáveis explicitamente tipadas que carreguem valores decimais recebem um sufixo de definição:

<ul>
 <li>Tipo double: d ou D</li>
 <li>Tipo float: f ou F</li>
 <li>Tipo decimal: m ou M</li>
</ul>

Uma constante possui a mesma definição de armazenamento de uma variável, tendo a diferença clara de imutabilidade do dado armazenado,
além de que um valor deverá ser necessariamente atribuído na declaração.:

    //Sintaxe:

    const <tipo> <identificador> = <valor>;

    //Exemplos

    const double PI = 3.14;
    const int mediaPadrao = 7;


<h2>Arrays</h2>


Array, vetor ou matriz define o armazenamento de multiplos dados em um único elemento. A delcaração de uma matriz é feita definindo o tipo de seus elementos.
Para definir que um array suporte any tipos é preciso especificar objeto como seu tipo. No sistema de tipo unificado do C#, todos os tipos, predefinidos
e definidos pelo usuário, tipos de referência e tipos de valor, herdam direta ou indiretamente do objeto.

> type[] arrayName;

O exemplo a seguir cria matrizes unidimensionais, multidimensionais e irregulares:

    class TestArraysClass
    {
        static void Main()
        {
            // Declare a single-dimensional array of 5 integers.
            int[] array1 = new int[5];
    
            // Declare and set array element values.
            int[] array2 = new int[] { 1, 3, 5, 7, 9 };
    
            // Alternative syntax.
            int[] array3 = { 1, 2, 3, 4, 5, 6 };
    
            // Declare a two dimensional array.
            int[,] multiDimensionalArray1 = new int[2, 3];
    
            // Declare and set array element values.
            int[,] multiDimensionalArray2 = { { 1, 2, 3 }, { 4, 5, 6 } };
    
            // Declare a jagged array.
            int[][] jaggedArray = new int[6][];
    
            // Set the values of the first array in the jagged array structure.
            jaggedArray[0] = new int[4] { 1, 2, 3, 4 };
        }
    }

Um Array tem as propriedades a seguir:

<ul>
  <li>Uma matriz pode ser unidimensional, multidimensional ou denteada.</li>
  <li>
      O número de dimensões e o comprimento de cada dimensão são estabelecidos quando a instância da matriz é criada.
      Esses valores não podem ser alterados durante o tempo de vida da instância.
  </li>
  <li>
     Os valores padrão dos elementos da matriz numérica são definidos como zero e os elementos de referência são definidos como nulos.
  </li>
  <li>
     Uma matriz denteada é uma matriz de matrizes e, portanto, seus elementos são tipos de referência e são inicializados como nulos.
  </li>
  <li>
     As matrizes são indexadas por zero: uma matriz com n elementos é indexada de 0 a n-1.
  </li>
  <li>
    Os elementos da matriz podem ser de qualquer tipo, incluindo um tipo de matriz.
  </li>
  <li>
    Os tipos de array são tipos de referência derivados do tipo base abstrato Array. Todas as matrizes implementam IList e IEnumerable.
    Você pode usar matrizes de iteração foreach em C#. Uma vez que as matrizes de dimensão única também implementam IList<T> e IEnumerable<T>.
  </li>
</ul>

<br>

<div align="center">
  <h1>Operadores</h1>
</div>


O C# fornece vários operadores. Muitos deles são suportados pelos tipos internos e permitem que a execução de operações básicas com valores desses tipos.
Esses operadores incluem os seguintes grupos:


<h1>Aritméticos</h1>


Os seguintes operadores realizam operações aritméticas com operandos unários de tipos numéricos:


<h2>Operador de Incremento</h2>


O operador de incremento unário ++ incrementa seu operando em 1. O operando deve ser uma variável, um acesso de propriedade ou um acesso de indexador.
O operador de incremento é suportado em duas formas: o operador de incremento pós-fixado, x++, e o operador de incremento de pré-fixo, ++x.


<h2>Pós Fixado X++</h2>


O resultado de x ++ é o valor de x antes da operação, como mostra o exemplo a seguir:


    int i = 3;
    Console.WriteLine(i);   // output: 3
    Console.WriteLine(i++); // output: 3
    Console.WriteLine(i);   // output: 4


<h2>Pré Fixado ++X</h2>


O resultado de ++ x é o valor de x após a operação, como mostra o exemplo a seguir:


    double a = 1.5;
    Console.WriteLine(a);   // output: 1.5
    Console.WriteLine(++a); // output: 2.5
    Console.WriteLine(a);   // output: 2.5


<h2>Operador de Decremento</h2>


O operador de decremento unário - diminui seu operando em 1. O operando deve ser uma variável, um acesso de propriedade ou um acesso de indexador.
O operador de decremento é suportado em duas formas: o operador de decremento pós-fixado, x--, e o operador de decremento de pré-fixo, --x.


<h2>Pós Fixado X--</h2>


O resultado de x-- é o valor de x antes da operação, como mostra o exemplo a seguir:


    int i = 3;
    Console.WriteLine(i);   // output: 3
    Console.WriteLine(i--); // output: 3
    Console.WriteLine(i);   // output: 2

<h2>Pré Fixado --X</h2>


O resultado de --x é o valor de x após a operação, como mostra o exemplo a seguir:


    double a = 1.5;
    Console.WriteLine(a);   // output: 1.5
    Console.WriteLine(--a); // output: 0.5
    Console.WriteLine(a);   // output: 0.5


<h2>Operadores unários de mais e menos</h2>


O operador unário + retorna o valor de seu operando. O operador unário - calcula a negação numérica de seu operando.


    Console.WriteLine(+4);     // output: 4
    
    Console.WriteLine(-4);     // output: -4
    Console.WriteLine(-(-4));  // output: 4
    
    uint a = 5;
    var b = -a;
    Console.WriteLine(b);            // output: -5
    Console.WriteLine(b.GetType());  // output: System.Int64
    
    Console.WriteLine(-double.NaN);  // output: NaN


Os seguintes operadores realizam operações aritméticas com operandos binários de tipos numéricos:


<h2>Operador de Multiplicação *</h2>


O operador de multiplicação * calcula o produto de seus operandos:


    Console.WriteLine(5 * 2);         // output: 10
    Console.WriteLine(0.5 * 2.5);     // output: 1.25
    Console.WriteLine(0.1m * 23.4m);  // output: 2.34


<h2>Operador de Divisão /</h2>


O operador de divisão / divide seu operando à esquerda por seu operando à direita.


<h2>Números Inteiros</h2>


Para os operandos de tipos inteiros, o resultado do operador / é do tipo inteiro e é igual ao quociente dos dois operandos arredondados para zero:


    Console.WriteLine(13 / 5);    // output: 2
    Console.WriteLine(-13 / 5);   // output: -2
    Console.WriteLine(13 / -5);   // output: -2
    Console.WriteLine(-13 / -5);  // output: 2


Para obter o quociente dos dois operandos como um número de ponto flutuante, use o tipo flutuante, duplo ou decimal:


    Console.WriteLine(13 / 5.0);       // output: 2.6
    
    int a = 13;
    int b = 5;
    Console.WriteLine((double)a / b);  // output: 2.6


<h2>Números Decimais</h2>


Para os tipos float, double e decimal, o resultado do operador / é o quociente dos dois operandos:


    Console.WriteLine(16.8f / 4.1f);   // output: 4.097561
    Console.WriteLine(16.8d / 4.1d);   // output: 4.09756097560976
    Console.WriteLine(16.8m / 4.1m);   // output: 4.0975609756097560975609756098


<h2>Operador %</h2>


O operador restante% calcula o restante após dividir seu operando à esquerda por seu operando à direita.


<h2>Números Inteiros</h2>


Para os operandos de tipos inteiros, o resultado de a % b é o valor produzido por a - (a / b) * b. O sinal do resto diferente de zero é o mesmo do
operando esquerdo, como mostra o exemplo a seguir:


    Console.WriteLine(5 % 4);   // output: 1
    Console.WriteLine(5 % -4);  // output: 1
    Console.WriteLine(-5 % 4);  // output: -1
    Console.WriteLine(-5 % -4); // output: -1


<h2>Números Decimais</h2>


Para os operandos float e double, o resultado de x % y para o x e y finito é o valor z tal que:

<ul>
  <li>O sinal de z, se diferente de zero, é igual ao sinal de x.</li>
  <li>
      O valor absoluto de z é o valor produzido por | x | - n * | y |onde n é o maior número inteiro possível menor ou igual
       a | x | / | y | e | x | e | y | são os valores absolutos de xey, respectivamente.
  </li>
</ul>

Para os operandos decimais, o operador restante% é equivalente ao operador restante do tipo System.Decimal.

O exemplo a seguir demonstra o comportamento do operador resto com operandos de ponto flutuante:


    Console.WriteLine(-5.2f % 2.0f); // output: -1.2
    Console.WriteLine(5.9 % 3.1);    // output: 2.8
    Console.WriteLine(5.9m % 3.1m);  // output: 2.8


<h2>Operador de Adição +</h2>


O operador de adição + calcula a soma de seus operandos:


    Console.WriteLine(5 + 4);       // output: 9
    Console.WriteLine(5 + 4.3);     // output: 9.3
    Console.WriteLine(5.1m + 4.2m); // output: 9.3


<h2>Operador de Subtração -</h2>


O operador de subtração - subtrai seu operando à direita de seu operando à esquerda:

    Console.WriteLine(47 - 3);      // output: 44
    Console.WriteLine(5 - 4.3);     // output: 0.7
    Console.WriteLine(7.5m - 2.3m); // output: 5.2


<h2>Atribuição Composta</h2>


O exemplo a seguir demonstra o uso de atribuição composta com operadores aritméticos:

    int a = 5;

    a += 9;
    Console.WriteLine(a);  // output: 14
    
    a -= 4;
    Console.WriteLine(a);  // output: 10
    
    a *= 2;
    Console.WriteLine(a);  // output: 20
    
    a /= 4;
    Console.WriteLine(a);  // output: 5
    
    a %= 3;
    Console.WriteLine(a);  // output: 2


<h1>Operadores Lógicos</h1>


Com suas restrições, os operadores lógicos tipicamente são usados com booleans e retornam booleans, executando uma operação entre dois ou mais operandos,
definindo um valor lógico final com base no valor lógico dos operandos que contenham.


<h2>Negação !</h2>


O operador unário de negação(!) calcula a negação lógica de seu operando. Ou seja, ele produz verdadeiro se o operando for avaliado como falso, e falso, se
o operando for avaliado como verdadeiro:


    bool passed = false;

    Console.WriteLine(!passed);  // output: True
    Console.WriteLine(!true);    // output: False


<h2>Conjunção &</h2>


O operador & calcula o AND lógico de seus operandos. O resultado de x & y é verdadeiro se x & y forem avaliados como verdadeiros. Caso contrário, o resultado
é falso.

O operador & avalia ambos os operandos, mesmo se o operando à esquerda for avaliado como falso, de modo que o resultado da operação seja falso, independentemente
do valor do operando à direita.

No exemplo a seguir, o operando à direita do operador & é uma chamada de método, que é realizada independentemente do valor do operando à esquerda:


    bool SecondOperand()
    {
        Console.WriteLine("Second operand is evaluated.");
        return true;
    }
    
    bool a = false & SecondOperand();
    Console.WriteLine(a);

    // Output:

    // Second operand is evaluated.
    // False
    
    bool b = true & SecondOperand();
    Console.WriteLine(b);

    // Output:

    // Second operand is evaluated.
    // True
    

O operador lógico condicional AND && também calcula o AND lógico de seus operandos, mas não avalia o operando direito se o operando esquerdo for avaliado
como falso.


<h2>Conjunção Condicional &&</h2> 


O operador AND lógico condicional &&, também conhecido como operador AND lógico de "curto-circuito", calcula o AND lógico de seus operandos. O resultado de x
&& y é verdadeiro se x & y forem avaliados como verdadeiros. Caso contrário, o resultado é falso. Se x for avaliado como falso, y não será avaliado.

No exemplo a seguir, o operando direito do operador && é uma chamada de método, que não é realizada se o operando esquerdo for avaliado como falso:


    bool SecondOperand()
    {
        Console.WriteLine("Second operand is evaluated.");
        return true;
    }
    
    bool a = false && SecondOperand();
    Console.WriteLine(a);
    // Output:
    // False
    
    bool b = true && SecondOperand();
    Console.WriteLine(b);
    // Output:
    // Second operand is evaluated.
    // True


<h2>Disjunção Exclusiva ^</h2> 


O operador ^ calcula o OU exclusivo lógico, também conhecido como XOR lógico, de seus operandos. O resultado de x ^ y é verdadeiro se x for avaliado como
verdadeiro e y for avaliado como falso, ou x for avaliado como falso e y for avaliado como verdadeiro. Caso contrário, o resultado é falso. Ou seja, para
os operandos bool, o operador ^ calcula o mesmo resultado que o operador de desigualdade !=.


    Console.WriteLine(true ^ true);    // output: False
    Console.WriteLine(true ^ false);   // output: True
    Console.WriteLine(false ^ true);   // output: True
    Console.WriteLine(false ^ false);  // output: False


<h2>Disjunção |</h2>


O operador | calcula o OR lógico de seus operandos. O resultado de x | y é verdadeiro se x ou y for avaliado como verdadeiro. Caso contrário, o resultado é
falso. O operador | avalia ambos os operandos, mesmo se o operando à esquerda for avaliado como verdadeiro, de modo que o resultado da operação seja verdadeiro, independentemente do valor do operando à direita.

No exemplo a seguir, o operando à direita do operador | é uma chamada de método, que é realizada independentemente do valor do operando à esquerda:


    bool SecondOperand()
    {
        Console.WriteLine("Second operand is evaluated.");
        return true;
    }
    
    bool a = true | SecondOperand();
    Console.WriteLine(a);

    // Output:

    // Second operand is evaluated.
    // True
    
    bool b = false | SecondOperand();
    Console.WriteLine(b);

    // Output:

    // Second operand is evaluated.
    // True


O operador lógico condicional OU || também calcula o OR lógico de seus operandos, mas não avalia o operando à direita se o operando à esquerda for verdadeiro.


<h2>Disjunção Condicional ||</h2>


O operador OR lógico condicional ||, também conhecido como o operador OR lógico de "curto-circuito", calcula o OR lógico de seus operandos. O resultado de
x || y é verdadeiro se x ou y for avaliado como verdadeiro. Caso contrário, o resultado é falso. Se x for avaliado como verdadeiro, y não será avaliado.

No exemplo a seguir, o operando à direita do operador || é uma chamada de método, que não é realizada se o operando esquerdo for avaliado como verdadeiro:


    bool SecondOperand()
    {
        Console.WriteLine("Second operand is evaluated.");
        return true;
    }
    
    bool a = true || SecondOperand();
    Console.WriteLine(a);

    // Output:

    // True
    
    bool b = false || SecondOperand();
    Console.WriteLine(b);

    // Output:

    // Second operand is evaluated.
    // True


O operador lógico OR | também calcula o OR lógico de seus operandos, mas sempre avalia ambos os operandos.


<h1>Operadores de Igualdade</h1>


Os operadores == (igualdade) e != (Desigualdade) verificam se seus operandos são iguais ou não.


<h2>Igualdade</h2>


O operador de igualdade == retorna verdadeiro se seus operandos forem iguais, falso caso contrário.

    int a = 1 + 2 + 3;
    int b = 6;
    Console.WriteLine(a == b);  // output: True
    
    char c1 = 'a';
    char c2 = 'A';
    Console.WriteLine(c1 == c2);  // output: False
    Console.WriteLine(c1 == char.ToLower(c2));  // output: True


<h2>Desigualdade</h2>


O operador de desigualdade != Retorna verdadeiro se seus operandos não forem iguais, caso contrário, falso. Para os operandos dos tipos internos, a
expressão x != Y produz o mesmo resultado que a expressão !(X == y). 

O exemplo a seguir demonstra o uso do operador != :


    int a = 1 + 1 + 2 + 3;
    int b = 6;
    Console.WriteLine(a != b);  // output: True
    
    string s1 = "Hello";
    string s2 = "Hello";
    Console.WriteLine(s1 != s2);  // output: False
    
    object o1 = 1;
    object o2 = 1;
    Console.WriteLine(o1 != o2);  // output: True


<h1>Operadores de Comparação</h1>


A comparação < (menor que), > (maior que), <= (menor ou igual) e >= (maior ou igual), também conhecida como relacional, compara seus operandos.
Esses operadores são suportados por todos os tipos numéricos integrais e de ponto flutuante.


<h2>Menor que < </h2>


O operador < retorna verdadeiro se seu operando à esquerda for menor que seu operando à direita, caso contrário, falso:


    Console.WriteLine(7.0 < 5.1);   // output: False
    Console.WriteLine(5.1 < 5.1);   // output: False
    Console.WriteLine(0.0 < 5.1);   // output: True
    
    Console.WriteLine(double.NaN < 5.1);   // output: False
    Console.WriteLine(double.NaN >= 5.1);  // output: False


<h2>Maior que > </h2>


O operador > retorna verdadeiro se seu operando à esquerda for maior que o operando à direita, caso contrário, falso:


    Console.WriteLine(7.0 > 5.1);   // output: True
    Console.WriteLine(5.1 > 5.1);   // output: False
    Console.WriteLine(0.0 > 5.1);   // output: False
    
    Console.WriteLine(double.NaN > 5.1);   // output: False
    Console.WriteLine(double.NaN <= 5.1);  // output: False


<h2>Menor ou Igual que <= </h2>


O operador <= retorna verdadeiro se seu operando à esquerda for menor ou igual ao operando à direita, caso contrário, falso:


    Console.WriteLine(7.0 <= 5.1);   // output: False
    Console.WriteLine(5.1 <= 5.1);   // output: True
    Console.WriteLine(0.0 <= 5.1);   // output: True
    
    Console.WriteLine(double.NaN > 5.1);   // output: False
    Console.WriteLine(double.NaN <= 5.1);  // output: False


<h2>Maior ou Igual que >= </h2>


O operador >= retorna verdadeiro se seu operando à esquerda for maior ou igual ao operando à direita, caso contrário, falso:


    Console.WriteLine(7.0 >= 5.1);   // output: True
    Console.WriteLine(5.1 >= 5.1);   // output: True
    Console.WriteLine(0.0 >= 5.1);   // output: False
    
    Console.WriteLine(double.NaN < 5.1);   // output: False
    Console.WriteLine(double.NaN >= 5.1);  // output: False

<br>

<div align="center">
  <h1>Operadores de Teste</h1>
</div>

<h2>Operador is</h2>


O operador is verifica se o tipo de tempo de execução de um resultado de expressão é compatível com um determinado tipo. Começando com C# 7.0, o operador
is também testa um resultado de expressão em relação a um padrão.

A expressão com o operador de teste de tipo tem a seguinte forma

> E is T

onde E é uma expressão que retorna um valor e T é o nome de um tipo ou parâmetro de tipo. E não pode ser um método anônimo ou uma expressão lambda.


<h2>Operador as</h2>


O operador as converte explicitamente o resultado de uma expressão em uma determinada referência ou tipo de valor anulável. Se a conversão não for possível,
o operador as retornará nulo. Ao contrário de uma expressão de conversão, o operador as nunca lança uma exceção.

> E as T

onde E é uma expressão que retorna um valor e T é o nome de um tipo ou parâmetro de tipo, produz o mesmo resultado que

> E is T ? (T)(E) : (T)null

exceto que E é avaliado apenas uma vez.

O operador as considera apenas as conversões de referência, anuláveis, boxing e unboxing. 

<br>

<div align="center">
  <h1>Operador Condicional Ternário</h1>
</div>

O operador condicional ?:, também conhecido como operador condicional ternário, avalia uma expressão booleana e retorna o resultado de uma das duas expressões,
dependendo se a expressão booleana for avaliada como verdadeira ou falsa, como mostra o exemplo a seguir:


    string GetWeatherDisplay(double tempInCelcius) => tempInCelcius < 20.0 ? "Cold." : "Perfect!";
    
    Console.WriteLine(GetWeatherDisplay(15));  // output: Cold.
    Console.WriteLine(GetWeatherDisplay(27));  // output: Perfect!


Como mostrado no exemplo anterior, a sintaxe do operador condicional é a seguinte:    

> condition ? consequent : alternative

A expressão de condição deve ser avaliada como verdadeira ou falsa. Se a condição for avaliada como verdadeira, a expressão consequente será avaliada e
seu resultado se tornará o resultado da operação. Se a condição for avaliada como falsa, a expressão alternativa será avaliada e seu resultado se tornará
o resultado da operação. Apenas consequente ou alternativa é avaliada.

<br>

<div align="center">
  <h1>Statement keyword</h1>
</div>

O Statement é definido por instruções do programa para tratar, modificar e redefinir dados utilizando estruturas lógicas. Sendo este divididos em:


<h2>if-else</h2>

Uma instrução if identifica qual instrução executar com base no valor de uma expressão booleana. No exemplo a seguir, a condição da variável bool é
definida como verdadeira e, em seguida, verificada na instrução if. A saída é a variável definida como verdadeira.


    bool condition = true;
    
    if (condition)
    {
        Console.WriteLine("The variable is set to true.");
    }
    else
    {
        Console.WriteLine("The variable is set to false.");
    }


A estrutura lógica else define um caminho alternativo caso o parâmetro avaliado não corresponda a condição imposta.


<h2>Switch</h2>

O switch é uma instrução de seleção que escolhe uma única seção switch para executar a partir de uma lista de casos com base em uma correspondência
de padrão com a expressão avaliada.


    using System;
    
    public class Example
    {
       public static void Main()
       {
          int caseSwitch = 1;
    
          switch (caseSwitch)
          {
              case 1:
                  Console.WriteLine("Case 1");
                  break;
              case 2:
                  Console.WriteLine("Case 2");
                  break;
              default:
                  Console.WriteLine("Default case");
                  break;
          }
       }
    }

    /* The example displays the following output: case 1 *\

A instrução switch é frequentemente usada como uma alternativa ao if-else se uma única expressão for testada em três ou mais condições.


<h2>do</h2>


A instrução do executa uma instrução ou um bloco de instruções enquanto uma expressão booleana especificada é avaliada como verdadeira. Como essa
expressão é avaliada após cada execução do loop, um loop do-while é executado uma ou mais vezes. Isso difere do loop while, que é executado zero
ou mais vezes.


    int n = 0;
     do
     {
         Console.WriteLine(n);
         n++;
     } while (n < 5);


<h2>while</h2>
 

A instrução while executa uma instrução ou um bloco de instruções enquanto uma expressão booleana especificada é avaliada como verdadeira. Como
essa expressão é avaliada antes de cada execução do loop, um loop while é executado zero ou mais vezes. Isso difere do loop do, que é executado
uma ou mais vezes.


    int n = 0;
    while (n < 5)
    {
        Console.WriteLine(n);
        n++;
    }


<h2>for</h2>


A instrução for executa uma instrução ou um bloco de instruções enquanto uma expressão booleana especificada é avaliada como verdadeira.
A instrução for define as seções initializer, condition, and iterator :


    for (initializer; condition; iterator)
        body

    //or

    for ( ; ; )
    {
        // Body of the loop.
    }


Todas as três seções são opcionais. O corpo do loop é uma instrução ou um bloco de instruções. O exemplo a seguir mostra a instrução for com
todas as seções definidas:


    for (int i = 0; i < 5; i++)
    {
        Console.WriteLine(i);
    }


<h2>foreach, in</h2>


A instrução foreach executa uma instrução ou um bloco de instruções para cada elemento em uma instância do tipo que implementa a interface
System.Collections.IEnumerable ou System.Collections.Generic.IEnumerable<T>, como mostra o exemplo a seguir:


    var fibNumbers = new List<int> { 0, 1, 1, 2, 3, 5, 8, 13 };
    int count = 0;
    foreach (int element in fibNumbers)
    {
        Console.WriteLine($"Element #{count}: {element}");
        count++;
    }

    Console.WriteLine($"Number of elements: {count}");

    /* output: 

    Element #0: 0
    Element #1: 1
    Element #2: 1
    Element #3: 2
    Element #4: 3
    Element #5: 5
    Element #6: 8
    Element #7: 13
    Number of elements: 8 
    
    *\


<h2>break</h2>


A instrução break termina o loop envolvente mais próximo ou instrução switch em que aparece. O controle é passado para a instrução que segue a
instrução encerrada, se houver.


<h2>Exemplo</h2>


Neste exemplo, a instrução condicional contém um contador que deve contar de 1 a 100; no entanto, a instrução break termina o loop após 4 contagens.


    class BreakTest
    {
        static void Main()
        {
            for (int i = 1; i <= 100; i++)
            {
                if (i == 5)
                {
                    break;
                }
                Console.WriteLine(i);
            }
    
            // Keep the console open in debug mode.

            Console.WriteLine("Press any key to exit.");
            Console.ReadKey();
        }
    }
    
    /*Output: 

        1
        2
        3
        4
    *\

<h2>Continue</h2>


A instrução continue passa o controle para a próxima iteração da instrução while, do, for ou foreach em que aparece.


<h2>Exemplo</h2>


Neste exemplo, um contador é inicializado para contar de 1 a 10. Usando a instrução continue em conjunto com a expressão (i <9),
as declarações entre continue e o final do corpo for são ignoradas nas iterações onde i é menor que 9. Nas últimas duas iterações
do loop for (onde i == 9 e i == 10), a instrução continue não é executada e o valor de i é impresso no console.


    class ContinueTest
    {
        static void Main()
        {
            for (int i = 1; i <= 10; i++)
            {
                if (i < 9)
                {
                    continue;
                }
                Console.WriteLine(i);
            }
    
            // Keep the console open in debug mode.

            Console.WriteLine("Press any key to exit.");
            Console.ReadKey();
        }
    }
    
    /* Output: 
         9 
         10
    *\


<h2>goto</h2>


A instrução goto transfere o controle do programa diretamente para uma instrução rotulada. Um uso comum de goto é transferir o controle
para um rótulo de switch-case específico ou o rótulo padrão em uma instrução switch. A instrução goto também é útil para sair de loops
profundamente aninhados.


<h2>Exemplo</h2>


O exemplo a seguir demonstra o uso de goto em uma instrução switch.


    class SwitchTest
    {
        static void Main()
        {
            Console.WriteLine("Coffee sizes: 1=Small 2=Medium 3=Large");
            Console.Write("Please enter your selection: ");
            string s = Console.ReadLine();
            int n = int.Parse(s);
            int cost = 0;
            switch (n)
            {
                case 1:
                    cost += 25;
                    break;
                case 2:
                    cost += 25;
                    goto case 1;
                case 3:
                    cost += 50;
                    goto case 1;
                default:
                    Console.WriteLine("Invalid selection.");
                    break;
            }
            if (cost != 0)
            {
                Console.WriteLine($"Please insert {cost} cents.");
            }
            Console.WriteLine("Thank you for your business.");
    
            // Keep the console open in debug mode.

            Console.WriteLine("Press any key to exit.");
            Console.ReadKey();
        }
    }
    /*
    Sample Input:  2
    
    Sample Output:
    Coffee sizes: 1=Small 2=Medium 3=Large
    Please enter your selection: 2
    Please insert 50 cents.
    Thank you for your business.
    */


<h2>return</h2>


A instrução de retorno termina a execução do método em que aparece e retorna o controle ao método de chamada. Ele também pode retornar
um valor opcional. Se o método for do tipo void, a instrução return pode ser omitida.


<h2>Exemplo</h2>


No exemplo a seguir, o método CalculateArea () retorna a área da variável local como um valor duplo.


    class ReturnTest
    {
        static double CalculateArea(int r)
        {
            double area = r * r * Math.PI;
            return area;
        }
    
        static void Main()
        {
            int radius = 5;
            double result = CalculateArea(radius);
            Console.WriteLine("The area is {0:0.00}", result);
    
            // Keep the console open in debug mode.
            Console.WriteLine("Press any key to exit.");
            Console.ReadKey();
        }
    }
    // Output: The area is 78.54

<h1>Blocos de Construção do Programa</h1>


Classes e structs são dois dos pricipais blocos de construção do sistema de tipo do .NET. O C# 9 adiciona records, que são uma espécie de classe.
Cada um é essencialmente uma estrutura de dados que encapsula um conjunto de dados e comportamentos que agem juntos como uma unidade lógica. Os
dados e comportamentos são os membros da classe, structs ou records e incluem seus métodos, propriedades, eventos e assim por diante. A frente 
classes serão abordados de forma mais aprofundada, enquando os demais blocos citados serão abordados posterioemente.


<h1>Class</h1>


Um tipo definido como uma classe é um reference type. Em tempo de execução, quando uma variável de um tipo de referência é declarada, seu valor 
é definido como nulo até que ela seja explicitamente instânciada, seja usando o operador new ou através da atribuição de um objeto de tipo
compatível que pode ter sido criado em outro lugar, conforme mostrado no exemplo a seguir:


    //Declaring an object of type MyClass.

    MyClass mc = new MyClass();
    
    //Declaring another object of the same type, assigning it the value of the first object.

    MyClass mc2 = mc;


<h2>Declarando Uma Classe</h2>


As classes são declaradas usando a palavra-chave class seguida por um identificador exclusivo, conforme mostrado no exemplo a seguir:


    //[access modifier] - [class] - [identifier]

    public class Customer
    {
       // Fields, properties, methods and events go here...
    }


A palavra-chave class é precedida pelo nível de acesso. Como public é usado neste caso, qualquer pessoa pode criar instâncias dessa classe.
O nome da classe segue a palavra-chave class. O nome da classe deve ser um nome de identificador C# válido. O restante da definição é o corpo
da classe, onde o comportamento e os dados são definidos. Campos, propriedades, métodos e eventos em uma classe são chamados coletivamente de
membros da classe.


<h2>Acessibilidade</h2>


Cada membro de uma classe tem uma acessibilidade associada, que controla as regiões do texto do programa que podem acessar o membro.
Existem seis formas de acessibilidade possíveis, sendo estas chamadas de modificadores de acesso.


<ul>
  <li><strong>public:</strong> O acesso não é limitado.</li>
  <li><strong>private:</strong> O acesso é limitado a esta classe.</li>
  <li><strong>protected:</strong> O acesso é limitado a esta classe ou classes derivadas desta classe.</li>
  <li><strong>internal:</strong> O acesso é limitado ao assembly atual (.exe ou .dll).</li>
  <li><strong>protected internal:</strong> O acesso é limitado a esta classe, classes derivadas desta classe ou classes dentro do mesmo assembly.</li>
  <li><strong>private protected:</strong>O acesso é limitado a esta classe ou classes derivadas deste tipo dentro do mesmo assembly.</li>
</ul>


<h2>Criando Objetos</h2>


Embora às vezes sejam usados alternadamente, uma classe e um objeto são coisas diferentes. Uma classe define um tipo de objeto, mas não é um
objeto em si. Um objeto é uma entidade concreta com base em uma classe e às vezes é referido como uma instância de uma classe.


Os objetos podem ser criados usando a palavra-chave new seguida do nome da classe na qual o objeto será baseado:


    Customer object1 = new Customer();


<h2>Herança de Classe</h2>


As classes oferecem suporte total à herança, uma característica fundamental da programação orientada a objetos. Ao criar uma classe, é possível
herdar de qualquer outra classe que não esteja definida como sealed, e outras classes podem herdar da classe recém criada e substituir os métodos
virtuais de classe. Além disso, é possível implementar uma ou mais interfaces.

A herança é realizada usando uma derivação, o que significa que uma classe é declarada usando uma classe base da qual herda dados e comportamento.
Uma classe base é especificada anexando-se dois pontos(:) e o nome da classe base após o nome da classe derivada, como é visto a seguir:


    public class Manager : Employee
    {
        // Employee fields, properties, methods and events are inherited
        // New Manager fields, properties, methods and events go here...
    }


Quando uma classe declara uma classe base, ela herda todos os membros da classe base, exceto os construtores


<h2>Membros de Uma Classe</h2>


Os membros de uma classe são membros estáticos ou membros de instância. Membros estáticos pertencem a classes e membros de instância
pertencem a objetos (instâncias de classes).

<br>

A lista a seguir fornece uma visão geral dos tipos de membros que uma classe pode conter.


<h2>Fields</h2>

Um Field ou campo é uma variável de qualquer tipo declarada diretamente em uma classe ou estrutura. Os campos são membros de seu tipo de
conteúdo.

Para acessar um campo em um objeto, é preciso adicionar um ponto após o nome do objeto, seguido pelo nome do campo, como exemplo a seguir:


    CalendarEntry birthday = new CalendarEntry();
    birthday.Day = "Saturday";


Um campo pode receber um valor inicial usando o operador de atribuição quando o campo é declarado. Para atribuir automaticamente o campo Day
para "Monday", por exemplo, Day seria declarado como no exemplo a seguir:


    public class CalendarDateWithInitialization
    {
        public string Day = "Monday";
        //...
    }


<h2>Constants</h2>


Constantes são valores imutáveis que são conhecidos em tempo de compilação e não mudam durante a vida do programa. As constantes são declaradas
com o modificador const. Apenas os tipos internos C# (excluindo System.Object) podem ser declarados como const. Tipos definidos pelo usuário,
incluindo classes, estruturas e matrizes, não podem ser const.

As constantes devem ser inicializadas à medida em que são declaradas. Por exemplo:


    class Calendar1
    {
        public const int Months = 12;
    }


<h2>Properties</h2>


Uma propriedade é um membro que fornece um mecanismo flexível para ler, gravar ou calcular o valor de um campo privado. As propriedades podem ser
usadas como se fossem membros de dados públicos, mas, na verdade, são métodos especiais chamados de accessors. Isso permite que os dados sejam
acessados facilmente e ainda ajuda a promover a segurança e a flexibilidade dos métodos.




<h2>Methods</h2>


Um método é um bloco de código que contém uma série de instruções. Um programa faz com que as instruções sejam executadas chamando o método e
especificando quaisquer argumentos de método necessários. Em C#, toda instrução executada é realizada no contexto de um método.

O método Main é o ponto de entrada para cada aplicativo C# e é chamado pelo common language runtime (CLR) quando o programa é iniciado.

Os métodos são declarados em uma classe, estrutura ou interface especificando o nível de acesso como public  ou private, modificadores opcionais
como abstract  ou sealed, o valor de retorno, o nome do método e quaisquer parâmetros do método. Essas partes juntas são a assinatura do método.

Os parâmetros do método são colocados entre parênteses e separados por vírgulas. Parênteses vazios indicam que o método não requer parâmetros.
A classe a seguir contém quatro métodos:


    abstract class Motorcycle
    {
        // Anyone can call this.

        public void StartEngine() {/* Method statements here */ }
    
        // Only derived classes can call this.

        protected void AddGas(int gallons) { /* Method statements here */ }
    
        // Derived classes can override the base class implementation.

        public virtual int Drive(int miles, int speed) { /* Method statements here */ return 1; }
    
        // Derived classes must implement this.

        public abstract double GetTopSpeed();
    }


<h2>Acessando um Método</h2>


Chamar um método em um objeto é como acessar um campo. Após o nome do objeto, adicione um ponto, o nome do método e parênteses. Os argumentos
são listados entre parênteses e separados por vírgulas. Os métodos da classe Motorcycle podem, portanto, ser chamados como no exemplo a seguir:


    class TestMotorcycle : Motorcycle
    {
    
        public override double GetTopSpeed()
        {
            return 108.4;
        }
    
        static void Main()
        {
    
            TestMotorcycle moto = new TestMotorcycle();
    
            moto.StartEngine();
            moto.AddGas(15);
            moto.Drive(5, 20);
            double speed = moto.GetTopSpeed();
            Console.WriteLine("My top speed is {0}", speed);
        }
    }


<h2>Método Void</h2>


O type void é usado como o tipo de retorno de um método (ou uma função local) para especificar que o método não retorna um valor.


    public static void Display(IEnumerable<int> numbers)
    {
        if (numbers is null)
        {
            return;
        }
    
        Console.WriteLine(string.Join(" ", numbers));
    }


<h2>Events</h2>


Os eventos permitem que uma classe ou objeto notifique outras classes ou objetos quando algo de interesse ocorre. A classe que envia (ou gera) o
evento é chamada de publisher e as classes que recebem (ou tratam) o evento são chamadas de subscribers.


<h2>Operators</h2>

O C# fornece vários operadores. Muitos deles são suportados pelos tipos integrados e permitem a execução de operações básicas com valores desses
tipos. Os operadores foram abordados anteriormente.


<h2>Indexers</h2>

Os indexadores permitem que instâncias de uma classe ou estrutura sejam indexadas da mesma forma que os arrays. O valor indexado pode ser definido
ou recuperado sem especificar explicitamente um tipo ou membro de instância. Os indexadores se parecem com propriedades, exceto que seus acessadores
usam parâmetros.

O exemplo a seguir define uma classe genérica com métodos acessadores get e set simples para atribuir e recuperar valores. A classe Program cria uma
instância dessa classe para armazenar strings.


    using System;
    
    class SampleCollection<T>
    {
       // Declare an array to store the data elements.
       private T[] arr = new T[100];
    
       // Define the indexer to allow client code to use [] notation.
       public T this[int i]
       {
          get { return arr[i]; }
          set { arr[i] = value; }
       }
    }
    
    class Program
    {
       static void Main()
       {
          var stringCollection = new SampleCollection<string>();
          stringCollection[0] = "Hello, World";
          Console.WriteLine(stringCollection[0]);
       }
    }
    // The example displays the following output:
    //       Hello, World.


<h2>Constructors</h2>


Sempre que uma classe ou estrutura é criada, seu construtor é chamado. Uma classe ou estrutura pode ter vários construtores que aceitam argumentos
diferentes. Os construtores permitem ao programador definir valores padrão, limitar a instanciação e escrever código flexível e fácil de ler. 


<h2>Constructors sem Parâmetros</h2>


Se um construtor bão for oferecido para a criada classe, o C# cria um por padrão que instancia o objeto e define variáveis ​​de membro para os valores
padrão. Caso um construtor não for definido para a estrutura, o C# depende de um construtor implícito sem parâmetros para inicializar automaticamente
cada campo com seu valor padrão.


<h2>Sintaxe de um Constructor</h2>


Um construtor é um método cujo nome é igual ao nome de seu tipo. Sua assinatura de método inclui apenas o nome do método e sua lista de parâmetros;
não inclui um tipo de retorno. O exemplo a seguir mostra o construtor de uma classe chamada Person.


    public class Person
    {
       private string last;
       private string first;
    
       public Person(string lastName, string firstName)
       {
          last = lastName;
          first = firstName;
       }
    
       // Remaining implementation of Person class.
    }


<h2>Finalizers</h2>


Finalizadores(que também são chamados de destruidores) são usados ​​para realizar qualquer limpeza final necessária quando uma instância de classe está
sendo coletada pelo garbage collector. Abaixo estão listadas as expecificações relacionadas a um finalizaer:

<ul>
  <li>Finalizadores não podem ser definidos em structs. Eles são usados ​​apenas com classes.</li>
  
  <li>Uma classe pode ter apenas um finalizador.</li>
  
  <li>Os finalizadores não podem ser herdados ou sobrecarregados.</li>
  
  <li>Finalizadores não podem ser chamados. Eles são chamados automaticamente.</li>
  
  <li>Um finalizador não aceita modificadores ou parâmetros.</li>
</ul>

Por exemplo, a seguir está uma declaração de um finalizador para a classe Car:


    class Car
    {
        ~Car()  // finalizer
        {
            // cleanup statements...
        }
    }



<h2>Nested Types</h2>


Um tipo definido em uma classe, estrutura ou interface é chamado de tipo aninhado. Por exemplo:


    public class Container
    {
        class Nested
        {
            Nested() { }
        }
    }


Independentemente de o tipo externo ser uma classe, interface ou estrutura, os tipos aninhados são privados como padrão; eles são
acessíveis apenas a partir do tipo que os contém. No exemplo anterior, a classe Nested é inacessível para tipos externos.


