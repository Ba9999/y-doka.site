---
title: <header>
name: header
section: html
type: doka
tags:
  - htmlDoka
  - post
article: post
autor:
---

# Кратко

`<header>` создаёт «шапку» — верхнюю часть страницы сайта.

Обычно здесь находятся логотип, поисковая строка и кнопки навигации.

## Пример

```html
<header>
  <img src="yandex_logo.png" alt="Яндекс" />
</header>
```

## Как это понять

Контейнер `<header>` помогает собрать шапку сайта — самую верхнюю его часть, где обычно находятся логотип, строка поиска, меню, кнопки соцсетей или другие ключевые элементы.

Как правило, шапка выглядит одинаково на всех страницах сайта. Она помогает вернуться на главную страницу или попасть в нужный раздел, если в ней есть кнопки меню.

`<header>` можно закрепить в окне браузера, чтобы он всегда был доступен пользователю во время прокрутки страницы.

## Как пишется

Тег `<header>...</header>` всегда закрывается.

На странице может быть несколько тегов `<header>`. Но их нельзя помещать в контейнеры `<footer>`, `<address>` или другой `<header>`.

## Атрибуты

Можно применить любые универсальные атрибуты.

## Ещё пример

Вот как будет выглядеть `<header>` на странице-портфолио:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>header</title>
  </head>
  <body>
    <!-- Шапка -->
    <header>
      <h1>Ольга Данилюк</h1>
    </header>
    <!-- End Шапка -->

    <article>
      <h2>Добро пожаловать!</h2>
      <p>Рада приветствовать вас на своем сайте.</p>
    </article>
    <footer>Copyright Ольга Данилюк</footer>
  </body>
</html>
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="max-grachev" data-slug-hash="vwKqXN" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;header&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/max-grachev/pen/vwKqXN">
  &lt;header&gt;</a> by Max Grachev (<a href="https://codepen.io/max-grachev">@max-grachev</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## В работе

<h3>Алёна, <a href="https://twitter.com/ABatickaya" target="_blank" rel="nofollow noopener noreferrer" class="twitter">@ABatickaya</a></h3>

🛠 На главной странице сайта в `header` принято оборачивать первый экран. А вот на внутренних страницах в этот тег лучше обернуть повторяющуюся часть, в которой обычно находятся логотип и навигация по сайту.

Если придерживаться принципа, при котором каждый блок находится в отдельном файле, хедер можно реализовать один раз и вставлять уже готовый элемент на все страницы.
