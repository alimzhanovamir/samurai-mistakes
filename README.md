# Ошибки js самураев:

## Компонент, не компонента!!!
<br>

## No 'Access-Control-Allow-Origin'
**Текст ошибки:**
`Access to XMLHttpRequest at 'https://social-network.samuraijs.com/api/1.0/status' from origin 'http://localhost:3000' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource.`
Это означает что в у вас не правильно настроены заголовки запроса<br>

**Совет:**
Проверить свойство headers. [Дока самурайского API](https://docs.google.com/document/d/1ZSXmTzkgq_Kj1VbWuq8fTv_DPD95GFDvPZgqFeIYGoM/edit).
Почитать про CORS можно [тут](https://developer.mozilla.org/ru/docs/Web/HTTP/CORS). Так же можно установить в браузер расширение no cors отключающее блокировку.
<br><br>

## Cannot read property 'название свойства' of undefined
**Текст ошибки:** `Cannot read property 'dialogs' of undefined`</pre>`

**Пример:** <pre>const dialogs = state.dialogsPage.dialogs</pre>

Это означает что в `state` или `dialogsPage` пришло значение `undefined`. Независимо какое свойство было указано в ошибке (`map`, `length` и т.д.).<br><br>
**Совет:** Проверить переданные данные (`props`). Начать проверку с родительского компонента.ю если данные пришли с него.
<br><br>

## Undefined is not a function
**Текст ошибки:** `undefined is not a function`

**Пример:** <pre>props.setChecked(value)</pre>

Это означает что пришло значение не являющееся функцией, например `undefined`.<br><br>
**Совет:** Проверить переданные данные (`props`). Начать проверку с родительского компонента.ю если данные пришли с него.