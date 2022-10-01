# Listagem de estudo para programação
Java e outras linguagens orientada a objetos
### Topicos que são necessários estudar
+ **[Algoritmos](https://educapes.capes.gov.br/bitstream/capes/560827/2/Apostila%20-%20Curso%20de%20L%C3%B3gica%20de%20Programa%C3%A7%C3%A3o.pdf)**
  + Tipos de dados
  + Variaveis, constantes e operadores
  + Estruturas de seleção (if, elseif, else, switch case)
  + Funções
  + Estruturas de repetição(while, for, etc.)
+ **[Orientação a objeto](https://www.caelum.com.br/apostila/apostila-java-orientacao-objetos.pdf)** 
 + Tipos (primitivos e não primitivos)
 + Classes
 + Package (Pacotes para organização da estrutura do seu projeto)
 + Atributos do objeto
 + Métodos (com e sem retorno **return**)
 + Instanciação e utilização dos métodos de uma classe
 + Referencia de objeto
 + **Modificadores de acesso**
   + Controle de acesso (private, public, protected)
   + Encapsulamento
   + Getters & Setters
   + Construtores
  + Polimorfismo, Herança e sobreescrita
  + Classes Abstratas e Interfaces
  + Controle de erros(exceptions, try catch)
+ **Inico de Estrutura de Dados**
 + **Arrays**
 + **Pilhas**
 + **Filas**
 + **Conjunto(Set)**
 + **Dicionarios(Map)**
 + Arvores
 + Grafos


> **A teoria sem a prática de nada vale, a prática sem a teoria é cega.**



### Ótimos sites para treinar logica de programação, algoritmos
+ [HackerRank](https://www.hackerrank.com/)
+ [LeetCode](https://leetcode.com/)

### Plataformas e escolas de estudo sobre programação
+ Udemy(https://www.udemy.com/)
+ [DIO(Digital Innovation One)](https://www.dio.me/)
+ [Rocketseat](https://www.rocketseat.com.br/)


### Melhorando sua lógica de programação
+ **Estudando por fora, nao foque somente uma única fonte de estudo(livros, apostilas, documentações, vídeos)**
+ **Crie pequenos projetos para firmar o que acabou de estudar**
 + **[Ideias de projetos](https://github.com/florinpop17/app-ideas)**

Um dos principais problemas de quem está começando com programação, é a forma de visualizar os problemas e tentamos resolve-los. Nesse estagio aqui é esperado que voce tenha a base da programação ja consolidada e esteja mais perdido de como utilizar o que acabou de estudar.

Quando nos deparamos com um problema para resolver, em um primeiro momento temos todas as informações consolidadas do problema, nessa fase é dificil tomarmos alguma decisão. E uma das formas para se resolver é dividindo o problema em varias etapas e assim chegamos na solução.

###### **Precisamos de uma aplicação que converta Celcius em Fahrenheit e vice-versa. **
Primeiro identificamos o problema, sabemos que precisamos converter Celcius em Fahrenheit e em um outro momento também vamos converter Fahrenheit em Celcius

Vamos pegar o problema maior e dividir ele em pequenos problemas.

> **Dividir para conquistar**

Veja um exemplo abaixo de como podemos começar a resolver o problema.

**Problema:** Crie um algoritmo que converta a temperatura em Grau Celsius para Grau Fahrenheit
Formula: Multiplicamos a temperatura em ºC por 1,8 e somamos 32 ao resultado.
1. Precisamos criar uma função que irá receber o valor que iremos converter em Fahrenheit
2. Criar uma variavel com o valor 1.8 que iremos utilizar para multiplicar com o valor
3. Multiplicar o 1.8 com o valor que recebemos na função e somar com 32
4. Agora temos o resultado da conversão.

```java
public Double converterCelciusEmFahrenheit(Double grauCelcius) {
    Double multiplicador = 1.8;
    return (grauCelcius * multiplicador) + 32;
}
```

**Problema:** Crie um algoritmo que converta a temperatura em Grau Fahrenheit para Grau Celsius
Formula: Subtraímos a temperatura em ºF por 32 e dividimos o resultado por 1,8.
1. Precisamos criar uma função que irá receber o valor que iremos converter em Grau Celcius
2. Criar uma variavel com o valor 1.8 que iremos utilizar para dividir com o valor subtraido por 32
3. Subtrair o valor que recebemos na função por 32 e dividir o resultado com a variavel que criamos acima.
4. Agora temos o resultado da conversão.

```java
public Double converterFahrenheitEmCelcius(Double grauFahrenheit) {
    Double divisor = 1.8;
    return (grauFahrenheit - 32) / divisor;
}
```

**Problema:** Crie um algoritmo que no primeiro parametro recebe um valor e em segundo parametro para qual unidade de medida deverá ser convertido
1. Precisamos criar uma função que irá receber o valor e o tipo de medida que iremos converter
2. Validar quais os tipos de unidade que iremos realizar as conversões (Celcius, Fahrenheit, etc...)
3. Caso o método receber **Celcius** na unidade, chamamos a função de conversão de Fahrenheit para Celcius que criamos acima **converterFahrenheitEmCelcius**, caso a unidade seja **Fahrenheit** chamamos **converterCelciusEmFahrenheit**
4. Caso na unidade venha algo diferente de Celcius ou Fahrenheit retornamos uma Exception dizendo que a unidade é invalida.


```java
public Double converterGrauEmAlgumaUnidade(Double grau, String unidade) {
    if(unidade.equals("Celcius")) {
        return converterFahrenheitEmCelcius(grau);
    } else if(unidade.equals("Fahrenheit")) {
        return converterCelciusEmFahrenheit(grau);
    } else {
        throw new RuntimeException("Unidade de medida inválida");
    }
}
```
Isso é uma forma de chegar a uma conclusão, nao necessariamente essa é a melhor forma. Mas resolve o problema. Melhoramos isso com o tempo e com refatorações.

> **Nós somos aquilo que fazemos repetidamente. Excelência, então, não é um modo de agir, mas um hábito.**

####  Estruturando o seu algoritmo para chegar na solução
Um algoritmo é uma sequencia de instruções que visa obter uma solução para determinado problema.

O matemático **G. Polya**  apresenta fases para o processo de resolução
de problemas.
- **Fase 1.** Entender o problema
- **Fase 2**. Construir um plano para solucionar o problema. *(Testes de mesa e Diagramas)*
- **Fase 3.** Colocar o plano em funcionamento. *(Inicio de desenvolvimento)*
- **Fase 4**. Avaliar a solução quanto à precisão e quanto ao seu potencial como ferramenta para solucionar outros problemas. (Refatoração do código para melhorar desempenho e avaliar se seu algoritmo resolve outro problema parecido)

###### Representação e documentação
+ **Descrição narrativa: ** consiste em analisar o enunciado do problema e
escrever, utilizando linguagem natural, os passos a serem seguidos para sua
resolução.
 + A língua natural abre espaço para várias interpretações, dificultando a transcrição desse algoritmo para programa. Mas é um ponto inicial forte para se ter ideia de qual é o problema e como vamos resolver o mesmo.
+ **Fluxograma:** consiste em analisar o enunciado do problema e escrever,
utilizando símbolos gráficos, os passos a serem seguidos para sua
resolução.
 +  O entendimento de elementos gráficos é mais simples que o entendimento de textos.
 + Os fluxogramas devem ser entendidos e o algoritmo resultante não é detalhado. Isso dificulta sua transcrição para um programa
+ **C4Model:** é um conjunto de diagramas hierárquicos baseado em camadas que pode ser usado para descrever a arquitetura de um software em diferentes níveis de abstração e conforme aumenta a profundidade, maior será o nível de detalhes.
 + **Nível 1: Contexto** - O primeiro nível tem o objetivo de exibir o quadro geral, possibilitando visualizar as fronteiras e os relacionamentos com cada item externo, geralmente para outros serviços 
 + **Nível 2: Container** - A camada container expõe a arquitetura de forma simplificada, exibindo as tecnologias usadas e como a comunicação acontece.
 + **Nível 3: Componentes** - com foco nas funcionalidades, apresentando suas responsabilidades e detalhes de tecnologia
 + **Nível 4: Código** - Objetivo é apresentar de forma simples como um componente deve ser implementado, para isso é possível usar diagramas de classe UML, diagrama de entidade e relacionamento

[![Nivel 1 - Contexto](https://static.structurizr.com/workspace/76748/diagrams/SystemContext.png "A")](https://static.structurizr.com/workspace/76748/diagrams/SystemContext.png "A")
> Nivel 1 - Contexto: Aqui temos uma visão mais simplificada de como um sistema funciona e com quais outros sistemas ele se comunica

[![Nivel 2 Container](https://static.structurizr.com/workspace/76748/diagrams/Containers.png "Nivel 2 Container")](https://static.structurizr.com/workspace/76748/diagrams/Containers.png "Nivel 2 Container")
> Nivel 2 Container: Aqui vemos uma parte mais técnica mas simples de como as aplicações estao se comunicando

[![Nivel 3 Componentes](https://static.structurizr.com/workspace/76748/diagrams/Components.png "Nivel 3 Componentes")](https://static.structurizr.com/workspace/76748/diagrams/Components.png "Nivel 3 Componentes")
> Nivel 3 Componentes: Aqui vemos mais baixo nivel de como nosso serviço funciona, quais as chamadas e componentes que estão sendo utilizados

[![Nivel 4 Codigo](https://c4model.com/img/class-diagram.png "Nivel 4 Codigo")](https://c4model.com/img/class-diagram.png "Nivel 4 Codigo")
> Nivel 4 Código: Aqui de fato pensamos e definimos o código e como resolvemos o problema. Essa é a parte mais baixa da modelagem desse diagrama. Neste nivel aqui podemos considerar que colocamos a Fase 1 e a Fase 2 que vimos acima sobre o processo de resolução de problemas.




> References
 > https://www.alura.com.br/artigos/estruturas-de-dados-introducao
 > 
 >https://www.caelum.com.br/apostila/apostila-java-orientacao-objetos.pdf
 >
 >http://www.waltenomartins.com.br/algdados_apostila_ord.pdf
 >
 > https://www.alura.com.br/artigos/estruturas-de-dados-introducao
 > 
 > http://wiki.icmc.usp.br/images/8/88/Aula2P2_-_Resolucao_de_Problemas_e_desenvolvimento_de_Algoritmos_2011101.pdf
 > 
 > https://c4model.com/
 > 
 > https://medium.com/pravaler-digital-team/c4-model-9b6e56705496
 > 

