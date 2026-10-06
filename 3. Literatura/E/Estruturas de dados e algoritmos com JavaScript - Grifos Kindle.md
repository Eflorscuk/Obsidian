---
tipo: grifos
obra: "Estruturas de dados e algoritmos com JavaScript: Escreva um código JavaScript complexo e eficaz usando a mais recente ECMAScript"
autor: "Loiane Groner"
fonte: Kindle
tema: []
tags:
  - kindle
  - grifos
Data: 2026-10-06
grifos: 33
notas: 3
---

# Estruturas de dados e algoritmos com JavaScript

> Conhecer as estruturas de dados e os algoritmos é muito importante. O primeiro motivo é o fato de as estruturas de dados e os algoritmos serem capazes de resolver os problemas mais comuns de modo eficiente.
— Posição 448

**Nota:** Em programação, "parse" (ou "parsing") se refere ao processo de analisar uma sequência de caracteres ou tokens para determinar sua estrutura sintática. O objetivo do parsing é transformar a entrada de texto em uma estrutura de dados que possa ser facilmente manipulada e compreendida pelo programa.O parsing é comumente usado em linguagens de programação, compiladores, interpretadores e análise de linguagens formais. Durante o processo de parsing, uma sequência de entrada é dividida em elementos significativos, como palavras-chave, símbolos, operadores e expressões, de acordo com a gramática da linguagem ou a regra de análise específica.Existem diferentes abordagens para realizar o parsing, como o uso de gramáticas formais, expressões regulares, análise sintática descendente (bottom-up) ou análise sintática ascendente (top-down). Cada abordagem possui suas próprias vantagens e é escolhida de acordo com a necessidade e complexidade do problema a ser resolvido.

> Seguindo a melhor prática, incluiremos qualquer código JavaScript no final da tag body. Desse modo, o navegador fará o parse do HTML, e ele será exibido antes de os scripts serem carregados. Com isso, a página terá um melhor desempenho.
— Posição 540

> Em JavaScript, os tipos disponíveis são: number (número), string, boolean (booleano), function (função) e object (objeto). Também temos undefined (indefinido) e null (nulo), junto com arrays, datas e expressões regulares.
— Posição 544

> • Um valor null quer dizer sem valor, e undefined significa uma variável que foi declarada, mas que ainda não recebeu nenhum valor.
— Posição 569

**Nota:** Importante sobre null e undefined

> O escopo se refere ao local em que podemos acessar a variável no algoritmo (também pode ser em uma função quando trabalhamos com escopos de função). As variáveis podem ser locais ou globais.
— Posição 587

> Talvez você ouça falar que variáveis globais em JavaScript são prejudiciais, e isso é verdade. Em geral, a qualidade do código-fonte JavaScript é avaliada de acordo com o número de variáveis e funções globais (um número elevado é ruim). Portanto, sempre que possível, procure evitar as variáveis globais.
— Posição 612

> De acordo com a especificação, há dois tipos de dados em JavaScript: • tipos de dados primitivos: null (nulo), undefined (indefinido), string, number (número), boolean (booleano) e symbol (símbolo); • tipos de dados derivados/objetos: objetos JavaScript, incluindo funções, arrays e expressões regulares.
— Posição 703

> Um aspecto muito importante em uma instrução switch é o uso das palavras reservadas case e break.
— Posição 861

> Em POO (Programação Orientada a Objetos), um objeto é uma instância de uma classe. Uma classe define as características do objeto.
— Posição 927

> Eis o modo como podemos declarar uma classe (construtor) que representa um livro: function Book(title, pages, isbn) {   this.title = title;   this.pages = pages;   this.isbn = isbn; }
— Posição 929

> var book = new Book('title', 'pag', 'isbn');
— Posição 935

> Um array é a estrutura de dados mais simples possível em memória.
— Posição 1652

> let daysOfWeek = new Array(); // {1} daysOfWeek = new Array(7); // {2} daysOfWeek = new Array('Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'); // {3}
— Posição 1676

> Contudo, usar a palavra reservada new não é
— Posição 1681

> considerada a melhor prática.
— Posição 1682

> Se quisermos criar um array em JavaScript, podemos atribuir colchetes vazios ([]), como neste exemplo: let daysOfWeek = [];
— Posição 1682

> length
— Posição 1687

> números da sequência de Fibonacci.
— Posição 1696

> Em JavaScript, um array é um objeto mutável.
— Posição 1726

> Podemos facilmente lhe acrescentar novos elementos. O objeto crescerá dinamicamente à medida que novos elementos forem adicionados. Em várias outras linguagens, por exemplo, em C e em Java, é preciso determinar o tamanho do array e, caso haja necessidade de adicionar mais elementos, um array totalmente novo deverá ser criado; não podemos simplesmente adicionar novos elementos ao array à medida que forem necessários.
— Posição 1726

> Podemos percorrer todos os elementos do array com um laço, começando pela última posição (o valor de length será o final do array), deslocando o elemento anterior (i-1) para a nova posição (i) e, por fim, fazendo a atribuição do novo valor desejado à primeira posição (índice 0).
— Posição 1738

> Os métodos push e pop permitem que um array emule uma estrutura de dados stack básica, que será o assunto do próximo capítulo.
— Posição 1762

> Para remover o valor do array, podemos também criar um método removeFirstPosition com a lógica descrita nesta seção. No entanto, para realmente remover o elemento do array, precisamos criar outro array e copiar todos os valores diferentes de undefined do array original para o novo array e atribuí-lo ao nosso array. Para isso, podemos também criar um método reIndex, assim:
— Posição 1776

> Os métodos shift e unshift permitem que um array emule uma estrutura de dados básica de fila (queue), que será o assunto do Capítulo 5, Filas e deques.
— Posição 1804

> Assim como em arrays e objetos JavaScript, o operador delete também pode ser usado para remover um elemento de um array, por exemplo, delete numbers[0]. No entanto, a posição 0 do array terá o valor undefined, ou seja, será o mesmo que executar numbers[0] = undefined, e teríamos de reindexar o array. Por esse motivo, devemos sempre usar os métodos splice, pop ou shift para
— Posição 1816

> remover elementos.
— Posição 1819

> O primeiro argumento do método é o índice a partir do qual queremos remover ou inserir elementos. O segundo argumento é a quantidade de elementos que queremos remover (nesse caso, não queremos remover nenhum, portanto passamos o valor 0 (zero)). Do terceiro argumento em diante, temos os valores que gostaríamos de inserir no array (os elementos 2, 3 e 4). Os valores de -3 a 12 serão novamente exibidos na saída.
— Posição 1823

**Nota:** Como funciona o splice

> Para exibir um array bidimensional no console do navegador, podemos usar também a instrução console.table(averageTemp). Com ela, teremos uma saída mais elegante para o usuário.
— Posição 1874

> Não importa quantas dimensões temos na estrutura de dados; precisamos percorrer cada dimensão com um laço a fim de acessar a célula. Podemos representar uma matriz 3 x 3 x 3 com um diagrama em forma de cubo, assim (Figura 3.5).
— Posição 1887

> negativeNumbers.concat(zero,
— Posição 1941

> Ser capaz de obter pares chave/valor será muito conveniente quando estivermos trabalhando com conjuntos, dicionários e mapas de hash (hash maps). Essa funcionalidade será bastante conveniente para nós em capítulos mais adiante neste livro.
— Posição 2060

> Esse código devolverá um número negativo se b for maior que a, um número positivo se a for maior que
— Posição 2136

> b e 0 (zero) se forem iguais. Isso significa que, se um valor negativo for devolvido, é sinal de que a é menor que b, o que será usado posteriormente pela função sort para organizar os elementos.
— Posição 2137

## Conexões
- [[Loiane Groner]]
- [[Grifos Kindle]]
