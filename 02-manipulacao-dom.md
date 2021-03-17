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

### Mudar o conteúdo do HTML

### Mudar o valor de um atributo

## Manipulação do CSS

### Mudar estilos de css

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