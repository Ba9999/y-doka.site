---
title: "float"
name: float
author: Lena Ryan
summary:
  - float
  - обтекание
  - clearfix
  - flow-root
---

## Кратко

Свойство помогает «обтекать» картинки текстом.

## Пример

<p class="codepen" data-height="352" data-theme-id="light" data-default-tab="result" data-user="lenaryan" data-slug-hash="PobvRGz" style="height: 352px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Float Demo">
  <span>Посмотреть пен <a href="https://codepen.io/lenaryan/pen/PobvRGz">
  Float Demo</a> на <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Как это понять

Иногда при вёрстке блока нужно, чтобы текст рядом с&nbsp;картинкой занимал всё оставшееся место, а&nbsp;после картинки располагался на&nbsp;всю ширину блока. Для таких ситуаций и&nbsp;создан `float`. Элемент, для которого указано это свойство, частично выходит из&nbsp;потока: все элементы блочного контекста, прописанные в&nbsp;коде после элемента с&nbsp;`float`, занимают его место, а&nbsp;элементы строчного контекста — «обтекают» его.

## Как пишется

```css
.element {
  float: none;
}
```

В&nbsp;файле стилей пишем селектор элемента, который будем «обтекать», и&nbsp;указываем одно из&nbsp;трёх значений свойства:

`left` — элемент встанет у&nbsp;левого края родительского блока.

`right` — элемент встанет у&nbsp;правого края родительского блока.

`none` — значение по&nbsp;умолчанию, элемент останется в&nbsp;потоке.

## Подсказки

💡 Применяя `float` к элементу, мы неявно делаем его блочным.

## В работе

🛠 `float` не&nbsp;предназначен для создания сеток или табличной раскладки! Раньше не было другого способа разбить контент на колонки и поставить их рядом друг с другом. Но сейчас для этого есть [flexbox](https://y-doka.site/css/long/flexbox-guide/) и [grid](https://y-doka.site/css/long/grid-guide/), а `float` используется для «обтекания».

🛠 Чтобы прекратить влияние `float` и&nbsp;вернуться к&nbsp;обычному потоку, после блока с&nbsp;обтеканием можно вставить пустой элемент, обычно с&nbsp;классом `clearfix`, и&nbsp;прописать свойство `clear`:

```css
.clearfix {
  clear: both;
}
```

Также можно не вставлять отдельный элемент в разметку, а обойтись псевдоэлементом [::after](https://y-doka.site/css/doka/after/) - этот вариант предпочтительнее.

🛠 Несколько лет назад для этой же цели появилось свойство `display: flow-root`. Достаточно применить его к&nbsp;блоку, внутри которого есть элемент с&nbsp;применённым к&nbsp;нему `float` — и&nbsp;влияние `float` не&nbsp;будет распространяться вне этого блока.
