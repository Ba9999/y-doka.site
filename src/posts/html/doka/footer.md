---
title: "<footer>"
name: footer
author: vladimir
co-authors:
  - ABatickaya
summary:
  - тэг
  - тег
  - футер
  - подвал
---

## Кратко

`<footer>` создаёт нижнюю часть страницы или блока — «подвал». Обычно здесь находятся контакты, ссылки на разделы сайта, копирайт.

## Пример

В нашем блоке со статьёй будет небольшой футер с указанием автора и его контактами:

```html
<article>
  <h3>Очень важная статья</h3>
  <p>Исходя из данного утверждения, марксизм неизбежен. Коммунизм, с другой стороны, означает экзистенциальный коллапс Советского Союза. Культ личности доказывает гуманизм.</p>
  <footer>
    <p>Ольга Данилюк</p>
    <p>Почта: <a href="mailto:someone@yandex.ru"> someone@yandex.ru</a>.</p>
  </footer>
</article>
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="solarrust" data-slug-hash="poNZVGm" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="poNZVGm">
  <span>See the Pen <a href="https://codepen.io/solarrust/pen/poNZVGm">
  poNZVGm</a> by Alena (<a href="https://codepen.io/solarrust">@solarrust</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Как это понять

Как правило у сайта есть «шапка» и «подвал»: верхняя и нижняя части страницы. Обычно эти блоки выглядят одинаково на всех страницах. Эти разделы помогают пользователю сориентироваться и получить основную инфу о сайте.

В «подвале» мы чаще всего видим название компании, правовую информацию, ссылки на соцсети и другие контакты.

`<footer>` может быть не только у всего сайта целиком, но и у отдельного блока или секции.

## Как пишется

Тег `<footer>` парный, должен всегда закрываться `</footer>`.

## Атрибуты

Применяются все [глобальные атрибуты](/html/doka/global-attrs).

## Подсказки

💡 У `<footer>` блочные стили по умолчанию 🤓

💡 Нельзя вкладывать в `<address>`, `<header>` или другой `<footer>`.

💡 Программа чтения с экрана на маках может не читать то, что написано в `<footer>`. Чтобы исправить это, добавь атрибут `role="contentinfo"` в `<footer>`.

💡 Контакты и информацию об авторе стоит поместить в контейнер `<address>`, а его добавить в `<footer>`.

## В работе

🛠 У `<footer>` особо нет никаких хитростей. Это нижняя часть страницы: там располагаются разные эпилоги. Если это [лендинг](https://ru.wikipedia.org/wiki/%D0%A6%D0%B5%D0%BB%D0%B5%D0%B2%D0%B0%D1%8F_%D1%81%D1%82%D1%80%D0%B0%D0%BD%D0%B8%D1%86%D0%B0), там могут лежать иконки соцсетей и информация о компании. Важно выделить `<footer>`, чтобы поисковик понял, что находится в этом блоке.

{% include "authors/vladimir/author.njk" %}
