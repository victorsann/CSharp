
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/115932830-19b66200-a464-11eb-8578-5a9249c16268.png">
</div>  
<br>
<img src="https://img.shields.io/static/v1?label=CSHARP&message=Language&color=purple&style=for-the-badge&logo="/>


Desenvolvida e mantida pela Micrsoft, o C# é uma linguagem de programação moderna, orientada a objetos e de tipagem forte. Por meio de suas feramentas
o C# permite o esenvolvimento de diversos tipos de aplicações seguras e robustas através do ecosistema do .NET. A linguagem é essencialmente utilizada
na plataforma .NET e usa sua máquina virtual(CLR) como meio para ser executada, além de ter disponível uma série de classes prontas para antender aos
requisitos definidos na criação de uma aplicação.<br> O C# foi desenvolvido para suprir a necessidade que a Microsoft tinha de uma linguagem que atendesse
a requisição de ser multiplataforma, assim como o Java, linguagem que esteve presente nos ambentes Windows por um bom tempo. Por um conflito judicial a
empresa passou a não poder utilizar o Java em seus projetos, o que levou em fim acriação do .NET e da liguagem C#.


<h2>Hellow World</h2>


Um dos primeiros passos ao iniciar em uma nova tecnologia é o clássico Hello World, bastante eficaz para enter a estrutura básica de uma linguagem,
sendo assim, abaixo está um exemplo de Hellow World em C#:


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
  <h1>Fundamentos da Linguagem</h1>
</div> 


<h1>Tipos e Variáveis</h1>

Os tipos se manifestam de duas formas no C#: value types e reference types. Variáveis de value types cotém direteamente seus valores.
Variáveis de reference types armazenam referências a esses valores, sendo posteriormente chamadas de objetos. Com reference types é possível
que duas variáveis referenciem o mesmo objeto e que as operações em uma variável afetem o objeto referenciado pela outra. Com o value types,
cada variável tem sua própria cópia do dado, e não é possível que as operações em uma afetem a outra (exceto para variáveis de parâmetro ref e out).

<br>

Um identificador é um nome de variável. Um identificador é uma sequência de caracteres Unicode sem nenhum espaço em branco. Um
identificador pode ser uma palavra reservada C#, se for prefixado por @. Usar uma palavra reservada como identificador pode ser útil ao
interagir com outros idiomas.

<br>

Os tipos de valor do C# são divididos em simple types, enum types, structure types, nullable value types, e tuple value types. Os tipos
de referência do C# são divididos em tipos de classe, tipos de interface, tipos de array e delegate types.

<h1>Value Types</h1>


<h2>Simple Types</h2>

Os Simple Types são definidos por três tipos próprios:

<br>

<h3>Tipos numéricos integrais</h3>

Os tipos numéricos integrais representam números inteiros. Todos os tipos numéricos integrais são tipos de valor. Eles também são tipos
simples e podem ser inicializados com literais. Todos os tipos numéricos integrais suportam operadores aritméticos, lógicos bit a bit,
de comparação e de igualdade.

### O C# suporta os seguintes tipos integrais predefinidos:

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


<h3>Tipos numéricos de ponto flutuante (referência C #)</h3>

Os tipos numéricos de ponto flutuante representam números reais. Todos os tipos numéricos de ponto flutuante são tipos de valor. Eles também
são tipos simples e podem ser inicializados com literais. Todos os tipos numéricos de ponto flutuante oferecem suporte a operadores aritméticos,
de comparação e de igualdade.

### O C# oferece suporte aos seguintes tipos de ponto flutuante predefinidos:

|  C# Tipo/Palavra-chave  |         Alcance Aproxiamdo         |   Precision   |   Tamanho   |     .NET type      |
| ----------------------- | ---------------------------------- | ------------- | ----------- | ------------------ | 
| float	                  | ±1.5 x 10(−45) to ±3.4 x 10(38)	   | ~6-9 digits   |   4 bytes   | System.Singlesbyte |
| double	                | ±5.0 × 10(−324) to ±1.7 × 10(308)  | ~15-17 digits |   8 bytes   | System.Double      |
| decimal	                | ±1.0 x 10(-28) to ±7.9228 x 10(28) | 28-29 digits  |   16 bytes  | System.Decimal     |


<h3>bool (referência C #)</h3>

A palavra-chave bool type é um alias para o tipo de estrutura .NET System.Boolean que representa um valor booleano, que pode ser true ou false.

<br>

Para realizar operações lógicas com valores do tipo booleano, use operadores lógicos booleanos. O tipo bool é o tipo de resultado dos operadores
de comparação e igualdade. Uma expressão booleana pode ser uma expressão condicional de controle nas instruções if, do, while e for e no operador
condicional:.

<br>

O valor padrão do tipo bool é falso.

    bool check = true;
    Console.WriteLine(check ? "Checked" : "Not checked");  // output: Checked
    
    Console.WriteLine(false ? "Checked" : "Not checked");  // output: Not checked


<h3>char (referência C #)</h3>

A palavra-chave char type é um alias para o tipo de estrutura .NET System.Char que representa um caractere Unicode UTF-16.


<div align="center">
  |  Tipo  |      Alcance	    |   Tamanho   |  .NET type  |
  | ------ | ---------------- | ----------- | ----------- |
  |  char  | U+0000 to U+FFFF	|   16 bit    | System.Char |
</div>


O valor padrão de um char é \0, que equivale a U+0000.

<br>

O tipo char oferece suporte a operadores de comparação, igualdade, incremento e decremento. Além disso, para operandos char, os operadores
lógicos aritméticos e bit a bit executam uma operação nos códigos de caracteres correspondentes e produzem o resultado do tipo int.

<br>

O tipo string representa texto através de uma sequência de valores char.


<h2>Enumeration types</h2>

Um tipo de enumeração (ou tipo enum) é um tipo de valor definido por um conjunto de constantes nomeadas do tipo numérico integral subjacente.
Para definir um tipo de enumeração, use a palavra-chave enum e especifique os nomes dos membros de enum:

    enum Season
    {
        Spring,
        Summer,
        Autumn,
        Winter
    }

Por padrão, os valores constantes associados de membros enum são do tipo int; eles começam com zero e aumentam em um seguindo a ordem do texto
de definição. Você pode especificar explicitamente qualquer outro tipo numérico integral como um tipo subjacente de um tipo de enumeração.
Você também pode especificar explicitamente os valores constantes associados, como mostra o exemplo a seguir:

    enum ErrorCode : ushort
    {
        None = 0,
        Unknown = 1,
        ConnectionLost = 100,
        OutlierReading = 200
    }


<h2>Structure types</h2>

Um tipo de estrutura (ou tipo de estrutura) é um tipo de valor que pode encapsular dados e funcionalidades relacionadas. Você usa a palavra-chave
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
das variáveis são copiados na atribuição, passando um argumento para um método e retornando um resultado do método. No caso de uma variável do
tipo de estrutura, uma instância do tipo é copiada. Para obter mais informações, consulte Tipos de valor.


<h2>Nullable value types</h2>

Um tipo de valor nullable T? representa todos os valores de seu tipo de valor subjacente T e um valor nulo adicional. Por exemplo, você pode
atribuir qualquer um dos três valores a seguir a um bool? variável: verdadeiro, falso ou nulo. Um tipo de valor subjacente T não pode ser um
tipo de valor nullable em si.

<br>

Qualquer tipo de valor nullable é uma instância da estrutura genérica System.Nullable<T>. Você pode se referir a um tipo de valor nullable com um
tipo subjacente T em qualquer uma das seguintes formas intercambiáveis: <strong>nullable<T></strong> ou <strong>T ?.</strong>

<br>

Normalmente, você usa um tipo de valor anulável quando precisa representar o valor indefinido de um tipo de valor subjacente. Por exemplo, uma
variável booleana ou booleana só pode ser verdadeira ou falsa. No entanto, em alguns aplicativos, um valor de variável pode ser indefinido ou
ausente. Por exemplo, um campo de banco de dados pode conter verdadeiro ou falso ou pode não conter nenhum valor, ou seja, NULL. Você pode usar
o <strong>bool?</strong> digite nesse cenário.

<h3>Declaração e atribuição</h3>

Como um tipo de valor é implicitamente conversível no tipo de valor anulável correspondente, você pode atribuir um valor a uma variável de um
tipo de valor anulável como faria para seu tipo de valor subjacente. Você também pode atribuir o valor nulo. Por exemplo:

    double? pi = 3.14;
    char? letter = 'a';
    
    int m2 = 10;
    int? m = m2;
    
    bool? flag = null;
    
    // An array of a nullable value type:
    int?[] arr = new int?[10];

O valor padrão de um tipo de valor anulável representa nulo, ou seja, é uma instância cuja propriedade <strong>Nullable<T></strong> .HasValue
retorna falso.


<h2>Tuple types</h2>

Disponível no C # 7.0 e posterior, o recurso de tuplas fornece sintaxe concisa para agrupar vários elementos de dados em uma estrutura de
dados leve. O exemplo a seguir mostra como você pode declarar uma variável de tupla, inicializá-la e acessar seus membros de dados:

    (double, int) t1 = (4.5, 3);
    Console.WriteLine($"Tuple with elements {t1.Item1} and {t1.Item2}.");
    // Output:
    // Tuple with elements 4.5 and 3.
    
    (double Sum, int Count) t2 = (4.5, 3);
    Console.WriteLine($"Sum of {t2.Count} elements is {t2.Sum}.");
    // Output:
    // Sum of 3 elements is 4.5.



<h1>Reference types</h1>

Existem dois tipos de Tipos em C#: tipos de referência e tipos de valor. Variáveis de tipos de referência armazenam referências a seus dados
(objetos), enquanto variáveis de tipos de valor contêm diretamente seus dados. Com tipos de referência, duas variáveis podem fazer referência
ao mesmo objeto; portanto, as operações em uma variável podem afetar o objeto referenciado pela outra variável. Com tipos de valor, cada
variável tem sua própria cópia dos dados, e não é possível que as operações em uma variável afetem a outra (exceto no caso de variáveis 
de parâmetro in, ref e out; ver modificador de parâmetro in, ref e out).


<h2>Class Types</h2>

As classes são declaradas usando a palavra-chave class, conforme mostrado no exemplo a seguir:

    class TestClass
    {
        // Methods, properties, fields, events, delegates
        // and nested classes go here.
    }

<h2>Remarks</h2>

Somente herança única é permitida em C #. Em outras palavras, uma classe pode herdar a implementação de apenas uma classe base. No entanto,
uma classe pode implementar mais de uma interface. A tabela a seguir mostra exemplos de herança de classe e implementação de interface:


|           Inheritance	            |                    Example                     |
| --------------------------------- | -----------------------------------------------|
| None	                            | class ClassA { }                               |
| Single	                        | class DerivedClass : BaseClass { }             |
| None, implements two interfaces	| class ImplClass : IFace1, IFace2 { }           |
| Single, implements one interface	| class ImplDerivedClass : BaseClass, IFace1 { } |


As classes que você declara diretamente em um namespace, não aninhadas em outras classes, podem ser públicas ou internas. As classes são
internas por padrão.

<br>

Os membros da classe, incluindo classes aninhadas, podem ser public, protected internal, protected, internal, private, or private protected.
Os membros são privados por padrão.

<br>

Mas a frente veremos mais sobre os Access Modifiers e Classes.


<h2>interface</h2>


Uma interface define um contrato. Qualquer classe ou estrutura que implemente esse contrato deve fornecer uma implementação dos membros definidos
na interface. A partir do C # 8.0, uma interface pode definir uma implementação padrão para os membros. Ele também pode definir membros estáticos
para fornecer uma única implementação para funcionalidade comum.

No exemplo a seguir, a classe <strong>ImplementationClass<strong> deve implementar um método denominado <strong>SampleMethod</strong> que não
possui parâmetros e retorna void:

    interface ISampleInterface
    {
        void SampleMethod();
    }
    
    class ImplementationClass : ISampleInterface
    {
        // Explicit interface member implementation:
        void ISampleInterface.SampleMethod()
        {
            // Method implementation.
        }
    
        static void Main()
        {
            // Declare an interface instance.
            ISampleInterface obj = new ImplementationClass();
    
            // Call the member.
            obj.SampleMethod();
        }
    }

Uma interface pode ser membro de um namespace ou classe. Uma declaração de interface pode conter declarações (assinaturas sem qualquer implementação)
dos seguintes membros:

<ul>
  <li>Methods</li>
  <li>Properties</li>
  <li>Indexers</li>
  <li>Events</li>
</ul>


<h2>Arrays</h2>


Você pode armazenar várias variáveis do mesmo tipo em uma estrutura de dados de matriz. Você declara uma matriz especificando o tipo de seus elementos.
Se quiser que a matriz armazene elementos de qualquer tipo, você pode especificar o objeto como seu tipo. No sistema de tipo unificado do C #, todos os
tipos, predefinidos e definidos pelo usuário, tipos de referência e tipos de valor, herdam direta ou indiretamente do objeto.

> type[] arrayName;

<br>

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
    Você pode usar matrizes de iteração   foreach em C #. Uma vez que as matrizes de dimensão única também implementam IList <T> e IEnumerable <T>.
  </li>
</ul>

<h2>Delegate</h2>

A declaração de um tipo de delegate é semelhante a uma assinatura de método. Ele tem um valor de retorno e qualquer número de parâmetros
de qualquer tipo:

> public delegate void MessageDelegate(string message);
> public delegate int AnotherDelegate(MyType m, long num);

Um delegate é um tipo de referência que pode ser usado para encapsular um método nomeado ou anônimo. Os delegate são semelhantes aos
ponteiros de função em C ++; no entanto, os delegados são protegidos contra tipos e seguros. Para aplicações de delegate, consulte
Delegate e Delegtes Genéricos. Os delegates são a base dos eventos. Um delegate pode ser instanciado associando-o a um método
nomeado ou anônimo.


<h1>Blocos de construção do programa</h1>


<h2>Membros</h2>

Os membros de uma classe são membros estáticos ou membros de instância. Membros estáticos pertencem a classes e membros de instância
pertencem a objetos (instâncias de classes).

<br>

A lista a seguir fornece uma visão geral dos tipos de membros que uma classe pode conter.

<ul>
  <li><strong>Constants:</strong> Valores constantes associados à classe</li>
  <li><strong>Fields:</strong> Variáveis que estão associadas à classe</li>
  <li><strong>Methods:</strong> Ações que podem ser realizadas pela classe</li>
  <li><strong>Properties:</strong> Ações associadas à leitura e gravação de propriedades nomeadas da classe</li>
  <li><strong>Indexers:</strong> Ações associadas a instâncias de indexação da classe como uma matriz</li>
  <li><strong>Events:</strong> Notificações que podem ser geradas pela classe</li>
  <li><strong>Operators:</strong> Operadores de conversão e expressão suportados pela classe</li>
  <li><strong>Constructors:</strong> Ações necessárias para inicializar instâncias da classe ou a própria classe</li>
  <li><strong>Finalizers:</strong> Ações realizadas antes de instâncias da classe são descartadas permanentemente</li>
  <li><strong>Types:</strong> Tipos aninhados declarados pela classe</li>
</ul>


<h2>Accessibility</h2>

Cada membro de uma classe tem uma acessibilidade associada, que controla as regiões do texto do programa que podem acessar o membro.
Existem seis formas de acessibilidade possíveis. Os modificadores de acesso são resumidos abaixo.

<ul>
  <li><strong>public:</strong> O acesso não é limitado.</li>
  <li><strong>private:</strong> O acesso é limitado a esta classe.</li>
  <li><strong>protected:</strong> O acesso é limitado a esta classe ou classes derivadas desta classe.</li>
  <li><strong>internal:</strong> O acesso é limitado ao assembly atual (.exe ou .dll).</li>
  <li><strong>protected internal:</strong> O acesso é limitado a esta classe, classes derivadas desta classe ou classes dentro do mesmo assembly.</li>
  <li><strong>private protected:</strong>O acesso é limitado a esta classe ou classes derivadas deste tipo dentro do mesmo assembly.</li>
</ul>

