## Manipulação do DOM
- O que é a DOM
- Seleção de Elementos
- Manipulação do HTML
- Manipulação do CSS
- Events
- Event Listner


## DOM
O `DOM` significa `Modelo de Documento por Objetos`, ou seja, é a interface que organiza os documentos numa estrutura de árvore para que se possa manipular os diferentes objetos/nós com recurso a métodos e propriedades.

## Seleção de elementos

### ID
- `document.getElementByID('id')` seleciona o primeiro elemento do DOM que possui o ID passado como argumento. 

### Class
- `document.getElementByClassName('class')` seleciona os elementos do DOM que possuem a classe passada como argumento. O valor devolvivido, independemente de só haver um elemento, é uma `HTMLCollection`. Esta lista é atualizada ao vivo caso sejam adicionados novos elementos com essa classe.

### Tag
- `document.getElementByTagName('tag')` seleciona os elementos do DOM que possuem a tag passada como argumento. O valor devolvivido, independemente de só haver um elemento, é uma `HTMLCollection`. Esta lista é atualizada ao vivo caso sejam adicionados novos elementos com essa tag.


### querySelector
- `document.querySelector('seletor')` seleciona o primeiro elemento do DOM que possuem o seletor passado como argumento. 

### querySelectorAll
- `document.querySelectorAll('seletor')` seleciona os elementos do DOM que possuem o seletor passado como argumento. O valor devolvivido, independemente de só haver um elemento, é um `node`. Este valor é estático.

## Manipulação do HTML
O JavaScript pode manipular de forma dinâmica o HTML

### Mudar o output do HTML
Para mudar o output do HTML utiliza-se o método `document.write()`.

`````Html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <script>
            document.write('Hello World!');
        </script>
    </body>
</html>
`````

### Mudar o conteúdo de um elemento HTML
Para mudar o contéudo de um elemento HTML utiliza-se a propriedade `.innerHTML`.

`````Html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1>Título</h1>
        <script>
        document.querySelector('h1').innerHTML = 'Hello World!';
        </script>
    </body>
</html>
`````

### Mudar o valor de um atributo
Para mudar o contéudo de um atibuto utiliza-se a propriedade com o nome do atributo.

`````Html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <a href="https://site1.com"></a>      
        <script>
        document.querySelector('a').href = 'https://site2.com';
        </script>
    </body>
</html>
`````

### Manipulação do CSS
Para mudar os estilos de um elemento HTML utiliza-se a propriedade `.style` seguida da propriedade com o nome do estilo. Em JavaScript a sintaxe das propriedade de estilos é ligeiramente diferente da sintaxe do CSS:

`````Html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1>Título</h1>
        <script>
        document.querySelector('h1').style.color = 'red';
        </script>
    </body>
</html>
`````

## Eventos

### Exemplos de Eventos

[Lista completa](https://www.w3schools.com/jsref/dom_obj_event.asp)

### Eventos como atributos

### Eventos como propriedade

### Eventos como método
`addEventListener()` é um método que anexa um eventos a determinado elemento

#### Sintaxe
`element.addEventListener(event, function, useCapture);`

#### Exemplo