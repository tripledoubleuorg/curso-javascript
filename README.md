# Javascript

## Conteúdos
- [Introdução ao Javascript](#introdução-ao-javascript)
- [Adicionar Javascript](#adicionar-javascript)
- [Primeiro Javascript](#primeiro-javascript)
- [Variáveis](#variáveis)
- [Tipos de variáveis](#tipos-de-variáveis)
- [Operadores](#operadores)
- [Condicionais](#condicionais)
- [Funções](#funções)
- [Arrays](#arrays)
- [Loops](#loops)



## Introdução ao Javascript
Javascript é uma linguagem de programação "client-side" que permite adicionar comportamentos aos elementos HTML.

## Adicionar Javascript
### Interno
O código Javascript pode ser adicionado a uma página HTML dentro da tag `<script>[conteúdo javascript]</script>`. Preferecialmente, este código deve ser colocado antes de se fechar o `</body>` para garantir que o HTML está todo renderizado antes do JS começar a correr.

### Externo
O código Javascript também pode ser escrito num ficheiro externo com a extensão `.js` e adicionado através do atributo `src=""` à tag `<script src="ficheiro.js"></script>`.

## Primeiro Javascript
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

## Variáveis
"Variável" é um recurso em programação para armazenar um valor na memória do computador durante a execução de um algoritmo. 

Em JS uma variável é declarada pela expressão `var`, `let` ou `const`.

### Sintaxe
````javascript
var/let/const identificador = valor;
````

### Nome
Os indentificadores podem começar com uma letra, $ ou _; Não podem começar com números; Não podem conter espaços; Não podem ser palavras que já façam parte da linguagem js (ex: alert) [lista de palavras reservadas](https://www.w3schools.com/js/js_reserved.asp).


### Exemplo
````javascript
    var x = 5;
    var y = 10;
    var total = x + y;
````
- x tem o valor 5;
– y tem o valor 10;
- total tem o valor de 15;

### var VS let VS const
- `var`, `let` – o seu valor pode ser alterado
- `const`– o seu valor não pode ser alterado

## Tipos de variáveis
Em JS existem vários tipos de variáveis mas vamos começar pelas seguinte:

### String
Variável que armazena uma sequência de caracteres colocados entre `""`.
````javascript
    var nome = "Sara"; 
````

### Número
Variável que armazena números e que pode ser do tipo inteiro ou float (decimal).
````javascript
    var idade = 30; //inteiro
    var altura = 1.65 //float
````

### Boolean
Variável que pode ser verdadeira ou falsa.
````javascript
    var aluno = true;
````

### Array
Variável vectorial que armazena vários valores.
````javascript
    var alunos = ['João', 'Maria', 'Sara'];
````

### Objecto
Variável vectorial que armazena vários valores de um objecto.
````javascript
    var alunos = {
        nome: 'Sara';
        idade: 30;
        altura: 1.65;
    };
````

## Operadores 
### Aritméticos
- `+` adição 
- `-` subtração
- `*` multiplicação 
- `/` divisão 
- `**` exponencial 
- `++` incrementação
- `--` decrementação

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

### Boolean
`````javascript
if (condicao) {
  //se a condição for verdadeira, executa este código
} else {
  //senão, executa este código
}
`````

Também podemos utilizar o `else if`
`````javascript
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
`````javascript
function nomeFuncao(){
    // corpo da funcao
}

nomeFuncao(); // chamar funcao
`````

### Função de execução
Este tipo de funções, como o próprio nome indica, serve para executar determinado código
`````
function ola(){
    alert('Hello World')
}
`````

### Função de retorno
Neste caso o termo `return` especifica o valor a ser retornado pela função
`````
function soma(x, y){
    var soma = x + y;
    return soma;
}
`````
## Arrays
Um array é uma estrutura de dados armazenados numa única variável.

### Introdução ao Arrays

#### Criar um array
Há duas formas de criar um array vazio.
````` Javascript
var animais = new Array();
var animais = [];
`````

#### Sintaxe do array
````` Javascript
var animais = ['elefante', 'leão', 'girafa', 'cão'];
`````

#### Aceder a um elemento do array
Para aceder a um elemento do array deve-se utilizar o index do ele.
````` Javascript
var elefante = array[0] 
console.log(elefante)  //elefante;

var cao = array[3] 
console.log(cao) //cão
`````

### Metodos 
#### push()
Acrescenta elementos no final do array.
````` Javascript
var animais = ['elefante', 'leão'];
animais.push('elefante', 'leão');
console.log(animais) //elefante, leão, girafa, cão
`````

#### unshif()
Acrescenta elementos no início do array.
````` Javascript
var animais = ['elefante', 'leão'];
animais.unshif('girafa', 'cão');
console.log(animais) //girafa, cão, elefante, leão
`````

#### pop()
Apaga o último elemento do array.
````` Javascript
var animais = ['elefante', 'leão', 'girafa', 'cão'];
animais.pop();
console.log(animais) //elefante, leão, girafa
`````

#### shift()
Apaga o primeiro elemento do array.
````` Javascript
var animais = ['elefante', 'leão', 'girafa', 'cão'];
animais.shift();
console.log(animais) //leão, girafa, cão
`````

## Loops
Loops são estruturas de repetição.

### While
`````Javascript
while (condição) {
  // corpo do loop
}
`````

`````Javascript
var i = 0;
while(i < 10){
    console.log(i); //0,1,2,3,4,5,6,7,8,9
    i++;
}
`````

### For
`````Javascript
for (começo; condição; incrementação) {
  // corpo do loop
}
`````

`````Javascript
for(var i = 0; i < 10; i++){
    console.log(i); //0,1,2,3,4,5,6,7,8,9
}
`````







