---
title: background-repeat
name: background-repeat
section: css
type: doka
tags:
 - cssDoka
 - post
article: post
---

## Кратко

Свойство `background-repeat` управляет тем, будет ли повторяться фоновое изображение. По умолчанию значение у этого свойства `repeat`. Значит фоновая картинка будет повторяться по вертикали и по горизонтали. 

## Пример

HTML

```html
<div class="element"></div>
```

CSS

```css
.element {
	height: 100vh;
	background-image: url(https://images.homedepot-static.com/productImages/3e6f74e5-e705-4f37-b2ce-e2db91463d70/svn/york-wallcoverings-wallpaper-dy0208-64_1000.jpg);
	background-size: 64px auto; /* Размер изображения */
}
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="solarrust" data-slug-hash="JzveNw" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="JzveNw">
  <span>See the Pen <a href="https://codepen.io/solarrust/pen/JzveNw">
  JzveNw</a> by Alena (<a href="https://codepen.io/solarrust">@solarrust</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Получился красивый паттерн. Изображение повторяется по горизонтали и по вертикали. 

Изменим значение по умолчанию на `repeat-x`

```css
.element {
	...
	background-repeat: repeat-x;
}
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="solarrust" data-slug-hash="VRxVWo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="VRxVWo">
  <span>See the Pen <a href="https://codepen.io/solarrust/pen/VRxVWo">
  VRxVWo</a> by Alena (<a href="https://codepen.io/solarrust">@solarrust</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Теперь картинка повторяется только горизонтали. Аналогично можно повторить картинку по вертикали при помощи значения `repeat-y`.

Но чаще всего в работе встречается значение `no-repeat`. С таким значением фоновая картинка не будет повторяться ни по горизонтали ни по вертикали. 

## Как это понять

Слово `repeat` переводится с английского как *повторение*. Дословно всё свойство можно перевести как *фон-повторение*. Если говорить по-русски, то получается повторение фона. 

## Как пишется

В качестве значения для свойства `background-repeat` пишутся следующие ключевые слова: 

- `no-repeat` — фоновое изображение не повторяется, остаётся только одно внутри элемента.
- `repeat` (значение по умолчанию) — изображение повторяется и по горизонтали и по вертикали до тех пор, пока не закроет всю площадь элемента. 
- `repeat-x` — фон повторяется по горизонтали. 
- `repeat-y` — фон повторяется по вертикали. 
- `space` — изображение повторяется до тех пор, пока не закроет весь размер элемента. При этом если по размерам не удаётся повторить изображение без обрезания, то между картинками добавляется равное пространство. Крайне редко требуется в работе.
- `round` — изображение повторяется так, чтобы закрыть весь элемент. Но картинка не обрезается, повторяется целое количество раз. Если это не удаётся, то картинки масштабируются. Крайне редко требуется в работе.

Эти ключевые слова `repeat` и `no-repeat` можно комбинировать чтобы управлять повторениями по горизонтали (первое значение) и по вертикали (второе значение). Но проще указывать специальные ключевые слова `repeat-x` и `repeat-y`.

## Подсказки

💡Свойство не наследуется.

💡Значение по умолчанию `repeat`. 

💡Чаще всего для *полноэкранных* фонов указывается значение `no-repeat`. 

💡Свойство `background-repeat` нельзя анимировать 😒

## В работе

### Алёна, front-end ниндзя
`background-repeat` — свойство простое. Написано повторять — повторяем фон. Написано не повторять — не повторяем. 

🛠Чаще всего в работе встречается значение свойства `background-repeat: no-repeat`.

🛠Повторение фона может пригодиться, если создаётся паттерн в качестве фона как в [примере]().

🛠С помощью повторения фона и линейного градиента (`linear-gradient`) можно создавать полосатые фоны.

HTML 

```html
<div class="element"></div>
```

CSS

```css
.element {
	height: 100vh;
	background-image: linear-gradient(#f1f1f1 50px, black 0); /* Линейный градиент */
	background-size: auto 100px; /* Размер фона: 50 пикселей серая полоска + 50 пикселей чёрная полоска */
	background-repeat: repeat-y; /* Повторяем фон по вертикали */
}
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="solarrust" data-slug-hash="QorzvV" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="QorzvV">
  <span>See the Pen <a href="https://codepen.io/solarrust/pen/QorzvV">
  QorzvV</a> by Alena (<a href="https://codepen.io/solarrust">@solarrust</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>