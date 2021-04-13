---
title: "sessionStorage"
name: session-storage
author: akellbl4
summary:
  - sessionstorage
  - webstorage
  - storage
---

## Кратко

Это объект, хранящийся в `window`, который позволяет сохранять данные в браузере на время сессии. Данный тип хранилища очень похож на (`localStorage`)[/js/doka/local-storage] Представлен как хранилище данных в формате ключ-значение, т.е. при сохранении данных мы указываем имя поля, в которое должны быть сохранены данные, и далее используем это имя для их получения.

- Сессия страницы создается при открытии новой вкладки браузера и остается активной до тех пор пока не была закрыта, состояние сессии сохраняется между перезагрузками вкладки. Открыти новой вкладки с таким же адресом приводит к созданию новой сессии.
- Позволяет сохранять текстовую информацию (при попытке сохранения других типов данных они будут приведены к строке. Из этого следует, что после сохранения числа, при попытке его получить, нам вернется число, записанное в строку).
- Не имеет ограничений по времени хранения (может быть очищен пользователем вручную или браузером при переполнении автоматически).
- Максимальный объем данных ограничен размером 5MB.

## Пример

Записываем данные:

```js
window.sessionStorage.setItem("name", "Doka Dog");
```

При чтении ранее записанных данных по ключу `name` мы получим `Doka Dog`.

```js
const name = window.sessionStorage.getItem("name");
console.log(name);
```

Повторная запись по тому же ключу приведет к замене данных:

```js
window.sessionStorage.setItem("name", "Dog Doka");
const name = window.sessionStorage.getItem("name");
console.log(name);
```

## Как это понять

Если нам нужно хранить данные в течении активной сессии, то Session Storage — то, отлично подходит для этого.

## Как пишется

### Запись

Запись производит метод `setItem("ключ", "значение")`, который принимает два строковых параметра: ключ, по которому будет сохранено значение, и само значение.

```js
window.sessionStorage.setItem("name", "Doka Dog");
```

### Чтение

За чтение отвечает `getItem("ключ")` c одним параметром, который указывает на ключ для чтения и возвращает полученное значение из хранилища, если до этого значение не было записано по этому ключу, то метод вернет `null`.

```js
window.sessionStorage.getItem("name"); // вернет "Doka Dog"
window.sessionStorage.getItem("user"); // вернет `null`
```

### Удаление

Удаляет запись из хранилища `removeItem("ключ")`. Так же успешно выполнится даже, если указанного ключа не существует в хранилище.

```js
window.sessionStorage.removeItem("name");
window.sessionStorage.removeItem("user");
```

### Очистка хранилища

Метод `clear()` очищает хранилище полностью

```js
window.sessionStorage.clear();
```

### Количество полей в хранилище

Используя поле `.length` можно узнать, сколько всего полей было записано в хранилище.

```js
window.sessionStorage.length
```

### Получение ключа по индексу

Метод `key()` может получать ключ по индексу.

```js
window.sessionStorage.setItem("name", "Doka Dog");
widow.sessionStorage.key(0); // вернет "name"
```

Таким образом, используя количество ключей в хранилище и получение ключа по индексу, можно организовать перебор всех значений в хранилище.

```js
const sessionStorageSize = window.sessionStorage.length;
for (let = 0; i < sessionStorageSize; i++) {
  console.log(window.sessionStorage.getItem(sessionStorage.key(i)))
}

```

## В работе

🛠 Session Storage в реальныйх проектах используется достаточно редко, но иногда может быть достаточно полезен. Например, если мы не хотим терять данные если пользователь случайно обновил страницу.

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="js,result" data-user="akellbl4" data-slug-hash="mdRXYgj" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Session Storage Example">
  <span>See the Pen <a href="https://codepen.io/akellbl4/pen/mdRXYgj">
  Session Storage Example</a> by Pavel Mineev (<a href="https://codepen.io/akellbl4">@akellbl4</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

🛠 Иногда нам нужно сохранить не просто текст, а целую структуру данных, и в этом нам поможет `JSON.stringify`

```js
const user = {
  name: "Doka Dog",
  avatarUrl: "https://y-doka.site/assets/images/mainpage/mascot-doka.svg"
};

sessionStorage.setItem("user", JSON.stringify(user))
```

И после чтения парсим:

```js
function readUser() {
  const userJSON = sessionStorage.getItem("user")

  if (userJSON === null) {
    return undefined
  }

  // Если вдруг в хранилище оказался невалидный JSON, предохраняемся от этого
  try {
    return JSON.parse(userJSON)
  } catch (e) {
    sessionStorage.removeItem("user")
    return undefined
  }
}
```

🛠 Если ваш сайт использует скрипты аналитики или другие внешние библиотеки, то они также имеют доступ к хранилищу. Поэтому лучше именовать ключи для записи в хранилище с префиксом и в едином стиле. Например, если мы записываем что-то на этом сайте, я бы выбрал префикс `YD_{название ключа}`, так можно сгруппировать только те значения, которые нам нужны, или применить фильтр в инструментах разработчика.

🛠 Используйте функции обертки для предотвращения ошибок связанных с неудачными попытками записи, отсутствия Session Storage в браузере и дублирования кода.

```js
function getItem(key, value) {
  try {
    return window.sessionStorage.getItem(key)
  } catch (e) {
    console.log(e)
  }
}

function setItem(key, value) {
  try {
    return window.sessionStorage.getItem(key, value)
  } catch (e) {
    console.log(e)
  }
}

function setJSON(key, value) {
  try {
    const json = JSON.stringify(value)

    setItem(key, json)
  } catch (e) {
    console.error(e)
  }
}

function getJSON(key) {
  try {
    const json = getItem(key)

    return JSON.parse(json)
  } catch (e) {
    console.error(e)
  }
}
```
