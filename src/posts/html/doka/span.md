---
title: <span>
name: span
section: html
type: doka
tags:
  - htmlDoka
  - post
article: post
autor:
---

## Кратко

С помощью тега `<span>` можно выбрать часть текста или другой информации в блоке и стилизовать её.

## Пример

```html
<p>
  Добавьте <span class="ingredient">базилик</span>,
  <span class="ingredient">арахис</span> и
  <span class="ingredient">чеснок</span> в блендер и перемешайте.
</p>
```

## Как это понять

Например, хочется, чтобы одно слово в абзаце было написано красным цветом. Помести это слово в коде в контейнер `<span>`...`</span>` и примени к нему CSS-стиль.

Этот тег очень похож на `<div>`, потому что тоже помогает сгруппировать элементы, чтобы применить к ним единый стиль. Разница лишь в том, что `<div>` собирает контент в отдельный блок, а `<span>` выделяет строчку или даже одну букву в этом блоке. Поэтому `<div>` называют блочными элементами, а `<span>` — строчным.

## Как пишется

```html
<span>...</span>
```

## Подсказки

💡 Иногда, чтобы отформатировать часть текста, можно использовать семантические элементы — это те, которые не просто являются контейнерами, а имеют своё значение, например, тег `<header>`, с помощью которого вы создаёте «шапку» своей страницы с меню и логотипом. Поэтому, если вместо `<span>` можно использовать семантический тег, например, `<address>` для выделения автора материала курсивом или `<mark>` для выделения текста жёлтым маркером, то используйте их.

## Ещё пример

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Тег SPAN</title>
    <style>
      body {
        font-family: Arial, sans-serif; /* Рубленый шрифт */
      }
      .letter {
        color: red; /* Красный цвет символов */
        font-size: 200%; /* Размер шрифта в процентах */
        font-family: serif; /* Шрифт с засечками */
        position: relative; /* Относительное позиционирование */
        top: 5px; /* Сдвиг сверху */
      }
    </style>
  </head>
  <body>
    <p>
      <span class="letter">Р</span>азумные люди приспосабливаются к окружающему
      миру. Неразумные люди приспосабливают мир к себе. Вот почему прогресс
      определяется действиями неразумных людей.
    </p>
    <p>Бернард Шоу</p>
  </body>
</html>
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="max-grachev" data-slug-hash="BMGxxq" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="span">
  <span>See the Pen <a href="https://codepen.io/max-grachev/pen/BMGxxq">
  span</a> by Max Grachev (<a href="https://codepen.io/max-grachev">@max-grachev</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## В работе

<h3>Владимир, <span class="twitter">-</span></h3>

🛠 `<span>` — крутой. Считается, что `<span>` — это когда тебе уже нечего добавить к тексту и ты уже использовал древние теги `<strong>` или `<em>`, то у тебя `<span>` — это последний бро, у которого по умолчанию нет предустановленных стилей, но ты можешь его немножко пересобрать и добавить стилей, чтобы он выглядел так, как ты хочешь.

Фишка в том, что в `<span>` можно встраивать вообще всё, что угодно. Внутри `<span>` можно собирать целые блоки, списки и, по факту, он может работать не только с текстом: я такое встречал очень часто. `<span>` можно встраивать друг в друга сколько угодно раз, чего не сделаешь, например, с тегом `<p>`. Допустим, ты хочешь, чтобы текст на сайте появлялся по одной букве, то ты добавляешь каждую букву в отдельный `<span>`, делаешь задержку и отдельно уже управляешь через JavaScript или CSS. `<span>` — тег, без которого современные сайты практически не могут существовать.

<h3>Алёна, <a href="https://twitter.com/ABatickaya" target="_blank" rel="nofollow noopener noreferrer" class="twitter">@ABatickaya</a></h3>

🛠 Тег `span` удобен, если нужно оформить другими стилями отдельное слово или словосочетание в тексте. Этот приём очень любят дизайнеры, чтобы акцентировать внимание на какой-то информации.

Например, выделим цветом важное для нас сообщение внутри заголовка на первом экране:

HTML

```html
<header class="header">
  <h1 class="header__title">
    We are
    <span class="header__title-accent">the best</span>
    company
  </h1>
</header>
```

CSS

```css
.header__title {
  max-width: 500px;
  font-family: Helvetica, Arial, sans-serif;
  font-size: 64px;
  color: #ffffff;
  text-align: center;
}

/* Задаём стили для текста, который нужно выделить */
.header__title-accent {
  display: block;
  padding: 5px;
  border: 1px solid #e72669;
  color: #e72669;
}
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="solarrust" data-slug-hash="arWjKL" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="arWjKL">
  <span>See the Pen <a href="https://codepen.io/solarrust/pen/arWjKL">
  arWjKL</a> by Alena (<a href="https://codepen.io/solarrust">@solarrust</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

<h3>Егор, <a href="https://twitter.com/furtivite" target="_blank" rel="nofollow noopener noreferrer" class="twitter">@furtivite</a></h3>

🛠 `<span>` — строковый элемент, поэтому по-умолчанию, у него нет высоты. Если нужна высота, то элементу стоит задать `display: block` или `display: inline-block`, или подумать: «А не нужен ли там `<div>`?»
