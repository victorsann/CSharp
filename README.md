
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/115932830-19b66200-a464-11eb-8578-5a9249c16268.png">
</div>  
<br>
<img src="https://img.shields.io/static/v1?label=CSHARP&message=Language&color=purple&style=for-the-badge&logo="/>


Desenvolvida e mantida pela Micrsoft, o C# é uma linguagem de programação moderna, orientada a objetos e fortemente tipada. Criada com o intuito de 
suprir a necessidade que a Microsoft tinha de uma linguagem que atendesse a requisição de ser multiplataforma, substituindo a anteriormente utilizada
Java, sendo ambas muitas parecidas. O C# é utilizado em conjunto com a máquina virtual disponibilizada pelo .NET, cgamada de Common Language Runtime
(CLR), sendo convertida em machine code em um processo chamado de JIT. 


<h2>Hellow World</h2>


Um dos primeiros passos ao iniciar em uma nova tecnologia é o clássico Hello World, bastante eficaz para enter a estrutura básica de uma linguagem.
Sendo assim, abaixo está um exemplo de Hellow World em C#:


      using System;

      class Hello
      {
          static void Main()
          {
              Console.WriteLine("Hello, World");
          }
      }

O "Hello World" começa com a diretiva <strong>using</strong> que referencia o namespace <strong>System</strong>. O namespace nada mais é que uma
definição de acesso hierárquico aos recursos dos programas e bibliotecas C#, sendo o Console um dos vários recursos do sistema. A classe criada e
chamada de Hello possui apenas o método Main() como seu recurso. Sendo definido como static, fazendo com que o método não precise ser referenciado,
ele assume a caracterítica de entry da classe Hello. Com a definição de acesso aos recursos do System é possível usar a classe Console, que por sua
vez possui o método WriteLine(). Esse método é o responsável por fazer o binding da string "Hello, World" no Console.


<div align="center">
  <h1>Tipos e Variáveis</h1>
</div>


Os tipos se manifestam de duas formas no C#: value types e reference types;


<h1>Value Types</h1>


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


<h1>Reference types</h1>


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

Obs.: Variáveis explicitamente tipada que carreguem valores decimais recebem um prefixo de definição:

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


<div align="center">
  <h1>Operadores</h1>
</div>


O C# fornece vários operadores. Muitos deles são suportados pelos tipos internos e permitem que a execução de operações básicas com valores desses tipos.
Esses operadores incluem os seguintes grupos:


<h2>Aritméticos</h2>


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


<h2>Operadores de Acesso</h2>


Os seguintes operadores e expressões são usados ao acessar um membro de tipo:


<h2>Acesso de Membro</h2>


Para acessar um membro de um namespace ou tipo usa-se o token . , como o exemplo a seguir demonstra:

> using System.Collections.Generic;


<h2>Operador indexador []</h2>


Colchetes, [], são normalmente usados para acesso a array, indexador ou elemento de ponteiro. O exemplo a seguir demonstra como acessar
os elementos da matriz:

    int[] fib = new int[10];
    fib[0] = fib[1] = 1;
    for (int i = 2; i < fib.Length; i++)
    {
        fib[i] = fib[i - 1] + fib[i - 2];
    }
    Console.WriteLine(fib[fib.Length - 1]);  // output: 55
    
    double[,] matrix = new double[2,2];
    matrix[0,0] = 1.0;
    matrix[0,1] = 2.0;
    matrix[1,0] = matrix[1,1] = 3.0;
    var determinant = matrix[0,0] * matrix[1,1] - matrix[1,0] * matrix[0,1];
    Console.WriteLine(determinant);  // output: -3


<h1>Operadores de Teste</h1>


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


<h1>Operador Condicional Ternário</h1>


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


<h1>?? e ?? = operadores</h1>


O operador de coalescência nula ?? retorna o valor de seu operando à esquerda, se não for nulo; caso contrário, avalia o operando à direita e retorna seu
resultado. O operador ?? não avalia seu operando à direita se o operando à esquerda for avaliado como não nulo.

<br>

Disponível no C# 8.0 e posterior, o operador de atribuição de coalescência nula ??= atribui o valor de seu operando à direita a seu operando à esquerda
apenas se o operando à esquerda for avaliado como nulo. O operador ??= não avalia seu operando à direita se o operando à esquerda for avaliado como não
nulo.


    List<int> numbers = null;
    int? a = null;
    
    (numbers ??= new List<int>()).Add(5);
    Console.WriteLine(string.Join(" ", numbers));  // output: 5
    
    numbers.Add(a ??= 0);
    Console.WriteLine(string.Join(" ", numbers));  // output: 5 0
    Console.WriteLine(a);  // output: 0


O operando à esquerda do operador ??= deve ser uma variável, uma propriedade ou um elemento indexador.

<br>

No C# 7.3 e anteriores, o tipo de operando esquerdo do ?? deve ser um tipo de referência ou um tipo de valor anulável. Começando com C# 8.0,
esse requisito é substituído pelo seguinte: o tipo de operando esquerdo do ?? e ??= operadores não podem ser um tipo de valor não anulável. Dentro
Em particular, começando com C# 8.0, é possível usar os operadores de coalescência nula com parâmetros de tipo irrestritos:


    private static void Display<T>(T a, T backup)
    {
        Console.WriteLine(a ?? backup);
    }
    

Os operadores de coalescência nula são associativos à direita. Ou seja, expressões da forma:


    a ?? b ?? c
    d ??= e ??= f
    

são avaliados como:

    a ?? (b ?? c)
    d ??= (e ??= f)

