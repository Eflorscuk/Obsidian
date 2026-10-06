---
tipo: grifos
obra: "Princípios de Orientação a Objetos em JavaScript"
autor: "Nicholas C. Zakas"
fonte: Kindle
tema: []
tags:
  - kindle
  - grifos
Data: 2026-10-06
grifos: 250
notas: 4
---

# Princípios de Orientação a Objetos em JavaScript

> Encapsulamento
— Posição 145

> objeto. • Agregação – um
— Posição 146

> Herança
— Posição 148

> Polimorfismo
— Posição 150

> Um
— Posição 154

> olhar
— Posição 154

> mais
— Posição 154

> profundo
— Posição 154

> na linguagem, no entanto, revela a existência de objetos por meio do uso da notação de ponto (.).
— Posição 154

> jamais irá precisar criar uma definição de classe,
— Posição 156

> Podemos simplesmente começar a escrever código sem planejar as classes de que precisaremos com antecedência. Você precisa de um objeto com campos específicos? Simplesmente crie um objeto ad hoc no local desejado. Você se esqueceu de adicionar um método a esse objeto? Sem problemas – basta adicionar depois.
— Posição 162

> Em vez de definir as classes desde o início,
— Posição 198

> com o JavaScript, você pode simplesmente escrever código e criar as estruturas de dados à medida que precisar delas.
— Posição 198

> JavaScript é como começar com uma folha em branco: você pode organizar tudo do jeito que quiser.
— Posição 201

> Para facilitar a transição a partir de linguagens orientadas a objetos tradicionais, em JavaScript, os objetos constituem a parte central da linguagem.
— Posição 205

> Os tipos primitivos são armazenados como tipos de dados simples. Os tipos de referência são armazenados como objetos e, na realidade, são apenas referências a posições de memória.
— Posição 215

> Enquanto outras linguagens de programação distinguem tipos primitivos de tipos de referência ao armazenar os tipos primitivos na pilha e os tipos de referência no heap, o JavaScript não utiliza, de modo algum, esse conceito: ele controla as variáveis de um escopo em particular usando um objeto variável.
— Posição 218

> Valores primitivos são armazenados diretamente no objeto variável, enquanto os valores de referência são criados como ponteiros no objeto variável.
— Posição 220

> Todos os tipos primitivos têm representações literais de seus valores. Os literais representam valores que não são armazenados em uma variável, por exemplo, um nome ou um preço fixo no código.
— Posição 241

> Em JavaScript, assim como em muitas outras linguagens, as variáveis que armazenam um primitivo contêm diretamente o valor primitivo
— Posição 255

> Object) para esse trecho de código.
— Posição 266

> A melhor maneira de identificar tipos primitivos é por meio do operador typeof
— Posição 280

> Você não seria o primeiro desenvolvedor a se confundir com o resultado desta linha de código: console.log(typeof null); // "object" Ao executar typeof null, o resultado é "object". Mas por que é um objeto
— Posição 293

> se o tipo é null? (De fato, isso foi reconhecido como um erro pelo TC39, que é o comitê que faz o design e mantém o JavaScript. Você poderia argumentar que null é uma referência a um objeto vazio, fazendo com que object seja um valor de retorno correto, porém ainda assim é confuso).
— Posição 296

> A melhor maneira de determinar
— Posição 299

> se um valor é null é compará-lo diretamente com null, desta maneira: console.log(value \=\=\= null); // true ou false
— Posição 300

> Os tipos null
— Posição 318

> e undefined não contêm métodos).
— Posição 318

> Os tipos de referência representam objetos em JavaScript e são o
— Posição 333

> recurso encontrado na linguagem que mais se assemelha às classes. Valores de referência são instâncias de tipos de referência e são sinônimos de objetos (o restante deste capítulo chama os valores de referência simplesmente de objetos).
— Posição 334

> Um objeto é uma lista não ordenada de propriedades constituídas de um nome
— Posição 336

> Quando o valor de uma propriedade for uma função, ela será chamada de método
— Posição 336

> As funções propriamente ditas, na verdade, são valores de referência em JavaScript, de modo que há pouca diferença entre uma propriedade que contém um array e uma que contém uma função, exceto pelo fato de que a função
— Posição 337

> pode ser executada.
— Posição 339

> Por convenção, os nomes dos construtores em JavaScript iniciam com uma letra maiúscula para distingui-los de funções que não são construtoras.
— Posição 346

> Os tipos de referência não armazenam o objeto diretamente na variável à qual ele foi atribuído, portanto a variável object nesse exemplo não contém a instância do objeto. Em vez disso, ela armazena um ponteiro (ou uma referência) para a posição de memória em que esse objeto está.
— Posição 349

> Quando um objeto for atribuído a uma variável, você estará, na verdade, atribuindo-lhe um ponteiro. Isso significa que se você atribuir uma variável a outra, cada variável terá uma cópia dessa
— Posição 353

> referência, e ambos continuarão referenciando o mesmo objeto na memória. Por exemplo: var object1 = new Object(); var object2 = object1;
— Posição 354

**Nota:** A comparação de objetos com o operador \=\= ou \=\=\= compara referências, não os valores dos objetos.

> Nesse caso, object1 é criado e usado antes de finalmente ser definido como null. Quando não houver mais referências a um objeto na memória, o coletor de lixo poderá usar essa área de memória para algo diferente. (Remover a referência aos objetos é especialmente importante em aplicações grandes, que utilizam
— Posição 370

> (Remover a referência aos objetos é especialmente importante em aplicações grandes, que utilizam milhares de objetos.)
— Posição 372

> milhares de objetos.)
— Posição 373

> Esse exemplo demonstra uma particularidade única do JavaScript: você pode modificar objetos quando quiser, mesmo que eles não tenham sido definidos
— Posição 384

> antes. Também há maneiras de evitar essas modificações, como você verá mais adiante neste livro.
— Posição 385

> Os tipos próprios são: • Array: uma lista ordenada de valores indexados numericamente • Date: uma data e uma hora • Error: um erro de execução (há vários subtipos mais específicos de erros) • Function: uma função • Object: um objeto genérico • RegExp: uma expressão regular
— Posição 391

> var items = new Array(); var now = new Date(); var error = new Error("Something bad happened."); var func = new Function("console.log('Hi');"); var object = new Object(); var re = new RegExp("\\\\d+");
— Posição 400

> Esse código define a função reflect(), que retorna qualquer valor passado a ela. Mesmo no caso dessa função simples, a forma literal é mais fácil de escrever e de ser entendida se comparada ao código que utiliza o construtor. Além disso, não há maneira eficiente de depurar funções criadas com o método do construtor: essas funções não são reconhecidas pelos debuggers de JavaScript e, desse modo, atuam como caixas pretas em sua aplicação.
— Posição 448

> Acesso a propriedades Propriedades são pares de nomes/valores armazenados em um objeto. A notação de ponto é a forma mais comum de acessar propriedades em JavaScript (e em muitas linguagens orientadas a objetos), mas você também pode acessar propriedades em objetos JavaScript usando a notação de colchetes com uma string. Por exemplo, você pode escrever este código, que usa a notação de ponto: var array = []; array.push(12345); Com a notação de colchetes, o nome do método passa a ser incluído em uma string dentro de colchetes, como neste exemplo: var array = []; array["push"](12345); Essa sintaxe é muito útil quando você precisa decidir dinamicamente qual propriedade deverá ser acessada. Por exemplo, no caso a seguir, a notação de colchetes permite usar uma variável em vez de usar uma string literal para especificar a propriedade a ser acessada: var array = []; var method = "push"; array[method](12345);
— Posição 467

> Propriedades são pares de nomes/valores
— Posição 467

> valores armazenados em um objeto. A notação de ponto é a forma mais comum de acessar propriedades em JavaScript (e em muitas linguagens orientadas a objetos), mas você também pode acessar propriedades em objetos JavaScript usando a notação de colchetes com uma string.
— Posição 468

> var array = []; array.push(12345);
— Posição 471

> var array = []; array["push"](12345);
— Posição 473

> Uma função é o tipo de referência mais fácil de ser identificado porque,
— Posição 486

> Para identificar tipos de referência mais facilmente, o operador instanceof do JavaScript pode ser utilizado.
— Posição 494

> Embora instanceof possa identificar arrays, há uma exceção que afeta os desenvolvedores web: valores em JavaScript podem ser passados entre frames na mesma página web. Isso se torna um problema somente quando você tenta identificar o tipo de um valor de referência, pois cada página web tem o seu próprio contexto global – sua própria versão de Object, Array e de todos os demais tipos próprios. Como resultado, ao passar um array de um frame para outro, instanceof não funciona porque o array é uma instância de Array de um frame diferente. Para corrigir esse problema, o ECMAScript 5 introduziu Array.isArray(), que identifica definitivamente o valor como uma instância de Array, sem se importar com a origem do valor. Esse método deve retornar true quando receber um valor que seja um array nativo de qualquer contexto. Se o seu ambiente de desenvolvimento suporta ECMAScript 5, Array.isArray() será a melhor maneira de identificar arrays: var items = []; console.log(Array.isArray(items)); // true
— Posição 527

> Para corrigir esse problema, o ECMAScript 5 introduziu Array.isArray()
— Posição 533

> Array.isArray(items));
— Posição 539

> Os tipos wrapper primitivos são tipos de referência criados
— Posição 546

**Nota:** Embrulho, invólucro

> autoboxing).
— Posição 562

> Embora não tenha classes, o JavaScript tem tipos. Cada variável ou porção de dado é associado a um tipo primitivo ou de referência específico.
— Posição 613

> Você pode usar typeof para identificar tipos primitivos com exceção de null, que deve ser comparado diretamente com o valor especial null.
— Posição 616

> Use o operador instanceof com um construtor para identificar objetos de outros tipos de referência.
— Posição 622

> A característica determinante de uma função – o que a distingue de outros objetos – é a presença de uma propriedade interna chamada \[\[Call\]\].
— Posição 630

> propriedade interna chamada
— Posição 631

> \[\[Call\]\].
— Posição 631

> A propriedade \[\[Call\]\] é exclusiva das funções e indica que o objeto pode ser executado.
— Posição 634

> typeof é definido pela ECMAScript para retornar "function" para qualquer objeto que tenha a propriedade \[\[Call\]\].
— Posição 635

> Como as funções são objetos, elas se comportam de modo diferente das funções em outras linguagens, e entender esse comportamento é fundamental
— Posição 641

> para ter uma boa compreensão de JavaScript.
— Posição 642

> de JavaScript.
— Posição 642

> A primeira é a declaração de função,
— Posição 643

> expressão de função,
— Posição 649

> duas formas são quase idênticas,
— Posição 655

> As declarações de função são “içadas” (hoisted) para o topo do contexto (seja na função em que a declaração é feita ou no escopo global)
— Posição 658

> quando o
— Posição 659

> código é executado.
— Posição 659

> O hoisting de funções ocorre somente em declarações de funções porque o nome da função é previamente conhecido.
— Posição 671

> Você pode atribuí-las a variáveis, adicioná-las a objetos, passá-las para outras funções como argumentos e retorná-las a partir de outras funções.
— Posição 681

> Quando você tem em mente que funções são objetos, muitos comportamentos começam a fazer sentido.
— Posição 702

> O método sort() de
— Posição 703

> arrays em JavaScript aceita uma função de comparação como parâmetro opcional. A função de comparação é chamada sempre que
— Posição 703

> sort() converte todos os itens de um array em uma string e, em seguida, efetua a comparação. Isso
— Posição 707

> um array de números de forma precisa sem especificar uma função de comparação.
— Posição 708

> Note que não há nome para a função; ela existe somente como uma referência que é passada para outra função (tornando-a uma função anônima).
— Posição 719

> Isso ocorre porque a comparação-padrão converte todos os valores para string antes de compará-los.
— Posição 723

**Nota:** sort()

> Outro aspecto único das funções JavaScript é que você pode passar qualquer número de parâmetros para qualquer função sem causar erros.
— Posição 725

> Isso ocorre porque os parâmetros de funções são armazenados em uma estrutura semelhante a arrays chamada arguments.
— Posição 726

> em uma estrutura semelhante a arrays chamada arguments.
— Posição 726

> objeto arguments está automaticamente disponível em qualquer função.
— Posição 730

> O objeto arguments não é uma instância de Array e, portanto, não tem os mesmos métodos de um array. Array.isArray(arguments) sempre retornará false.
— Posição 733

> Lembre-se de que uma função é apenas um objeto, portanto ela pode ter propriedades.
— Posição 737

> A propriedade length indica a aridade (arity) da função, ou seja, o número de parâmetros que ela espera. Conhecer a aridade das funções é importante em JavaScript porque as funções não gerarão um erro se você lhes passar parâmetros a mais ou a menos.
— Posição 738

> Conhecer a aridade das funções é importante em JavaScript porque as funções não gerarão um erro se você lhes passar parâmetros a mais ou a menos.
— Posição 739

> reflect = function() {     return arguments[0] };
— Posição 749

> propriedade length é igual a 1 porque há somente um parâmetro nomeado. A função reflect() então é redefinida sem parâmetros nomeados; ela retorna arguments[0],
— Posição 756

> Em algumas ocasiões, porém, usar arguments é mais eficiente do que utilizar parâmetros nomeados.
— Posição 764

> Não é possível usar parâmetros nomeados porque não sabemos quantos serão necessários, portanto, nesse caso, usar arguments é a melhor opção:
— Posição 766

**Nota:** Hoje da para utilizar rest ...

> function sum() {     var result = 0,         i = 0,         len = arguments.length;     while (i < len) {         result += arguments[i];         i++;     }
— Posição 768

> A maioria das linguagens orientadas a objetos suporta sobrecarga de função, que é a possibilidade de uma função ter diversas assinaturas. A assinatura de uma função é composta do nome da função e da quantidade e dos tipos de parâmetros esperados
— Posição 787

> pela função.
— Posição 789

> Como mencionado anteriormente, as funções em JavaScript aceitam qualquer quantidade de parâmetros, e os tipos de parâmetro que uma função aceita não são especificados. Isso significa que em JavaScript as funções não têm assinatura.
— Posição 791

> Em JavaScript, no entanto, quando várias funções são
— Posição 802

> definidas com o mesmo nome, a função que aparecer por último em seu código será a vencedora. As funções declaradas anteriormente serão totalmente
— Posição 802

> removidas e a última será usada. Mais uma vez, usar objetos ajuda a entender essa situação:
— Posição 803

> O fato de as funções não terem assinatura em JavaScript não quer dizer que você não possa imitar o comportamento da sobrecarga de função. O número de parâmetros passados pode ser obtido por meio do objeto arguments, e essa informação pode ser usada para decidir
— Posição 810

> o que deve ser feito.
— Posição 812

> outras linguagens, mas o resultado final será o mesmo. Se você realmente deseja verificar se há tipos de dados diferentes, os operadores typeof ou instanceof poderão ser utilizados. Nota Na prática, comparar o parâmetro nomeado com undefined é mais comum do que basear-se em arguments.length \=\=\= 0.
— Posição 823

> Na prática, comparar o parâmetro nomeado com undefined é mais comum do que basear-se em arguments.length \=\=\= 0.
— Posição 826

> Todo escopo em JavaScript tem um objeto this que representa o objeto que chama a função.
— Posição 848

> Esse código funciona do mesmo modo que a versão anterior, mas, dessa vez, sayName() referencia this em vez de person. Isso significa que você pode facilmente alterar o nome da variável ou até mesmo reutilizar a função em objetos diferentes.
— Posição 861

> Isso ocorre porque this é definido quando a função é chamada, portanto this.name estará correto.
— Posição 884

> A capacidade de usar e de manipular o valor de this das funções é fundamental para um bom entendimento de orientação a objetos em JavaScript.
— Posição 889

> Embora this normalmente seja definido automaticamente, seu valor poderá ser alterado para obter resultados diferentes.
— Posição 891

> O primeiro método para manipular this é call(),
— Posição 894

> que executa a função com um determinado valor de this e com parâmetros específicos.
— Posição 895

> porque ela é acessada como um objeto em vez de ser acessada como um código a ser executado.
— Posição 914

> Como o método call() está sendo usado, não é preciso adicionar a função diretamente a cada objeto – você especifica explicitamente o valor de this em vez de deixar a engine do JavaScript fazer isso automaticamente.
— Posição 917

> método apply() funciona exatamente como call(), exceto pelo fato de ele aceitar somente dois parâmetros: o valor de this e um array ou um objeto semelhante a um array contendo os parâmetros a serem passados para a função (isso significa que você pode usar um objeto arguments como segundo parâmetro).
— Posição 922

> O terceiro método para mudar o valor de this
— Posição 946

> O primeiro argumento de bind() corresponde ao valor de this para a nova função. Todos os demais argumentos representam parâmetros nomeados que devem ser definidos permanentemente na nova função.
— Posição 947

> Nenhum parâmetro foi associado a sayNameForPerson1() ❶, portanto continua sendo necessário passar "label" para gerar a saída. A função sayNameForPerson2() não só faz o binding de this com person2 como também associa o primeiro parâmetro a "person2" ❷. Isso significa que você pode chamar sayNameForPerson2() sem passar nenhum argumento adicional. Essa parte do exemplo adiciona sayNameForPerson1() a person2 com o nome sayName ❸. A
— Posição 974

> A principal diferença entre uma função JavaScript e outros objetos está na propriedade interna especial \[\[Call\]\],
— Posição 987

> Como as funções são objetos, o construtor Function está presente.
— Posição 994

> Como em JavaScript não há o conceito de classes, tudo o que você tem para trabalhar a fim de implementar a agregação e a herança são as funções e os demais objetos.
— Posição 999

> Quando fizer isso, tenha em mente que os objetos em JavaScript são dinâmicos, o que significa que eles podem mudar a qualquer momento durante a execução do código.
— Posição 1003

> Enquanto as linguagens baseadas em classes restringem os objetos de acordo com uma definição de classe, os objetos em JavaScript não têm essa limitação.
— Posição 1005

> Quando uma propriedade é adicionada pela primeira vez a um objeto, o JavaScript utiliza um método interno chamado \[\[Put\]\] no objeto. O método \[\[Put\]\] cria um espaço no objeto para armazenar a propriedade. Isso pode ser comparado à adição de uma chave em uma tabela hash pela primeira
— Posição 1026

> Nota Propriedades próprias são diferentes de propriedades de protótipos, que serão discutidas no capítulo 4. Quando um novo valor é atribuído a uma propriedade, uma operação diferente chamada \[\[Set\]\] é executada.
— Posição 1035

> Propriedades próprias são diferentes de propriedades de protótipos, que serão discutidas no capítulo 4.
— Posição 1036

> Essa operação substitui o valor atual da propriedade pelo novo valor. No exemplo anterior, atribuir um novo valor a name
— Posição 1039

> Uma maneira mais confiável de testar a existência de uma propriedade é por meio do operador in.
— Posição 1065

> O operador in procura uma propriedade com um determinado nome em um objeto específico e retorna true se ela for encontrada. Com efeito, o operador in verifica se a chave especificada existe na tabela hash. Por exemplo, aqui está o que acontece quando in é usado para verificar se algumas propriedades existem no objeto person1: console.log("name" in person1); // true console.log("age" in person1); // true console.log("title" in person1); // false
— Posição 1066

> operador in procura uma propriedade com um determinado nome em um objeto específico e retorna true se ela for encontrada. Com efeito, o operador in verifica se a chave especificada existe na tabela hash. Por exemplo, aqui está o que acontece quando in é usado para verificar se algumas
— Posição 1066

> Tenha em mente que os métodos são apenas propriedades que referenciam funções, portanto você pode verificar a existência de um método da mesma forma. O exemplo a seguir adiciona uma nova função sayName() a person1 e utiliza in para confirmar a sua existência:
— Posição 1073

> Na maioria dos casos, o operador in é a melhor forma de determinar se uma propriedade existe em um objeto. Essa solução tem também a vantagem adicional de não avaliar o valor da propriedade, o que pode ser importante se uma avaliação como essa puder causar um problema de desempenho ou um erro.
— Posição 1083

> O operador in verifica
— Posição 1087

> tanto as propriedades próprias quanto as propriedades de protótipos, de modo que você deverá adotar uma abordagem diferente. Use o método hasOwnProperty(), que está presente em todos os objetos e retorna true somente se a propriedade dada existir e for uma propriedade própria.
— Posição 1087

> Use o método hasOwnProperty(), que está presente em todos os objetos e retorna true somente se a propriedade dada existir e for uma propriedade própria. Por exemplo, o código a seguir compara o resultado do uso de in em relação a hasOwnProperty() em diferentes propriedades de person1:
— Posição 1088

> O operador in retorna true para toString(), mas hasOwnProperty retorna false ❶.
— Posição 1106

> Você deve usar o operador delete para remover totalmente uma propriedade de um objeto.
— Posição 1114

> O operador delete atua em uma única propriedade do objeto e chama uma operação interna de nome \[\[Delete\]\]. Você pode pensar nessa operação como a remoção de um par chave/valor de uma tabela hash.
— Posição 1115

> Por padrão, todas as propriedades que você adicionar
— Posição 1135

> a um objeto são enumeráveis, o que significa que você pode iterar por elas usando um loop for-in.
— Posição 1135

> Object.keys()
— Posição 1149

> Normalmente, Object.keys() será usado em situações em que você deseja operar sobre um array de nomes de propriedades e for-in quando não precisar de um array.
— Posição 1161

> Nota Há uma diferença entre as propriedades enumeráveis retornadas em um loop for-in e aquelas retornadas por Object.keys(). O loop for-in também enumera propriedades do protótipo, enquanto Object.keys() retorna somente as propriedades
— Posição 1163

> próprias (da instância). A diferença entre propriedades do protótipo e propriedades próprias será discutida no capítulo 4.
— Posição 1167

> propertyIsEnumerable(), que
— Posição 1170

> Há dois tipos diferentes de propriedade: propriedades de dados e propriedades de acesso. As propriedades de dados contêm um valor, como a propriedade name dos exemplos anteriores deste capítulo.
— Posição 1186

> As propriedades de dados contêm um valor, como a propriedade name dos exemplos anteriores deste capítulo. O comportamento-padrão do método \[\[Put\]\]
— Posição 1187

> As propriedades de acesso não contêm valores; em vez disso, elas definem uma função a ser chamada quando a propriedade é lida (chamada getter) e uma função a ser chamada quando a propriedade é atualizada (chamada setter). As propriedades de acesso exigem somente um getter ou um setter, embora ambas possam existir.
— Posição 1189

> \_name: "Nicholas", ❷    get name() {
— Posição 1195

> set name(value) {
— Posição 1201

> (O underline no início é uma convenção comum para indicar que a propriedade é considerada privada, embora, na realidade, ela continue sendo pública).
— Posição 1212

> sintaxe usada para definir o getter ❷ e o setter ❸ para name se parece bastante com uma função, mas sem a palavra-chave function. As palavras-chave especiais get e set são usadas antes do nome da propriedade de acesso, seguidas por parênteses e do corpo
— Posição 1213

> da função. Espera-se que os getters retornem um valor, enquanto os setters recebem o valor sendo atribuído à propriedade como argumento. Embora esse exemplo use \_name para armazenar o valor da propriedade, você poderia facilmente armazenar o valor em uma variável ou até mesmo em outro objeto.
— Posição 1217

> As propriedades de acesso serão mais úteis se você quiser que a atribuição de um valor acione algum tipo de comportamento ou quando a leitura de um valor exigir o cálculo do valor de retorno desejado. Nota Não é necessário definir tanto um setter quanto um getter; você pode escolher um deles ou ambos. Se apenas um getter for definido, a propriedade será somente de leitura; uma tentativa de escrever nessa propriedade irá falhar silenciosamente em modo não restrito e irá causar um erro em modo restrito. Se somente um setter for definido, a propriedade será somente de escrita, e uma tentativa de ler o valor irá falhar silenciosamente tanto em modo restrito quanto em modo não restrito.
— Posição 1221

> Nota Não é necessário definir tanto um setter quanto um getter; você pode escolher um deles ou ambos. Se apenas um getter for definido, a propriedade será somente de leitura; uma tentativa de escrever nessa propriedade irá falhar silenciosamente em modo não restrito e irá causar um erro em modo restrito. Se somente um setter for definido, a propriedade será somente de escrita, e uma tentativa de ler o valor irá falhar silenciosamente tanto em modo restrito quanto em modo não restrito.
— Posição 1223

> Há dois atributos internos que são compartilhados entre as propriedades de dados e as propriedades de acesso.
— Posição 1234

> Enumerable\]\],
— Posição 1235

> Configurable\]\],
— Posição 1236

> Por padrão, todas as propriedades declaradas em um objeto são enumeráveis e configuráveis.
— Posição 1239

> Se quiser mudar os atributos das propriedades, você poderá usar o método Object.defineProperty(). Esse método aceita três argumentos: o objeto que tem a propriedade, o nome da propriedade e um objeto descritor da propriedade que contém os atributos a serem definidos.
— Posição 1240

> var person1 = { ❶    name: "Nicholas" }; Object.defineProperty(person1, "name", { ❷    enumerable: false });
— Posição 1246

> A última parte do código tenta redefinir a propriedade name para que ela seja configurável novamente ❻. No entanto isso gera um erro, pois uma propriedade não configurável não pode se tornar uma propriedade configurável novamente. Tentar
— Posição 1279

> Com esses dois atributos adicionais, você pode definir completamente uma propriedade de dado usando Object.defineProperty(), mesmo que a propriedade ainda não exista. Considere este código:
— Posição 1292

> Em seu lugar, as propriedades de acesso têm \[\[Get\]\] e \[\[Set\]\],
— Posição 1332

> A vantagem de usar atributos de propriedades de acesso em vez de utilizar a notação literal de objeto para definir as propriedades de acesso é que você também pode definir essas propriedades em objetos que já existem. Se quiser usar a notação literal de objeto, você deve definir as propriedades de acesso quando o objeto for criado.
— Posição 1337

> var person1 = {     \_name: "Nicholas" }; Object.defineProperty(person1, "name", {     get: function() {         console.log("Reading name");         return this.\_name;     },     set: function(value) {         console.log("Setting name to %s", value);         this.\_name = value;     },     enumerable: true,     configurable: true });
— Posição 1354

> Nesse código, name é uma propriedade de acesso que tem somente um getter ❶. Não há setter nem outros atributos explicitamente definidos como true, portanto o valor poderá ser lido, mas não poderá ser alterado.
— Posição 1391

> Object.defineProperties()
— Posição 1400

> var person1 = {}; Object.defineProperties(person1, { ❶    // propriedade de dados para armazenar informações     \_name: {         value: "Nicholas",         enumerable: true,         configurable: true,         writable: true     }, ❷    // propriedade de acesso     name: {         get: function() {             console.log("Reading name");             return this.\_name;         },         set: function(value) {             console.log("Setting name to %s", value);             this.\_name = value;         },         enumerable: true,         configurable: true     } });
— Posição 1404

> Object.getOwnPropertyDescriptor().
— Posição 1439

> Um desses atributos é \[\[Extensible\]\] – um valor booleano que indica se o objeto pode ser modificado.
— Posição 1458

> Ao definir \[\[Extensible\]\] com false, você pode evitar que novas propriedades sejam adicionadas a um objeto. Há três maneiras de conseguir esse resultado.
— Posição 1460

> Object.preventExtensions().
— Posição 1463

> A segunda maneira de criar um objeto não extensível é selar o objeto.
— Posição 1487

> Se um objeto estiver selado, você poderá somente ler e atualizar as suas propriedades.
— Posição 1490

> Object.seal()
— Posição 1491

> Entretanto, se uma propriedade contiver um objeto, você poderá modificá-lo. De fato, objetos selados em JavaScript representam a maneira de permitir que você tenha o mesmo grau de controle sem usar classes.
— Posição 1525

> A última maneira de criar objetos não extensíveis é congelá-los. Se um objeto estiver congelado, não será possível adicionar nem remover propriedades, mudar seus tipos nem atualizar qualquer propriedade de dados.
— Posição 1531

> Se um objeto estiver congelado, não será possível adicionar nem remover propriedades, mudar seus tipos nem atualizar qualquer propriedade de dados.
— Posição 1531

> Nota Objetos congelados são como “fotografias” de objetos em um determinado momento. Eles são muito limitados e raramente devem ser usados. Como ocorre com todos os objetos não extensíveis, você deve usar o modo restrito com objetos congelados.
— Posição 1568

> Pensar em objetos JavaScript como uma tabela hash em que as propriedades são apenas pares de chaves e valores pode ajudar.
— Posição 1572

> Tanto as
— Posição 1584

> Como o JavaScript não tem classes, cabe aos construtores e aos protótipos proporcionar um comportamento semelhante aos objetos.
— Posição 1602

> Um construtor é simplesmente uma função usada com o operador new para criar um objeto. Até este ponto, você viu diversos
— Posição 1606

> A vantagem dos construtores é que os objetos criados com o mesmo construtor têm as mesmas propriedades e os mesmos métodos.
— Posição 1608

> Como um construtor é somente uma função, ele deve ser definido da mesma maneira. A única diferença é que os nomes dos construtores devem começar com uma letra maiúscula para diferenciá-lo de outras funções.
— Posição 1611

> A única diferença é que os nomes dos construtores devem começar com uma letra maiúscula para diferenciá-lo de outras funções.
— Posição 1611

> Se não houver parâmetros para passar para o construtor, você poderá até mesmo omitir os parênteses: var person1 = new Person; var person2 = new Person;
— Posição 1621

> Embora o construtor Person não retorne nada explicitamente, tanto person1 quanto person2 são considerados instâncias do novo tipo Person. O operador new cria automaticamente um objeto do tipo especificado e o retorna. Isso significa também que o operador instanceof pode ser utilizado para deduzir o tipo do objeto. O código a seguir mostra instanceof em ação com os objetos recém-criados: console.log(person1 instanceof Person); // true console.log(person2 instanceof Person); // true
— Posição 1624

> operador new cria automaticamente um objeto do tipo especificado e o retorna.
— Posição 1626

> Toda instância de objeto é automaticamente criada com uma propriedade chamada constructor que contém uma referência à função construtora que a criou.
— Posição 1635

> console.log(person1.constructor \=\=\= Person); // true console.log(person2.constructor \=\=\= Person); // true
— Posição 1642

> Mesmo que esse relacionamento exista entre uma instância e o seu construtor, continua sendo aconselhável usar instanceof para verificar o tipo de uma instância. Isso se deve ao fato de a propriedade constructor poder ser sobrescrita,
— Posição 1646

> É claro que um construtor vazio não é muito útil. O propósito de um construtor é fazer com que seja fácil criar mais objetos com as mesmas propriedades e os mesmos métodos. Para fazer isso, simplesmente adicione qualquer propriedade que você quiser a this no construtor, como no exemplo a seguir: function Person(name) { ❶    this.name = name; ❷    this.sayName = function() {         console.log(this.name);     }; }
— Posição 1649

> Não há
— Posição 1665

> necessidade de retornar um valor na função porque o operador new gera o valor de retorno. Agora você pode usar
— Posição 1665

> Object.defineProperty() pode ser usado em um construtor para ajudar a inicializar a instância:
— Posição 1681

> function Person(name) {     Object.defineProperty(this, "name", {         get: function() {             return name;         },         set: function(newName) {             name = newName;         },         enumerable: true,         configurable: true     });     this.sayName = function() {         console.log(this.name);
— Posição 1683

> Não se esqueça de sempre chamar os construtores com new; caso contrário, você correrá o risco de mudar o objeto global em vez de alterar o objeto recém-criado. Considere o que acontece no código a seguir:
— Posição 1702

> Quando Person é chamado como uma função, sem o operador new, o valor de this no construtor é igual ao objeto this global. A
— Posição 1709

> variável person1 não contém um valor porque o construtor Person depende de new para fornecer um valor de retorno. Sem new, Person é somente uma função sem uma instrução de return.
— Posição 1711

> A atribuição a this.name cria uma variável global chamada name, em que o nome passado para Person é armazenado.
— Posição 1714

> Seria muito mais eficiente se todas as instâncias compartilhassem um método e esse método pudesse usar this.name para acessar o dado apropriado. É nesse caso que os protótipos entram em cena.
— Posição 1726

> Você pode pensar em um protótipo como uma receita para um objeto.
— Posição 1729

> IDENTIFICANDO UMA PROPRIEDADE DE PROTÓTIPO É possível determinar se uma propriedade está em um protótipo ao usar uma função como esta: function hasPrototypeProperty(object, name) {     return name in object && !object.hasOwnProperty(name); } console.log(hasPrototypeProperty(book, "title")); // false console.log(hasPrototypeProperty(book, "hasOwnProperty")); // true" Se a propriedade estiver em um objeto, mas hasOwnProperty() retornar false, então ela estará no protótipo.
— Posição 1748

> Uma instância mantém o controle de seu protótipo por meio de uma propriedade interna chamada \[\[Prototype\]\]. Essa propriedade é um ponteiro para o objeto referente ao protótipo que a instância está usando. Quando um novo objeto é criado usando new, a propriedade prototype do construtor é atribuída à propriedade \[\[Prototype\]\] desse novo objeto.
— Posição 1759

> Essa propriedade é um ponteiro para o objeto referente ao protótipo que a instância está usando.
— Posição 1760

> (tenha em mente que você não pode apagar uma propriedade do protótipo a partir de uma instância porque o operador delete atua somente em propriedades próprias).
— Posição 1811

> Esse exemplo também enfatiza um conceito importante: não se pode atribuir um valor a uma propriedade do protótipo a partir de uma instância. Como você pode ver na seção central da figura 4.2, atribuir um valor a toString faz com que uma nova propriedade própria seja criada na instância, deixando a propriedade do protótipo inalterada.
— Posição 1817

> não se
— Posição 1817

> pode atribuir um valor a uma propriedade do protótipo a partir de uma instância.
— Posição 1817

> A natureza compartilhada dos protótipos faz com que eles sejam ideais para definir métodos somente uma vez para todos os objetos de um dado tipo. Como os métodos tendem a fazer o mesmo para todas as instâncias, não há razão para que cada instância deva ter seu próprio conjunto de métodos.
— Posição 1821

> function Person(name) {     this.name = name; } Person.prototype = { ❶    sayName: function() {         console.log(this.name);     }, ❷    toString: function() {         return "[Person " + this.name + "]";     } };
— Posição 1867

> Esse código define dois métodos no protótipo: sayName() ❶ e toString() ❷. Esse padrão se tornou bem popular porque elimina a necessidade de digitar Person.prototype diversas vezes. Porém há um efeito colateral do qual você deve estar ciente:
— Posição 1879

> Usar a notação de objeto literal para sobrescrever o protótipo alterou a propriedade constructor, de modo que agora ela aponta para Object ❶ em vez de apontar para Person. Isso aconteceu porque a propriedade constructor está no protótipo, e não na instância do objeto. Quando uma função é criada, sua propriedade prototype é criada com uma propriedade constructor igual à função. Esse padrão sobrescreve completamente o objeto referente ao protótipo, o que significa que constructor será proveniente do novo objeto (genérico) criado, atribuído a Person.prototype. Para evitar isso, restaure a propriedade constructor para um valor adequado ao sobrescrever o protótipo:
— Posição 1887

> Isso aconteceu porque a propriedade constructor está no protótipo, e não na instância do objeto.
— Posição 1890

> function Person(name) {     this.name = name; } Person.prototype = { ❶    constructor: Person,     sayName: function() {         console.log(this.name);     },     toString: function() {         return "[Person " + this.name + "]";     } };
— Posição 1896

> var person1 = new Person("Nicholas"); var person2 = new Person("Greg"); console.log(person1 instanceof Person); // true console.log(person1.constructor \=\=\= Person); // true console.log(person1.constructor \=\=\= Object); // false console.log(person2 instanceof Person); // true console.log(person2.constructor \=\=\= Person); // true console.log(person2.constructor \=\=\= Object); // false
— Posição 1908

> Nesse exemplo, a propriedade constructor é especificamente atribuída no protótipo ❶. Fazer com que essa seja a primeira propriedade no protótipo para que você não se esqueça de incluí-la constitui uma boa prática.
— Posição 1917

> Talvez o aspecto mais interessante das relações entre construtores, protótipos e instâncias esteja no fato de não haver uma ligação direta entre a instância e o construtor. Entretanto há uma ligação direta entre a instância e o protótipo e entre o protótipo e o construtor.
— Posição 1920

> Lembre-se de que a propriedade \[\[Prototype\]\] contém somente um ponteiro para o protótipo, e qualquer alteração no protótipo estará imediatamente disponível a qualquer instância que o referenciar.
— Posição 1927

> A procura por uma propriedade nomeada ocorre sempre que a propriedade for acessada, o que proporciona fluidez ao processo.
— Posição 1961

> A capacidade de modificar o protótipo a qualquer momento tem repercussões interessantes para objetos selados e congelados. Quando Object.seal() e Object.freeze() forem utilizados em um objeto, você estará agindo somente na instância do objeto e em suas propriedades próprias. Não é possível adicionar novas propriedades próprias nem mudar as que já existem em objetos congelados, mas, certamente, você poderá continuar adicionando propriedades ao protótipo e poderá estender esses
— Posição 1962

> capacidade de modificar o protótipo a qualquer momento tem repercussões interessantes para objetos selados e congelados. Quando Object.seal() e Object.freeze() forem utilizados em um objeto, você estará agindo somente na instância do objeto e em suas propriedades próprias. Não é possível adicionar novas propriedades próprias nem mudar as que já existem em objetos congelados, mas, certamente, você poderá continuar adicionando propriedades ao protótipo e poderá estender esses objetos, como mostrado a seguir:
— Posição 1962

> Nesse ponto, você deve estar se perguntando se os protótipos também permitem modificar os objetos prontos que são padrões na engine do JavaScript. A resposta é sim.
— Posição 1986

> Array.prototype.sum = function() {     return this.reduce(function(previous, current){         return previous + current;     }); }; var numbers = [1, 2, 3, 4, 5, 6]; var result = numbers.sum(); console.log(result); // 21
— Posição 1990

> Embora possa parecer divertido e interessante modificar objetos prontos para testar novas funcionalidades, não é uma boa ideia fazer isso em ambiente de produção. Os desenvolvedores esperam que os objetos prontos se comportem de uma determinada maneira e que tenham determinados métodos. Alterar objetos prontos deliberadamente viola essas expectativas e faz com que outros desenvolvedores não tenham certeza de como os objetos devem funcionar.
— Posição 2015

> Os construtores são apenas funções normais chamadas com o operador new. Você pode definir seus próprios construtores sempre que quiser ter vários objetos com as mesmas propriedades. Os objetos criados por meio de construtores podem ser identificados pelo operador instanceof ou pelo acesso direto à sua propriedade constructor.
— Posição 2019

> Se uma propriedade própria não for encontrada, a procura será feita no protótipo.
— Posição 2029

> herdam propriedades de outras classes. Em JavaScript, entretanto, a herança pode ocorrer entre objetos que não tenham uma estrutura semelhante a classes que defina a sua relação. Você já está familiarizado com o sistema usado nessa herança: ela é feita por meio dos protótipos.
— Posição 2037

> Em JavaScript, entretanto, a herança pode ocorrer entre objetos que não tenham uma estrutura semelhante a classes que defina a sua relação. Você já está familiarizado com o sistema usado nessa herança: ela é feita por meio dos protótipos.
— Posição 2037

> Cadeia de protótipos e Object.prototype
— Posição 2039

> cadeia de protótipos ou herança prototípica.
— Posição 2041

> Essa é a cadeia de protótipos: um objeto herda de seu protótipo, enquanto esse protótipo, por sua vez, herda de seu protótipo, e assim por diante.
— Posição 2043

> Todos os objetos, incluindo aqueles que você mesmo define, automaticamente herdam de Object, a menos que você especifique o contrário
— Posição 2045

> Mais especificamente, todos os objetos herdam
— Posição 2046

> Muitos métodos usados em capítulos anteriores deste livro estão, na verdade, definidos em Object.prototype e, portanto, são herdados por todos os demais objetos. Esses métodos são: • hasOwnProperty()
— Posição 2060

> exemplo,
— Posição 2093

> Todos os objetos herdam de Object.prototype por padrão, portanto mudanças em Object.prototype afetam todos os objetos.
— Posição 2123

> Adicionar Object.prototype.add() faz com que todos os objetos tenham um método add(), não importa se isso faça sentido ou não. Essa questão tem sido um problema não só para os desenvolvedores, mas também para o comitê que trabalha na linguagem JavaScript: foi necessário inserir novos métodos em locais diferentes porque adicionar métodos em Object.prototype pode provocar consequências inesperadas.
— Posição 2138

> Por essa razão, Douglas Crockford recomenda sempre usar hasOwnProperty() em loops for-in1, como em: var empty = {}; for (var property in empty) {     if (empty.hasOwnProperty(property)) {         console.log(property);     } } Se, por um lado,
— Posição 2151

> não modificar Object.prototype.
— Posição 2162

> O tipo mais simples de herança é a herança entre objetos. Tudo o que você deve fazer é especificar que objeto deve ser o \[\[Prototype\]\] do novo objeto. Objetos literais têm seu \[\[Prototype\]\] definido como Object.prototype implicitamente, mas \[\[Prototype\]\] também pode ser explicitamente especificado no método Object.create(). O método Object.create() aceita dois argumentos. O primeiro argumento é o objeto que corresponderá ao \[\[Prototype\]\] do novo objeto. O segundo argumento opcional é um objeto contendo descritores de propriedade no mesmo formato usado por Object.defineProperties() (veja o capítulo 3). Considere o código a seguir: var book = {     title: "Princípios de orientação a objetos em JavaScript" }; // é o mesmo que: var book = Object.create(Object.prototype, {               title: {                 configurable: true,                 enumerable: true,                 value: "Princípios de orientação a objetos em JavaScript",                 writable: true                 }             }); As duas declarações nesse código são exatamente iguais. A primeira declaração usa um objeto literal para definir um objeto com uma única propriedade chamada title. Esse objeto herda automaticamente de Object.prototype,
— Posição 2164

> Você também pode criar objetos com um \[\[Prototype\]\] igual a null por meio de Object.create(), como mostrado a seguir: var nakedObject = Object.create(null); console.log("toString" in nakedObject); // false console.log("valueOf" in nakedObject); // false O nakedObject nesse exemplo é um objeto sem cadeia de protótipos. Isso significa que métodos prontos como toString() e valueOf() não estão presentes no objeto. De fato, esse objeto é um quadro totalmente em branco, sem propriedades predefinidas, o que o torna perfeito para a criação de uma tabela de pesquisa hash sem que você tenha de se preocupar com colisões de nomes com as propriedades herdadas.
— Posição 2233

> O JavaScript suporta a herança por meio de cadeia de protótipos. Uma cadeia de protótipos é criada entre os objetos quando o \[\[Prototype\]\] de um objeto é definido como o outro objeto.
— Posição 2471

> O padrão de módulo é um padrão de criação de objetos concebido para criar objetos únicos (singleton) com dados privados.
— Posição 2504

> abordagem básica consiste em usar uma IIFE (Immediately Invoked Function Expression, ou expressão de função imediatamente invocada) que retorna um objeto. Uma IIFE é uma expressão de função definida e chamada imediatamente para gerar um resultado.
— Posição 2505

> padrão de módulo permite usar variáveis normais como propriedades de objetos que não são expostas publicamente.
— Posição 2520

## Conexões
- [[Nicholas C. Zakas]]
- [[Grifos Kindle]]
