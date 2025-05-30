# 📝 Minha Lista de Tarefas

Authors:

- Bruno Silva o Tampa !
- Cristiano Costa

## Comandos para serem usados no GITHUB

`git add .` = sever para adicionar as mudanças, para fazer commit no github .

`git commit -m " descrição para o commit ou nome sobre o assunto para o commit "` = server para colocar commit no github (respositório minha lista de tarefas)

`git push origin main` = server para enviar as mudanças da maquina local para o github (respositório minha lista de tarefas)

`git pull` = Syncronizar o codigo da minha maquina local, com o codigo do repositorio no github (⚠️ Atencao: pode dar conflitos)

`git clone Adiciona_url_do_repositorio` = Voce pode interagir com outros repositorios no github e clonar ele localmente. Porem voce nao vai conseguir puxar suas informacoes para o repositorio principal se nao houver permissoes.

---

## 📘 JavaScript Data Types

JavaScript has two main categories of data types: Primitive and Reference types.

---

### 🟢 Primitive Types (Immutable)

| Type        | Description                   | Example                  |
| ----------- | ----------------------------- | ------------------------ |
| `string`    | Text values                   | `let name = "João";`     |
| `number`    | Integer or decimal values     | `let age = 25;`          |
| `boolean`   | True or false                 | `let isLoggedIn = true;` |
| `undefined` | Variable declared but not set | `let x;`                 |
| `null`      | Intentional absence of value  | `let user = null;`       |
| `bigint`    | Very large numbers            | `let bigNum = 123n;`     |
| `symbol`    | Unique, immutable identifier  | `let id = Symbol("id");` |

---

### 🟣 Reference Types (Objects)

| Type       | Description                   | Example                                   |
| ---------- | ----------------------------- | ----------------------------------------- |
| `object`   | Collection of key-value pairs | `let person = { name: "Ana" };`           |
| `array`    | Ordered list of values        | `let fruits = ["apple", "banana"];`       |
| `function` | Executable block of code      | `function greet() { console.log("Hi"); }` |

---

### 🧪 `typeof` Examples

```js
typeof "text"; // "string"
typeof 123; // "number"
typeof true; // "boolean"
typeof undefined; // "undefined"
typeof null; // "object"  // quirk in JS
typeof {}; // "object"
typeof []; // "object"  // (but it's an array)
typeof function () {}; // "function"
```

# 🧪 JavaScript Data Type Practice – 10 Exercises

Practice and reinforce your understanding of JavaScript data types.

---

## 1. Declare variables of all primitive types

Create one variable of each primitive type.

```js
let nome = "Carlos"; // string
let idade = 30; // number
let ativo = true; // boolean
let saldo; // undefined
let endereco = null; // null
let big = 123456789n; // bigint
let id = Symbol("id"); // symbol
```

## 2. Check the data type using typeof

Use typeof to log each variable’s type.

```js
console.log(typeof nome); // "string"
console.log(typeof idade); // "number"
console.log(typeof ativo); // "boolean"
console.log(typeof saldo); // "undefined"
console.log(typeof endereco); // "object" (quirk!)
console.log(typeof big); // "bigint"
console.log(typeof id); // "symbol"
```

## 3. Create an object representing a car

Object should include string, number, and boolean values.

```js
let carro = {
  marca: "Toyota",
  ano: 2020,
  ligado: true,
};
console.log(carro.marca);
```

## 4. Create an array with 5 fruits

Then access the first and last item.

```js
let frutas = ["banana", "maçã", "uva", "melão", "laranja"];

console.log(frutas[0]); // banana
console.log(frutas[frutas.length - 1]); // laranja
```

## 5. Write a function that returns your name

Use a function expression.

```js
const dizerNome = function () {
  return "Seu Nome";
};

console.log(dizerNome()); // "Seu Nome"
```

## 6. Change a variable from undefined to a value

Declare a variable, then assign a string to it.

```js
let profissao;
profissao = "Desenvolvedor";
console.log(profissao); // "Desenvolvedor"
```

## 7. Convert a number to a string

Use String() or .toString().

```js
let numero = 100;
let texto = numero.toString();

console.log(typeof texto); // "string"
```

## 8. Create a function that returns the type of a value

```js
function tipoDe(valor) {
  return typeof valor;
}

console.log(tipoDe(true)); // "boolean"
console.log(tipoDe(42)); // "number"
console.log(tipoDe("JS")); // "string"
```

## 9. Compare null vs undefined

```js
let a = null;
let b;

console.log(a === b); // false
console.log(typeof a); // "object"
console.log(typeof b); // "undefined"
```

## 10. Declare a bigint and add two values

```js
let big1 = 10000000000000000n;
let big2 = 20000000000000000n;

console.log(big1 + big2); // 30000000000000000n
```

---

---

## Arquitetura do Projeto

A arquitetura do projeto se dividirá em três etapas: A estrutura do projeto (HTML), a aparência do projeto (CSS) e a funcionalidade da lista de tarefas (JavaScript).

### 🧑‍🎨 Design:

#### Design One:

<img src="assets/DesignOne.png" width="80%" >

<br />
<br />

Color Pallet:

```css
    #3aafa9
    #2b7a78
    #def2f1
    #545454
    #c7c9cd
    #ffffff
```

#### Design Two:

<img src="assets/DesignTwo.png" width="80%" >

<br />
<br />

Color Pallet:

```css
    #5d5174
    #9680a4
    #e2deea
    #545454
    #e4e0dd
    #ffffff
```

#### Design Three:

<img src="assets/DesignThree.png" width="80%" >

<br />
<br />

Color Pallet:

```css
    #545454
    #edecec
    #e4e0dd
    #c8dbf8
    #ffffff
```

### HTML

1. O objetivo é analisar o design proposto e recriar apenas a estrutura em HTML.

- Dicas:
  - Seja o mais semantico possível (https://www.youtube.com/watch?v=tAFRHcEH-Pc)

| Elemento        | Propósito                             |
| --------------- | ------------------------------------- |
| `<aside>`       | Barra lateral (sidebar)               |
| `<nav>`, `<ul>` | Menu de navegação                     |
| `<main>`        | Área principal de conteúdo            |
| `<header>`      | Barra superior com título e busca     |
| `<section>`     | Agrupamento de conteúdo               |
| `<footer>`      | Rodapé (ou paleta de cores, se usada) |

---

- Desenhe retângulos ao redor das seções de maneira lógica.
- Pense na navegação lateral, barra superior, conteúdo principal e rodapé como blocos visuais.
- Cada bloco representa uma possível tag ou componente na estrutura HTML.
  Example: <img src="assets/box-method.png" width="50%" >

**[⬆ Back to Top](#-minha-lista-de-tarefas)**

---
