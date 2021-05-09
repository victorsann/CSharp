
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/115932830-19b66200-a464-11eb-8578-5a9249c16268.png">
</div>  
<br>
<img src="https://img.shields.io/static/v1?label=CSHARP&message=Language&color=purple&style=for-the-badge&logo="/>


Desenvolvida e mantida pela Micrsoft, o C# é uma linguagem de programação moderna, orientada a objetos e de
tipagem forte. Por meio de suas feramentas o C# permite o desenvolvimento de diversos tipos de aplicações
seguras e robustas através do ecosistema do .NET. A linguagem é essencialmente utilizada na plataforma .NET e
usa sua máquina virtual(CLR) como meio para ser executada, além de ter disponível uma série de classes prontas
para antender aos requisitos definidos na criação de uma aplicação.<br>
O C# foi desenvolvido para suprir a necessidade que a Microsoft tinha de uma linguagem que atendesse a requisição
de ser multiplataforma, assim como o Java, linguagem que esteve presente nos ambentes Windows por um bom tempo.
Por um conflito judicial a empresa passou a não poder utilizar o Java em seus projetos, o que levou em fim a
criação do .NET e da liguagem C#.


<h2>Hellow World</h2>


Um dos primeiros passos ao iniciar em uma nova tecnologia é o clássico Hello World,
bastante eficaz para enter a estrutura básica de uma linguagem, sendo assim, abaixo 
está um exemplo de Hellow World em C#:


      using System;

      class Hello
      {
          static void Main()
          {
              Console.WriteLine("Hello, World");
          }
      }

O "Hello World" começa com a diretiva <strong>using</strong> que referencia o namespace 
<strong>System</strong>. O namespace nada mais é que uma definição de acesso hierárquico
aos recursos dos programas e bibliotecas C#, sendo o Console um dos vários recursos do 
sistema. A classe criada e chamada de Hello possui apenas o método Main() como seu recurso.
Sendo definido como static, fazendo com que o método não precise ser referenciado, ele 
assume a caracterítica de entry da classe Hello. Com a definição de acesso aos recursos do
System é possível usar a classe Console, que por sua vez possui o método WriteLine(). Esse
método é o responsável por fazer o binding da string "Hello, World" no Console.


<div align="center">
  <h1>Fundamentos da Linguagem</h1>
</div> 


<h1>Tipos e Variáveis</h1>

