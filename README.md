
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/115932830-19b66200-a464-11eb-8578-5a9249c16268.png">
</div>  
<br>
<img src="https://img.shields.io/static/v1?label=CSHARP&message=Language&color=purple&style=for-the-badge&logo="/>

<h5>
     Desenvolvida e mantida pela Micrsoft, o C# é uma linguagem de programação moderna, orientada a objetos
  e de tipagem forte. Por meio de suas feramentas o C# permite o desenvolvimento de diversos tipos de aplicações
  seguras e robustas através do ecosistema do .NET. A linguagem é essencialmente utilizada na plataforma .NET e
  usa sua máquina virtual(CLR) como meio para ser executada, além de ter disponível uma série de classes prontas
  para antender aos requisitos definidos na criação de uma aplicação.<br>
  O C# foi desenvolvido para suprir a necessidade que a Microsoft tinha de uma linguagem que atendesse a requisição
  de ser multiplataforma, assim como o Java, linguagem que esteve presente nos ambentes Windows por um bom tempo.
  Por um conflito judicial a empresa passou a não poder utilizar o Java em seus projetos, o que levou em fim a
  criação do .NET e da liguagem C#.
</h5>

<h2>Hellow World</h2>

<h5>
  Um dos primeiros passos aos iniciar em uma nova tecnologia é o clássico Hello World,
  bastante eficaz para enter a estrutura básica de uma linguagem, sendo assim, abaixo 
  está um exemplo de Hellow World em C#:
</h5>

       using System;
       using System.Collections.Generic;
       using System.Linq;
       using System.Text;
       using System.Threading.Tasks;

       namespace HelloWorld
       {
           class Program
           {
               static void Main(string[] args)
               {
                  Console.WriteLine("Hello World");
                  Console.ReadLine();
               }
           }
       }
 

<h3>Modules</h3>
     
<h5>
  Os módulos ou pacotes padrões são subdivisões da linguagem, arquitetura definida graças ao tamanho do C# em
  termos de conteúdo. Cada funcionalidade da linguagem que será utilizada dentro do projeto deve ter seu módulo
  definido na parte inicial do programa, não sendo necessário escreve-los manualmente, já que o .NET possui toda
  uma estrutura de pré definição das características do projeto em sua criação, mas sendo possível caso necessário.
</h5>

<h3>
  Sintaxe de Uso de Um Módulo using System
</h3>
 
<h5>  
  A diretiva 'using' define a intenção que o programa tem de, em determinado momento, fazer uso do módulo que será
  declarado em seguida, sendo nesse caso o System. O módulo System define que o projeto pretende fazer uso das
  funcionalidades do sistema operacional do usuário, entre outra coisas.
</h5>

<h3>Namespace</h3>

<h5>
  O Namespace tem a função de identificar determinada classe como única na solução, evitando conflitos sintáticos.
  Além disso, agrupa as funcionalidades comuns a essa classe e permite que ela seja utilizada em outra parte da
  aplicação quando chamada. Exemplo:
<h5>

><h4>System.Console.WriteLine("Hello World!")<h4>

<h5>
  System é um namespace e Console é uma classe nesse Namespace. Caso seja preciso chamar essa classe, a palavra-chave
  using pode ser usada para que o nome completo não seja necessário, exatamente como na definição de uso
  de um módulo.
</h5>
   
<h3>Class</h3>
  
<h5>
     A classe é aonde se define o comportamento da própria classe. Sendo declarada através da palavra chave "class",
  pode ser precedida de um identificador de nível de acessibilidade, podendo ser instanciada por qualquer um caso seja
  do tipo public, identificador padrão. Além disso, as classes também possuem um Namespace único que as identifica, sendo
  este chamado em caso de uso dessa classe em outra parte da aplicação. A partir desse ponto, tudo o que for contido por
  uma classe é chamado de membro de classe, e faz parte do que será executado junto com o programa.
</h5>

<h3>MainFunction</h3>

<h5>
  A MainFunction, função principal, método ou rotina principal, é uma função de execução padrão, ou seja, tudo o que for
  definido como seu conteúdo, será executado ao iniciar o programa.
</h5>
