# DOM

A DOM (Document Object Model) é uma representação hierárquica de elementos HTML/XML em uma página da web. Você pode usar JavaScript para interagir com a DOM, manipulando elementos, alterando conteúdo e respondendo a eventos. Aqui estão alguns exemplos de como usar a DOM com JavaScript:

### Com a DOM eu posso Modificar Elementos atráves do seu Id

```javascript
const varName = document.getElementById("id");
```

Após eu selecionar um elemento por seu Id, eu tenho a possibilidade de :

- Alterar seu conteúdo HTML usando:
  ```javascript
  varName.innerHTML = "Novo Conteudo";
  ```

- Adicionar classes a Tags
  ```javascript
  varName.classList.add("pClass");
  ```

- Remover uma classe da Tag
  ```javascript
  varName.classList.remove("otherClass");
  ```

- Adicionar Atributos a uma Tag
  ```javascript
  varName.setAttribute("atributo", "valor");
  ```

### Com a DOM também posso Manipular conteudos e elementos:

Após eu selecionar um elemento por seu Id, eu posso acessar seu valor usando .value

- Pegando o valor de um Input

```javascript
  let myIpt = document.getElementById("myIpt").value ||
  let value = myIpt.value;
```

- Criar um novo elemento e inserir ele no Body

```javascript
let newElement = document.createElement("p");
newElement.innerHTML = "hello world";
document.body.appendChild(newElement);
```

- Inserir o valor de um input em um elemento

```javascript
let myIpt = document.getElementById("myIpt");
let myBtn = document.getElementById("myBtn");
let myCleanBtn = document.getElementById("myCleanBtn");
let myCleanAllBtn = document.getElementById("myCleanAllBtn");

myBtn.addEventListener("click", function () {
  let newElement = document.createElement("p");
  newElement.classList.add("myP");
  newElement.innerHTML = myIpt.value;
  document.body.appendChild(newElement);
});

myCleanBtn.addEventListener("click", function () {
  clearOne();
});

myCleanAllBtn.addEventListener("click", function () {
  clearAll();
});

function clearOne() {
  let myP = document.getElementsByTagName("p");
  myP[0].remove();
}

function clearAll() {
  let myP = document.getElementsByTagName("p");
  while (myP.length > 0) {
    myP[0].remove();
  }
}

```


### Com a DOM também posso Controlar Eventos
