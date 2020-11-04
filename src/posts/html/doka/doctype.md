---
title: <!DOCTYPE>
name: doctype
section: html
type: doka
tags:
  - htmlDoka
  - post

autor:
co-autors:
designers:
contributors:
summary:
---

## Кратко

<code><!DOCTYPE></code>  —  это сокращение от document type или _тип документа_. <code><!DOCTYPE></code>  говорит браузеру: «Работай со страницей в стандартном режиме, плиз».

В общем, чтобы браузер узнал тип HTML-документа и правильно его открыл, просто поставьте тег <code><!DOCTYPE></code> в первой строке кода.

## Пример

Дело в том, что у HTML есть несколько версий, а также расширенные языки, вроде XHTML. Поэтому внутри вы можете увидеть вот такую дичь, которая задаёт параметры всего документа:

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "[http://www.w3.org/TR/html4/strict.dtd](http://www.w3.org/TR/html4/strict.dtd)">
```

Вот как это расшифровать:

```html
<!DOCTYPE [Элемент верхнего уровня] [Публичность] "[Регистрация]//[Организация]//[Тип] [Имя]//[Язык]" "[URL]">
```

## Как пишется

- <em>Элемент верхнего уровня</em> — указывает корневой элемент документа: для HTML это тег <em>&lt;html&gt;</em>.
- <em>Публичность</em> — есть два значения: PUBLIC (публичный) и SYSTEM (системный). Для HTML/XHTML указывается значение PUBLIC.
- <em>Регистрация</em> — сообщает, что разработчик DTD (описания шаблона документа) зарегистрирован в международной организации по стандартизации (International Organization for Standardization, ISO). Принимает одно из двух значений: плюс (+) — разработчик зарегистрирован в ISO и - (минус) — разработчик не зарегистрирован. Для W3C значение ставится (-).
- <em>Организация</em> — уникальное название организации, разработавшей DTD. Официально HTML/XHTML публикует W3C, это название и пишется в <code><!DOCTYPE></code>.
- <em>Тип</em> — тип документа. Для HTML/XHTML значение указывается DTD.
- <em>Имя</em> — уникальное имя документа для описания DTD.
- <em>Язык</em> — язык, на котором написан текст для описания объекта. Содержит две буквы, пишется в верхнем регистре. Для документа HTML/XHTML указывается английский язык (EN).
- <em>URL</em> — адрес документа с DTD.

## Типы 🤖

<table class="table">
    <tr>
        <th colspan="2">
            HTML 4.01
        </th>
    </tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">Строгий синтаксис HTML</td>
    <tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">Переходный синтаксис HTML</td>
    <tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">В HTML-документе применяются фреймы</td>
    <tr>
    <tr>
        <th colspan="2">
            HTML 5
        </th>
    </tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE html&gt;
        </code><td>
        <td class="table__item table__item_half">Для всех документов</td>
    <tr>
    <tr>
        <th colspan="2">
            XHTML 1.0
        </th>
    </tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">Строгий синтаксис XHTML</td>
    <tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">Переходный синтаксис XHTML</td>
    <tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">Документ написан на XHTML и содержит фреймы</td>
    <tr>
    <tr>
        <th colspan="2">
            XHTML 1.1
        </th>
    </tr>
    <tr>
        <td class="table__item table__item_half"><code>
            &lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd"&gt;
        </code><td>
        <td class="table__item table__item_half">Разработчики XHTML 1.1 предполагают, что он постепенно вытеснит HTML. Никакого деления на виды это определение не имеет, синтаксис один и подчиняется четким правилам.</td>
    <tr>
</table>

## В работе

<h3>Владимир, <span class="twitter">-</span></h3>

🛠 Если сравнивать HTML с устройством человека, то <code>&lt;!DOCTYPE&gt;</code> — это его вид. Важно знать, что было раньше, но не надо быть австралопитеком. Единственный вариант, который можно использовать — это <code>&lt;!DOCTYPE html&gt;</code>, все остальные устарели.

<h3>Алёна, <a href="https://twitter.com/ABatickaya" target="_blank" rel="nofollow noopener noreferrer" class="twitter">@ABatickaya</a></h3>

🛠 Программисты прошлого соревновались в том, кто может написать один из доктайпов по памяти и без ошибок.

Сейчас такого веселья уже не видать. Во-первых, доктайп <i>усох</i> <code>&lt;!DOCTYPE html&gt;</code> — сложно НЕ написать его без ошибок. А во-вторых, все разработчики используют плагин [Emmet](https://emmet.io/) для написания стандартной разметки страницы. Гораздо удобнее напечатать `!` и нажать клавишу `Tab` чем запоминать доктайп. Аналогичного результата можно добиться, набрав в файле <code>html:5</code> и нажав Tab.

Так что нужно просто знать что такой тег есть, где он должен находится в разметке и за что отвечает. Остальное сделает машина.

🛠 Некоторые особо хитрые работодатели любят спросить о доктайпе на собеседовании. Будьте готовы 😏

Вопрос обычно звучит так:

- Что делает DOCTYPE?

  <code><!DOCTYPE></code>  —  это сокращение от «document type» (тип документа). Он объявляется в HTML для того, чтобы различать стандартный режим или [режим совместимости (quirks mode)](https://quirks.spec.whatwg.org/#history). <code><!DOCTYPE></code>  говорит браузеру: «Работай со страницей в стандартном режиме, плиз».

  Мораль истории  —  просто добавляй <code>&lt;!DOCTYPE html&gt;</code> в начало страницы.
