# Introdução ao Javascript

## Conteúdos
- Introdução 
- Adicionar 
- Variáveis e Constantes
- Estrutura de Dados
- Operadores
- Condicionais
- Funções
- Estruturas de repetição
- Objectos
- DOM



## Introdução ao Javascript
Javascript [JS] é uma linguagem de programação "client-side" que permite adicionar comportamentos aos elementos HTML. Esta linguagem é fundamental para o desenvolvimento web.

## ES6
Em 2015 houve a segunda maior revisão do Javascript a que se dá o nome de ECMAScript 2015, ES6 ou ECMAScript 6. Nesta revisão foram acrescentadas vários novos recursos e funcionalidades tornando o Javascript mais acessível, versátil e limpo.

## Adicionar o Javascript
### Interno
O código JS pode ser adicionado a uma página HTML dentro da tag `<script>[conteúdo javascript]</script>`. Preferecialmente, este código deve ser colocado antes de se fechar o `</body>` para garantir que o HTML está todo renderizado antes do JS começar a correr.

````html
<html>
    <head>
    </head>
    <body>
        <script>
            window.alert('Olá Mundo!');
        </script>
    </body>
</html>
````

### Externo
O código JS também pode ser escrito num ficheiro externo com a extensão `.js` e adicionado através do atributo `src=""` à tag `<script src="[caminho relativo]"></script>`.

## Variáveis e Constantes
"Variável" é um recurso em programação para armazenar um valor na memória do computador durante a execução de um algoritmo. Em JS uma variável pode ser declarada pela expressão `var`, `let` ou `const`.

````Javascript
let identificador = valor;
````
````Javascript
    let x = 5;
    let y = 10;
    let total = x + y;
````

- x tem o valor 5;
- y tem o valor 10;
- total tem o valor de 15;

Os valores associados a variáveis declaradas pelas expressões `var` e `let` podem ser alterados, enquando os valores associados a variáveis `const` não podem ser alterados.

Os indentificadores podem começar com uma letra, $ ou _; Não podem começar com números; Não podem conter espaços; Não podem ser palavras que já façam parte da linguagem JS (ex: alert). 

### Camel Case
A linguagem JS utiliza como o padrão o Camel Case: uma maneira de escrever palavras compostas em que a primeira letra de cada palavra é maiúscula.

````
    let nome = "João";
    let sobrenome = "Oliveira";
    let nomeCompleto = nome + ' ' + sobrenome;
````

## Estruturas de dados
Uma estrutura de dados é um conjunto de valores ou de operações. As principais estruturas de dados definidas por defeito no JS são:

### String
Sequência de caracteres colocados entre `""`.

````Javascript
     let nome = "João";
     let sobrenome = "Oliveira";
````

#### Concatenar

````Javascript
     let nome = "João";
     let sobrenome = "Oliveira";
     let nomeCompleto = nome + ' ' + sobrenome; //João Oliveira
````

#### Template Strings

````Javascript
     let nome = "João";
     let sobrenome = "Oliveira";
     let anos = 30;  
     
     let frase = `O ${nome} ${sobrenome} tem ${anos} anos.`; //O João Oliveira tem 30 anos.
````

### Número
Dados numéricos que podem ser do tipo inteiro ou float (decimal).
````Javascript
     let anos = 30;
````

### Boolean
Tipo de dados que varia entre `verdadeiro` e `falso`.
````Javascript
     let verdadeiro = true;
     let falso = false;
````

### Array
Coleação de dados armazenada em forma de lista.
````Javascript
     let alunos = ['João', 'Maria', 'Sara'];
````

### Objeto
Coleção de propriedades e métodos que associam uma chave a um valor.
````Javascript
    let aluno = {
        nome: 'Sara',
        idade: 30,
        altura: 1.65,
    };
````

## Operadores 
### Aritméticos
- `+` adição 
- `-` subtração
- `*` multiplicação 
- `/` divisão 
- `**` exponencial 
- `%` resto da divisão 
- `++` incrementação
- `--` decrementação

### Atribuição Composta
- `=` atribuição 
- `+=` atribuição de adição
- `-=` atribuição de sub

Nome | Operador | Desconstrução
-- | -- | -- 
atribuição | x = y | x = y
atribuição de adição | x += y | x = x + y
atribuição de subtração | x -= y | x = x - y

### Relacionais
- `>` maior 
- `<` menor
- `>=` maior ou igual
- `<=` menor ou igual
- `==` igual
- `!=` diferente

### Lógicos
- `!` não (operador unário)
- `&&` e (conjunção)
- `||` ou (dijunção)

## Condicionais
Uma condicional avalia se determinada afirmação é verdadeira ou falsa. No Javascript a condicional mais comum é a `if... else`.

`````
if (condicao) {
  //se a condição for verdadeira, executa este código
} else {
  //senão, executa este código
}
`````

Também podemos utilizar o `else if`
`````
if (condicao1) {
  //se a condição 1 for verdadeira, executa este código
} else if(condicao2) {
  //senão e se a condição 2 for verdadeira, executa este código
} else {
  //senão, executa este código
}
`````

## Funções
As funções funcionam como acções no Javascript. Elas permitem executar determinado código e podem ter argumentos e retornar determidado valor. As funções são declaradas pelo termo `function` e têm de ser chamadas ou executadas.
`````Javascript
function nomeFuncao(argumentos){
    // corpo da funcao
}

nomeFuncao(); // chamar funcao
`````

### Função de execução
Este tipo de funções, como o próprio nome indica, serve para executar determinado código
`````Javascript
function ola(){
    console.log('Hello World'); // Hello World
}
`````

### Função de retorno
Neste caso o termo `return` especifica o valor a ser retornado pela função
`````Javascript
function soma(x, y){
    var soma = x + y;
    return soma;
}
soma(10, 5); // 15
`````

`````Javascript
function cambio(dolar){
    var euro = dolar * 0,83;
    return euro;
}

cambio(10); // 8.3
`````

## Estruturas de repetição

### For
O `for` é uma estrutura de repetição recebe três argumentos:
- valor inicial de uma variável
- condição de continuação / valor de parar
- expressão que acontece no final de cada repetição (loop)

`````Javascript
var alunos = ['João', 'Maria', 'Sara'];
for(var i = 0; i < alunos.length; i++){
    console.log(alunos[i]); 
}
`````

#### Quebrar o loop
`````Javascript
var alunos = ['João', 'Maria', 'Sara'];
for(var i = 0; i < alunos.length; i++){
    console.log(alunos[i]); 
    if(alunos[i] === 'Maria'){
        break;
    }
}
`````

### For Each
O `forEach` é uma estrutura de repetição que recebe uma função que por sua vez recebe três argumentos:
- a variável do item
- o index do item
- o array total

`````Javascript
var alunos = ['João', 'Maria', 'Sara'];
alunos.forEach(function(aluno, index, array){
    console.log('aluno: ' + aluno)
    console.log('index: ' + index)
    console.log('array: ' + array)
})
`````


### While
O `while` é uma estrutura de repetição que normalmente se utiliza quando não se sabe o valor de parar.

`````Javascript
var i = 1000;
while(i > 10){
    console.log(i);
    i /= 15;
}
`````

## Objectos
O JavaScript é uma linguagem orientada a objectos o que significa que é composta por colecções de propriedades e métodos chamadas de 'objectos'. 

### Propriedades
Uma propriedade de um objecto é uma variável associada que permite aceder a determidado dado desse objecto.

`````Javascript
var nome = "Sara"
console.log(nome.lenght); // 4
`````

### Métodos
Um médoto de um objecto é uma função associada que executa uma acção.


`````Javascript
var nome = "Sara"
console.log(nome.toUpperCase()); // SARA
`````


## DOM Javascript

### O que é o DOM?

Document Object Model é o conjunto de objectos que constituem um website e que permite o acesso aos diferentes componentes. Por outras palavras, é a árvore de elementos em que a raiz é a “window”.

```Javascript
window.document.URL; //url da págiina
window.document.write('Hello World'); //escreve na tela 'Hello World'
```

### Principais Seleccionadores

#### Por ID

Selecciona o elemento que tenha determinado ID.

```Javascript
document.getElementByID();
```

#### Por Tag

Selecciona todos os elementos que tenham determinada Tag.

```Javascript
document.getElementsByTagName();
```

#### Por Classe

Selecciona todos os elementos que tenham determinada classe.

```Javascript
document.getElementsByClassNam();
```

#### Por Selector

Selecciona a partir de elementos do CSS

```Javascript
document.querySelectorAll(); //devolve uma NodeList
document.querySelector(); //devolve o primeiro elemento que tenha o selector
```

### Eventos

Eventos são todas as reações que um elemento possa ter. 

Lista de eventos: [https://developer.mozilla.org/pt-BR/docs/Web/Events](https://developer.mozilla.org/pt-BR/docs/Web/Events)

Os eventos podem ser colocados no HTML ou no JavaScript. 

#### HTML

No caso do HTML tem que se colocar ‘on’ antes do nome do evento.

```html
<div onclick="funcao()">Clicar</div>
```

#### JavaScript

No JavaScript utiliza-se o método `addEventListener()`.

```Javascript
document.querySelector('div').addEventListener('click', funcao);
```

