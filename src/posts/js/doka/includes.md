---
title: includes
name: includes
section: js
type: doka
tags:
  - jsDoka
autor: N_Lopin
co-autors:
designers:
contributors:
summary:
---

## Кратко

Этот метод определен у [массивов](/posts/js/doka/arrays/) и [строк](/posts/js/doka/string/).

Для _массивов_: проверяет, есть ли искомый элемент в массиве.

Для _строк_: проверяет, есть ли искомая подстрока в строке.

Возвращает `true`, если искомый элемент нашелся и `false` — если нет 😎

## Пример

Метод принимает один аргумент — значение, которое нужно проверить.

Массив:

```jsx
const dead = ["Joffrey", "Ned Stark", "Night king"]
const isJonDead = dead.includes("Jon Snow")
console.log(isJonDead) // напечатает false

const isJoffreyDead = dead.includes("Joffrey")
console.log(isJoffreyDead) // напечатает true
```

Строка:

```jsx
const text =
  "Посмотри, ведь это рядом наша панда. Мы бежим с тобой как-будто от гепарда."

console.log(text.includes("панда")) // true

console.log(text.includes("Обезьяна")) // false

// поиск идет с учетом регистра
console.log(text.includes("Панда")) // false
```

## В работе

<h3>Николай, <a href="https://twitter.com/N_Lopin" target="_blank" rel="nofollow noopener noreferrer" class="twitter">@N_Lopin</a></h3>

🛠Используй метод, когда нужно убедиться в том, что объект находится в массиве. Например, чтобы не добавить одно и то же значение дважды.

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="y-doka" data-slug-hash="VwjwNzg" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Использование includes, чтобы избежать дублирования">
  <span>See the Pen <a href="https://codepen.io/y-doka/pen/VwjwNzg">
  Использование includes, чтобы избежать дублирования</a> by doka (<a href="https://codepen.io/y-doka">@y-doka</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

🛠Будь внимателен, когда передаешь в `includes` объекты. Помни, что если два объекта выглядят одинаково, это не обязательно один объект.

```jsx
const phoneContacts = [
  { name: "Иван", lastName: "Таранов" },
  { name: "Игорь", lastName: "Иванов" },
  { name: "Мама", lastName: "" },
]

console.log(phoneContacts.includes({ name: "Мама", lastName: "" }))
// напечатает false, так как мы создали новый объект,
// хотя он выглядит так же как и тот, что в массиве
```

---

<p>Автор: Николай, <a href="https://twitter.com/N_Lopin" target="_blank" rel="nofollow noopener noreferrer" class="twitter">@N_Lopin</a></p>
