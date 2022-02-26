# Introdução ao Javascript

## Conteúdos
- Introdução 
- Adicionar 
- Dados
- Variáveis
- Operadores
- Condicionais
- Funções
- Loops
- Propriedades
- Metodos


## Introdução ao Javascript
Javascript [JS] é uma linguagem de programação "client-side" que permite adicionar comportamentos aos elementos HTML.


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

## Estruturas de dados built-in
Uma estrutura de dados é um conjunto de valores ou de operações. As principais estruturas de dados definidas por defeito no JS são:

### String
Sequência de caracteres colocados entre `""`.

### Número
Dados numéricos que podem ser do tipo inteiro ou float (decimal).

### Boolean
Tipo de dados que varia entre `verdadeiro` e `falso`.

### Array
Coleação de dados armazenada em forma de lista.
[ver mais]
````Javascript
     ['João', 'Maria', 'Sara'];
````

### Objeto
Coleção de propriedades e métodos que associam uma chave a um valor.
````Javascript
    {
        nome: 'Sara',
        idade: 30,
        altura: 1.65,
    };
````


## Variáveis
"Variável" é um recurso em programação para armazenar um valor na memória do computador durante a execução de um algoritmo. Em JS uma variável pode ser declarada pela expressão `var`.

````Javascript
var identificador = valor;
````

Os indentificadores podem começar com uma letra, $ ou _; Não podem começar com números; Não podem conter espaços; Não podem ser palavras que já façam parte da linguagem JS (ex: alert). 

````
    var x = 5;
    var y = 10;
    var total = x + y;
````

- x tem o valor 5;
- y tem o valor 10;
- total tem o valor de 15;


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

## Loops
Loops são estruturas de repetição.

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

## Propriedades
As propriedades são variavéis associadas a um objeto.
`````Javascript
var aluno = {
    nome: 'João',
    idade: 20,
    inscrito: true,
}

aluno.nome // João
aluno.idade // 20
aluno.inscrito // true
`````

## Métodos
Os métodos são funções associadas a objeto.
`````Javascript
var aluno = {
    nome: 'João',
    idade: 20,
    inscrito: true,
    modulos: 4,
    mensalidade: function(valor) {
        return valor * this.modulos;
    },
}

aluno.nome // João
aluno.idade // 20
aluno.inscrito // true
aluno.mensalidade(10) // 40
`````







