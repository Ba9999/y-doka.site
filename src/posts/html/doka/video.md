---
title: <video>
name: video
section: html
type: doka
tags:
  - htmlDoka
  - post
  - video
  - <video>
  - видео
  - autoplay
  - muted
  - controls
  - source
  - buffered
  - loop
  - preload
  - poster
  -
article: post
autor:
---

## Кратко

Встраивает видео на страницу 📺

## Пример

Одно видео в двух разных форматах и текст, который появится, если оба формата не поддерживаются браузером:

```html
<video controls width="250">
  <source src="/media/examples/flower.webm" type="video/webm" />

  <source src="/media/examples/flower.mp4" type="video/mp4" />
  Ваш браузер не поддерживает встроенные видео :(
</video>
```

## Как это понять

Тег `<video>` добавляет на страницу видеоплеер, который может воспроизвести одно или несколько видео.

## Как пишется

Тег `<video>...</video>` всегда закрывается.

Адрес видео задаётся внутри контейнера `<video>` через тег `<source src="URL">` или с помощью атрибута `src`.

Некоторые браузеры могут не поддерживать какой-то формат. Поэтому в `<video>` можно добавить один и тот же файл в нескольких форматах. Это будет выглядеть так:

```html
<source src="myVideo.mp4" type="video/mp4" />
<source src="myVideo.webm" type="video/webm" />
```

На случай, если браузер не поддерживает встроенные видео, можно вставить текст или картинку — они просто добавляются в `<video>...</video>`:

```html
<video controls>
  <source src="myVideo.mp4" type="video/mp4" />
  <source src="myVideo.webm" type="video/webm" />
  <p>
    Ваш браузер не поддерживает встроенные видео. Попробуйте скачать его по
    <a href="myVideo.mp4">этой ссылке</a>.
  </p>
</video>
```

## Атрибуты

С помощью атрибутов мы можем настроить кнопки управления, зацикливание видео и другие параметры:

- `autoplay` — видео воспроизводится автоматически после загрузки страницы. Используй автопроигрывание с умом: мало кому нравится, когда что-то начинает само играть;
- `buffered` — этот атрибут собирает информацию о том, какие минуты видео уже загрузились;
- `controls` — добавляет стандартные элементы управления видеоплейером: кнопку воспроизведения и паузы, полосу прокрутки, уровень громкости, полноэкранный режим и другие элементы, в зависимости от браузера;
- `height` — высота видеоплейера в пикселях;
- `loop` — зацикливает воспроизведение видео, так что оно снова начинается каждый раз после завершения;
- `muted` — видео начнёт играть без звука, пока его не включит пользователь;
- `preload` — подсказывает браузеру, нужно ли загружать видео или информацию о нём сразу со страницей. Без этого атрибута предварительная загрузка видео будет зависеть от настроек конкретного браузера. Есть несколько значений:
- `none` — видео не загружается предварительно;
- `metadata` — загружается только информация о файле, например, размер, продолжительность или обложка. Используй этот параметр, чтобы не загружать видео, пока пользователь не захочет его посмотреть;
- `auto` — видеофайл загружается со страницей, чтобы пользователь мог сразу начать смотреть его. Если не указывать никакое значение `preload`, то атрибут будет работать как `auto`. Учти, что если стоит атрибут `autoplay`, то `preload` не работает.
- `playsinline` — указывает браузеру, чтобы тот воспроизводил видео в рамках элемента `<video>` на странице;
- `poster` — URL-адрес картинки, которая будет показываться, пока видео не загрузится. По сути, это обложка ролика. Если её не будет, то на месте видео пользователь увидит чёрный экран, пока не загрузится первый кадр;
- `src` — URL-адрес видео. Его ещё можно задать через тег `<source>`;
- `width` — ширина видео в пикселях.

## Подсказки

💡 Если не указать атрибут `controls`, то браузер не будет показывать стандартные элементы управления видеоплейером. Создать свои элементы управления можно с помощью JavaScript.

💡 Используй CSS-свойство `object-position`, чтобы настроить расположение видео внутри элемента, а также `object-fit`, чтобы настроить размер видео относительно элемента.

💡 Атрибут `preload` носит рекомендательный характер для браузера: будет ли видео предварительно загружено, зависит от настроек конкретного браузера.

💡 Высоту `height` и ширину `width` видеоплейера лучше задавать через CSS-стили. По умолчанию эти параметры будут такими, как у видео, которое ты встраиваешь.

## Ещё пример

Вот простой пример, где у видео есть обложка `poster`, которую покажут сразу, и текст на случай, если видео не загрузится.

HTML

```html
<video
  controls
  src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
  width="580"
>
  Простите, но ваш браузер не поддерживает встроенные видео. Попробуйте скачать
  его <a href="https://archive.org/details/BigBuckBunny_124">по этой ссылке</a>
  и открыть его на своём устройстве.
</video>
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="max-grachev" data-slug-hash="QREJgQ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;video&amp;gt; example 1">
  <span>See the Pen <a href="https://codepen.io/max-grachev/pen/QREJgQ">
  &lt;video&gt; example 1</a> by Max Grachev (<a href="https://codepen.io/max-grachev">@max-grachev</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

А теперь добавим несколько форматов одного видео. Браузер попробует воспроизвести первый из поддерживаемых им форматов: сначала попробует проиграть mp4, потом ogg, затем avi. Если встраиваемые видео вообще не поддерживаются, то появится соответствующее сообщение:

HTML

```html
<video
  width="580"
  controls
  poster="https://m.media-amazon.com/images/M/MV5BODU0NmViMDEtODEyZi00MjgyLWI4ZjktNzk0NmRiYjQwZDY0XkEyXkFqcGdeQXVyNTc0NjY1ODk@._V1_.jpg"
>
  <source
    src="https://archive.org/download/ElephantsDream/ed_1024_512kb.mp4"
    type="video/mp4"
  />
  <source
    src="https://archive.org/download/ElephantsDream/ed_hd.ogv"
    type="video/ogg"
  />
  <source
    src="https://archive.org/download/ElephantsDream/ed_hd.avi"
    type="video/avi"
  />
  Ваш браузер не поддерживает встроенные видео.
</video>
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="max-grachev" data-slug-hash="vwKQJG" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;video&amp;gt; example 2">
  <span>See the Pen <a href="https://codepen.io/max-grachev/pen/vwKQJG">
  &lt;video&gt; example 2</a> by Max Grachev (<a href="https://codepen.io/max-grachev">@max-grachev</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## В работе

🛠 На некоторых сайтах можно встретить фоновое видео вместо статичной картинки. Выглядит круто, а делается очень просто:

HTML

```html
<video autoplay muted loop class="background-video">
  <source src="http://epic.spb.ru/biostorm2.av1.mkv" type="video/mp4" />
</video>
<div class="content">
  <h1>Heading</h1>
  <p>Lorem ipsum...</p>
</div>
```

CSS

```css
.background-video {
  position: absolute;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
}

.content {
  position: absolute;
  top: 0;
  bottom: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: rgba(0, 0, 0, 0.5);
  color: #f1f1f1;
  width: 100%;
  padding: 20px;
}
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="solarrust" data-slug-hash="arWgPV" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="arWgPV">
  <span>See the Pen <a href="https://codepen.io/solarrust/pen/arWgPV">
  arWgPV</a> by Alena (<a href="https://codepen.io/solarrust">@solarrust</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

🛠 Обрати внимание на пару важных моментов, чтобы видео работало:

1. Используй для фонового видео форматы AV1 или WebM. Это современные форматы кодирования, которые позволяют экономить на размере видео. Это ускорит загрузку страницы и причинит меньше раздражения пользователю. Проверяй поддержку форматов на сайте [caniuse.com](https://caniuse.com/)

2. Чтобы не надоедать пользователю навязчивыми рекламными роликами, браузеры придерживаются политики, что в автоматическом режиме могут проигрываться только видео с атрибутом `mute`. Обязательно добавь этот атрибут для фонового видео.

<h3>Владимир, <span class="twitter">-</span></h3>

🛠 Не забывай добавлять хотя бы два дублирующих видео в формате webm и mp4. Фишка в том, что webm очень круто сжимает ролики, и если браузер поддерживает формат, то видео загрузится сильно быстрее и не сожрёт трафик. Ну а если ты юзаешь Internet Explorer или Safari, то откроется обычный mp4 и сработает как обычно.
