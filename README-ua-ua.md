# Шо за прутня JavaScript?

[![WTFPL 2.0][license-image]][license-url]
[![NPM version][npm-image]][npm-url]

> Список веселих та хитромудрих прикладів з JavaScript

JavaScript - чудова мова. Вона має простий синтаксис, велику екосистему і, що найголовніше, велику спільноту.

У той же час ми всі знаємо, що JavaScript - це досить весела мова з підступними моментами. Деякі з них можуть швидко перетворити нашу повсякденну роботу в пекло, а деякі з них можуть нас розсмішити.

Оригінальна ідея для WTFJS належить [Brian Leroux](https://twitter.com/brianleroux).
Цей список натхненний його виступами [**“WTFJS”** at dotJS 2012](https://www.youtube.com/watch?v=et8xNAc2ic8):

[![dotJS 2012 - Brian Leroux - WTFJS](https://img.youtube.com/vi/et8xNAc2ic8/0.jpg)](https://www.youtube.com/watch?v=et8xNAc2ic8)

# Node Packaged Manuscript

Ви можете встановити цей довідник за допомогою `npm`. Запустіть:

```
$ npm install -g wtfjs
```

Тепер ви можете запусти `wtfjs` в command line
Ви повинні мати змогу запустити `wtfjs` at the command line now. Це відкриє посібник у вибраному вами `$PAGER`. В іншому випадку ви можете продовжувати читати далі.

Джерело доступне тут: <https://github.com/denysdovhan/wtfjs>

# Переклади

Поки що існують такі переклади **wtfjs**:

- [中文版](./README-zh-cn.md)
- [Français](./README-fr-fr.md)
- [Português do Brasil](./README-pt-br.md)
- [Polski](./README-pl-pl.md)
- [Українська](./README-ua-ua.md)

[**Запит на інший переклад**][tr-request]

[tr-request]: https://github.com/denysdovhan/wtfjs/issues/new?title=Translation%20Request:%20%5BPlease%20enter%20language%20here%5D&body=I%20am%20able%20to%20translate%20this%20language%20%5Byes/no%5D

<!-- prettier-ignore-start -->
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
# Зміст

- [💪🏻 Мотивація](#-motivation)
- [✍🏻 Примітки](#-notation)
- [👀 Приклади](#-examples)
  - [`[]`є рівним `![]`](#-is-equal-)
  - [`true` не є рівним `![]`, але не рівний `[]` також](#true-is-not-equal--but-not-equal--too)
  - [true є false](#true-is-false)
  - [baNaNa](#banana)
  - [`NaN` не є `NaN`](#nan-is-not-a-nan)
  - [Це фейл](#its-a-fail)
  - [`[]` є правдивим, але не `true`](#-is-truthy-but-not-true)
  - [`null` є хибним, але не `false`](#null-is-falsy-but-not-false)
  - [`document.all` є об'єктом, але він є undefined](#documentall-is-an-object-but-it-is-undefined)
  - [Мінімальне значення більше нуля](#minimal-value-is-greater-than-zero)
  - [Функція не є функцією](#function-is-not-a-function)
  - [Додавання масивів](#adding-arrays)
  - [Кінцеві коми](#trailing-commas-in-array)
  - [Рівність масивів - це чудовисько](#array-equality-is-a-monster)
  - [`undefined` і `Number`](#undefined-and-number)
  - [`parseInt` - поганий хлопець](#parseint-is-a-bad-guy)
  - [Обчислення з 'true' і 'false'](#math-with-true-and-false)
  - [Коментарі HTML дійсні в JavaScript](#html-comments-are-valid-in-javascript)
  - [`NaN` ~~не~~ є числом](#nan-is-not-a-number)
  - [`[]` і `null` - це об'єкти](#-and-null-are-objects)
  - [Чарівним способом збільшується кількість](#magically-increasing-numbers)
  - [Точність `0,1 + 0,2`](#precision-of-01--02)
  - [Виправлення чисел](#patching-numbers)
  - [Порівняння трьох чисел](#comparison-of-three-numbers)
  - [Кумедні обчислення](#funny-math)
  - [Додавання RegExps](#addition-of-regexps)
  - [Строки не є екземплярами `String`](#strings-arent-instances-of-string)
  - [Calling functions with backticks](#calling-functions-with-backticks)
  - [Call call call](#call-call-call)
  - [A `constructor` property](#a-constructor-property)
  - [Object as a key of object's property](#object-as-a-key-of-objects-property)
  - [Accessing prototypes with `__proto__`](#accessing-prototypes-with-__proto__)
  - [`` `${{Object}}` ``](#-object-)
  - [Destructuring with default values](#destructuring-with-default-values)
  - [Dots and spreading](#dots-and-spreading)
  - [Labels](#labels)
  - [Nested labels](#nested-labels)
  - [Insidious `try..catch`](#insidious-trycatch)
  - [Is this multiple inheritance?](#is-this-multiple-inheritance)
  - [A generator which yields itself](#a-generator-which-yields-itself)
  - [A class of class](#a-class-of-class)
  - [Non-coercible objects](#non-coercible-objects)
  - [Tricky arrow functions](#tricky-arrow-functions)
  - [Arrow functions can not be a constructor](#arrow-functions-can-not-be-a-constructor)
  - [`arguments` and arrow functions](#arguments-and-arrow-functions)
  - [Tricky return](#tricky-return)
  - [Chaining assignments on object](#chaining-assignments-on-object)
  - [Accessing object properties with arrays](#accessing-object-properties-with-arrays)
  - [Null and Relational Operators](#null-and-relational-operators)
  - [`Number.toFixed()` display different numbers](#numbertofixed-display-different-numbers)
  - [`Math.max()` less than `Math.min()`](#mathmax-less-than-mathmin)
  - [Comparing `null` to `0`](#comparing-null-to-0)
  - [Same variable redeclaration](#same-variable-redeclaration)
  - [Default behavior Array.prototype.sort()](#default-behavior-arrayprototypesort)
  - [resolve() won't return Promise instance](#resolve-wont-return-promise-instance)
- [📚 Other resources](#-other-resources)
- [🎓 License](#-license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->
<!-- prettier-ignore-end -->

# 💪🏻 Motivation

> Задля розваги
>
> &mdash; _[**“Just for Fun: The Story of an Accidental Revolutionary”**](https://en.wikipedia.org/wiki/Just_for_Fun), Linus Torvalds_

Основна мета цього списку - зібрати кілька божевільних прикладів і пояснити, як вони працюють, якщо це можливо. Просто тому, що цікаво дізнатися щось нове.

Якщо ви новачок, ви можете скористатися цими нотатками, щоб глибше зануритися в JavaScript. Сподіваюся, ці нотатки змотивують вас витратити більше часу на читання специфікації.

Якщо ви професійний розробник, ви можете розглянути ці приклади як чудове посилання на всі химерності та неочікувані винятки нашого улюбленого JavaScript.

У будь-якому випадку, просто прочитайте це. Ви, мабуть, знайдете щось нове.

# ✍🏻 Примітки

**`// ->`** використовується для відображення результату виразу. Наприклад:

```js
1 + 1; // -> 2
```

**`// >`** означає результат `console.log` або інший результат. Наприклад:

```js
console.log("hello, world!"); // > hello, world!
```

**`//`** це просто коментар, що використовується для пояснень. Приклад:

```js
// Assigning a function to foo constant
const foo = function () {};
```

# 👀 Приклади

## `[]` is equal `![]`

Масив дорівнює не масиву:

```js
[] == ![]; // -> true
```

### 💡 Пояснення:

Оператор абстрактної рівності перетворює обидві сторони на числа, щоб порівняти їх, і обидві сторони стають числом "0" з різних причин. Масиви є істинними, тож праворуч, протилежним до істинного значення є `false ', яке потім перетворене до` 0'. Однак ліворуч порожній масив перетворений до числа, не стаючи спочатку булевим, а порожні масиви перетворені до "0", незважаючи на неправдивість.

Ось як цей вираз спрощує:

```js
+[] == +![];
0 == +false;
0 == 0;
true;
```

Дивіться також [`[]` є правдивим, але не `true`](#-is-truthy-but-not-true).

- [**12.5.9** Logical NOT Operator (`!`)](https://www.ecma-international.org/ecma-262/#sec-logical-not-operator)
- [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

## `true` не є рівним `![]`, але не рівний `[]` також

Масив не дорівнює `true`, але не Array не дорівнює` true`;
Масив дорівнює `false`, не Array також дорівнює` false`:

```js
true == []; // -> false
true == ![]; // -> false

false == []; // -> true
false == ![]; // -> true
```

### 💡 Пояснення:

```js
true == []; // -> false
true == ![]; // -> false

// Відповідно до специфікації

true == []; // -> false

toNumber(true); // -> 1
toNumber([]); // -> 0

1 == 0; // -> false

true == ![]; // -> false

![]; // -> false

true == false; // -> false
```

```js
false == []; // -> true
false == ![]; // -> true

// Відповідно до специфікації

false == []; // -> true

toNumber(false); // -> 0
toNumber([]); // -> 0

0 == 0; // -> true

false == ![]; // -> true

![]; // -> false

false == false; // -> true
```

- [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

## true є false

```js
!!"false" == !!"true"; // -> true
!!"false" === !!"true"; // -> true
```

### 💡 Пояснення:

Розглянемо це крок за кроком:

```js
// true - це `правдиво' і представлене значенням 1 (число), `true ' у формі строки - NaN.
true == "true"; // -> false
false == "false"; // -> false

// 'false' - це не порожня строка, тому це правдиве значення
!!"false"; // -> true
!!"true"; // -> true
```

- [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

## baNaNa

```js
"b" + "a" + +"a" + "a"; // -> 'baNaNa'
```

Це жарт старої школи в JavaScript, але перероблений. Ось оригінальний:

```js
"foo" + +"bar"; // -> 'fooNaN'
```

### 💡 Пояснення:

Вираз обчислюється як ``foo '+ (+' bar ')`, що перетворює' bar 'у не число.

- [**12.8.3** The Addition Operator (`+`)](https://www.ecma-international.org/ecma-262/#sec-addition-operator-plus)
- [12.5.6 Unary + Operator](https://www.ecma-international.org/ecma-262/#sec-unary-plus-operator)

## `NaN` не є `NaN`

```js
NaN === NaN; // -> false
```

### 💡 Пояснення:

Специфікація чітко визначає логіку такої поведінки:

> 1. Якщо `Type (x)` відрізняється від `Type (y)`, поверніть **false**.
> 2. Якщо `Type (x)` має значення Number, тоді
>    1. Якщо `x` - ** NaN **, поверніть ** false **.
>    2. Якщо `y` - ** NaN **, поверніть ** false **.
>    3. … … …
>
> &mdash; [**7.2.14** Strict Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-strict-equality-comparison)

Дотримуючись визначення `NaN` з IEEE:

> Можливі чотири взаємовиключні відносини: менше, рівне, більше і невпорядковане. Останній випадок виникає, коли принаймні одним операндом є NaN. Кожен NaN повинен порівнювати не впорядковане з усіма, включаючи самого себе.
>
> &mdash; [“What is the rationale for all comparisons returning false for IEEE754 NaN values?”](https://stackoverflow.com/questions/1565164/1573715#1573715) на StackOverflow

## Це "фейл"

Ви б не повірили, але …

```js
(![] + [])[+[]] +
  (![] + [])[+!+[]] +
  ([![]] + [][[]])[+!+[] + [+[]]] +
  (![] + [])[!+[] + !+[]];
// -> 'fail'
```

### 💡 Пояснення:

Розбиваючи цю масу символів на частини, ми помічаємо, що часто трапляється такий шаблон:

```js
![] + []; // -> 'false'
![]; // -> false
```

Тому ми намагаємось додати `[]` до `false`. Але через низку викликів внутрішніх функцій (`binary + Operator` ->` ToPrimitive` -> `[[DefaultValue]]`) ми в підсумку перетворюємо правий операнд у рядок:

```js
![] + [].toString(); // 'false'
```

Думаючи про рядок як про масив, ми можемо отримати доступ до його першого символу через `[0]`:

```js
"false"[0]; // -> 'f'
```

Решта очевидно, але `i` хитре. Значення `i` в` fail` захоплюється шляхом генерування рядка `` falseundefined` та захоплення елемента за індексом `['10']`

## `[]` правдиве, але не `true`

Масив - це правдиве значення, однак воно не дорівнює `true`.

```js
!![]       // -> true
[] == true // -> false
```

### 💡 Пояснення:

Ось посилання на відповідні розділи в специфікації ECMA-262:

- [**12.5.9** Logical NOT Operator (`!`)](https://www.ecma-international.org/ecma-262/#sec-logical-not-operator)
- [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

## `null` є хибне, але не `false`

Незважаючи на те, що `null` - це хибне значення, воно не дорівнює` false '.

```js
!!null; // -> false
null == false; // -> false
```

У той же час інші хибні значення, наприклад, `0` або `''`, дорівнюють `false`.

```js
0 == false; // -> true
"" == false; // -> true
```

### 💡 Пояснення:

Пояснення таке ж, як і в попередньому прикладі. Ось відповідне посилання:

- [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

## `document.all` є об’єктом, але він є undefined

> ⚠️ Це частина браузерного API і не буде працювати в середовищі Node.js ⚠️

Незважаючи на те, що `document.all` є подібним до масиву об'єктом і надає доступ до DOM-вузлів на сторінці, він реагує на функцію` typeof` як `undefined`.

```js
document.all instanceof Object; // -> true
typeof document.all; // -> 'undefined'
```

У той же час, `document.all` не дорівнює` undefined`.

```js
document.all === undefined; // -> false
document.all === null; // -> false
```

Але в той же час:

```js
document.all == null; // -> true
```

### 💡 Пояснення:

> `document.all` раніше був способом доступу до елементів DOM, зокрема зі старими версіями IE. Хоча це ніколи не було стандартом, воно широко використовувалось у старовинному коді JS. Коли стандарт прогресував із новими API (наприклад, `document.getElementById`), цей виклик API застарів, і комітет стандарту повинен був вирішити, що з ним робити. Через його широке використання вони вирішили зберегти API, але ввести навмисне порушення специфікації JavaScript.

> Причина, по якій він відповідає на `false` при використанні [Strict Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-strict-equality-comparison) з `undefined`, а `true` при використанні [Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison) пов’язано з навмисним порушенням специфікації, яка прямо це дозволяє.
>
> &mdash; [“Obsolete features - document.all”](https://html.spec.whatwg.org/multipage/obsolete.html#dom-document-all) at WhatWG - HTML spec
> &mdash; [“Chapter 4 - ToBoolean - Falsy values”](https://github.com/getify/You-Dont-Know-JS/blob/0d79079b61dad953bbfde817a5893a49f7e889fb/types%20%26%20grammar/ch4.md#falsy-objects) at YDKJS - Types & Grammar

## Мінімальне значення більше нуля

`Number.MIN_VALUE` - найменше число, яке більше нуля:

```js
Number.MIN_VALUE > 0; // -> true
```

### 💡 Пояснення:

> `Number.MIN_VALUE` дорівнює` 5e-324`, тобто найменше додатне число, яке може бути представлене в точності з плаваючою точкою, тобто це максимально близько, наскільки ви можете наблизитись до нуля. Він визначає найкращу роздільну здатність, яку вам можуть дати плаваючі числа.
>
> У даний моменті загальним найменшим значенням є `Number.NEGATIVE_INFINITY`, хоча насправді воно не є числовим у "strict" сенсі.
>
> &mdash; [“Why is `0` less than `Number.MIN_VALUE` in JavaScript?”](https://stackoverflow.com/questions/26614728/why-is-0-less-than-number-min-value-in-javascript) at StackOverflow

- [**20.1.2.9** Number.MIN_VALUE](https://www.ecma-international.org/ecma-262/#sec-number.min_value)

## Функція не є функцією

> ⚠️ Помилка, наявна у V8 v5.5 або нижче (Node.js <= 7) ⚠️

Всі ви знаєте про надокучливий _undefined не є функцією_, а що на рахунок цього?

```js
// Declare a class which extends null
class Foo extends null {}
// -> [Function: Foo]

new Foo() instanceof null;
// > TypeError: function is not a function
// >     at … … …
```

### 💡 Пояснення:

Це не є частиною специфікації. Це лише помилка, яку зараз виправлено, тому в майбутньому з нею не повинно бути проблем.

## Додавання масивів

Що буде, якщо спробувати додати два масиви?

```js
[1, 2, 3] + [4, 5, 6]; // -> '1,2,34,5,6'
```

### 💡 Пояснення:

Відбудеться конкатенація. Покроково це виглядає так:

```js
[1, 2, 3] +
  [4, 5, 6][
    // call toString()
    (1, 2, 3)
  ].toString() +
  [4, 5, 6].toString();
// concatenation
"1,2,3" + "4,5,6";
// ->
("1,2,34,5,6");
```

## Кінцеві коми

Ви створили масив із 4 порожніми елементами. Незважаючи на все, ви отримаєте масив із трьома елементами через коми, що замикаються:

```js
let a = [, , ,];
a.length; // -> 3
a.toString(); // -> ',,'
```

### 💡 Пояснення:

> **Кінцеві коми** (іноді їх називають "заключними комами") можуть бути корисними для додавання нових елементів, параметрів чи властивостей у коді JavaScript. Якщо ви хочете додати нову властивість, ви можете просто додати новий рядок, не змінюючи перед цим попередній рядок, якщо цей рядок вже використовує кінцеву кому. Це робить контроль версій зрозумілішим, а редагування коду може бути менш проблемним.
>
> &mdash; [Кінцеві коми](https://developer.mozilla.org/uk/docs/Web/JavaScript/Reference/Trailing_commas) at MDN

## Рівність масивів - це чудовисько в JS

Рівність масивів - це чудовисько в JS, як ви можете бачити нижче:

```js
[] == ''   // -> true
[] == 0    // -> true
[''] == '' // -> true
[0] == 0   // -> true
[0] == ''  // -> false
[''] == 0  // -> true

[null] == ''      // true
[null] == 0       // true
[undefined] == '' // true
[undefined] == 0  // true

[[]] == 0  // true
[[]] == '' // true

[[[[[[]]]]]] == '' // true
[[[[[[]]]]]] == 0  // true

[[[[[[ null ]]]]]] == 0  // true
[[[[[[ null ]]]]]] == '' // true

[[[[[[ undefined ]]]]]] == 0  // true
[[[[[[ undefined ]]]]]] == '' // true
```

### 💡 Пояснення:

Слід уважно стежити за наведеними вище прикладами! Поведінка описана в розділі [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison) специфікації.

## `undefined` і `Number`

Якщо ми не передамо жодного аргументу в конструктор `Number`, ми отримаємо` 0`. Значення `undefined` присвоюється формальним аргументам, коли відсутні фактичні аргументи, тому ви можете очікувати, що `Number` без аргументів бере значення `undefined` як значення свого параметра. Однак, коли ми передаємо `undefined`, ми отримаємо `NaN`.

```js
Number(); // -> 0
Number(undefined); // -> NaN
```

### 💡 Пояснення:

Відповідно до специфікації:

1. Якщо до виклику цієї функції не було передано жодного аргументу, нехай `n` буде `+0`.
2. В іншому випадку нехай буде `n`? `ToNumber (значення)`.
3. У разі `undefined`,`ToNumber (undefined)`повинен повернути` NaN`.

Ось відповідний розділ:

- [**20.1.1** The Number Constructor](https://www.ecma-international.org/ecma-262/#sec-number-constructor)
- [**7.1.3** ToNumber(`argument`)](https://www.ecma-international.org/ecma-262/#sec-tonumber)

## `parseInt` - поганий хлопець

`parseInt` відомий своїми химерностями:

```js
parseInt("f*ck"); // -> NaN
parseInt("f*ck", 16); // -> 15
```

**💡 Пояснення:** Це трапляється тому, що `parseInt` буде продовжувати синтаксичний розбір символів за символом, поки не потрапить на символ, він не знає. `f` у `'f*ck'` - шістнадцяткова цифра `15`.

Розбір `Infinity` до цілого числа - це щось ...

```js
//
parseInt("Infinity", 10); // -> NaN
// ...
parseInt("Infinity", 18); // -> NaN...
parseInt("Infinity", 19); // -> 18
// ...
parseInt("Infinity", 23); // -> 18...
parseInt("Infinity", 24); // -> 151176378
// ...
parseInt("Infinity", 29); // -> 385849803
parseInt("Infinity", 30); // -> 13693557269
// ...
parseInt("Infinity", 34); // -> 28872273981
parseInt("Infinity", 35); // -> 1201203301724
parseInt("Infinity", 36); // -> 1461559270678...
parseInt("Infinity", 37); // -> NaN
```

Будьте обережні з розбором `null`:

```js
parseInt(null, 24); // -> 23
```

**💡 Пояснення:**

> Це перетворення `null` у рядок` null` та спроба перетворити його. Для коріньів від 0 до 23 немає цифр, які він може перетворити, тому він повертає NaN. На 24, до системи числення додається `"n"`, 14-та буква. У 31 додається `"u"`, 21-а буква, і весь рядок може бути декодований. На 37 далі не існує жодного дійсного набору цифр, який можна створити і повернути `NaN`.

> &mdash; [“parseInt(null, 24) === 23… wait, what?”](https://stackoverflow.com/questions/6459758/parseintnull-24-23-wait-what) at StackOverflow

Не забувайте про вісімкові числа:

```js
parseInt("06"); // 6
parseInt("08"); // 8 if support ECMAScript 5
parseInt("08"); // 0 if not support ECMAScript 5
```

**💡 Пояснення:** Якщо вхідний рядок починається з "0", корінь дорівнює восьми (вісімковій) або 10 (десятковий). Вибраний корінь залежить від реалізації. ECMAScript 5 визначає, що використовується 10 (десятковий), але ще не всі браузери мають підтримку. З цієї причини завжди вказуйте корінь при використанні `parseInt`.

`parseInt` завжди перетворюйте вхідні дані у строку:

```js
parseInt({ toString: () => 2, valueOf: () => 1 }); // -> 2
Number({ toString: () => 2, valueOf: () => 1 }); // -> 1
```

Будьте обережні під час розбору значень із плаваючою комою

```js
parseInt(0.000001); // -> 0
parseInt(0.0000001); // -> 1
parseInt(1 / 1999999); // -> 5
```

**💡 Пояснення:** `ParseInt` приймає аргумент рядка і повертає ціле число вказаного кореня. `ParseInt` також знімає будь-що після включення першої нецифрової цифри в параметр строки. `0,000001` перетворюється на рядок" `"0,000001"`, а `parseInt` повертає `0`. Коли значення `0,0000001` перетворюється на строку, воно розглядається як`"1e-7"`, а отже,` parseInt` повертає `1`. `1 / 1999999` інтерпретується як `5.00000250000125e-7` і `parseInt` повертає `5`.

## Обчислення з 'true' і 'false'

Давайте порахуємо:

```js
true -
  true +
  // -> 2
  (true + true) * (true + true) -
  true; // -> 3
```

Хммммм… 🤔

### 💡 Пояснення:

Ми можемо перетворити значення до чисел за допомогою конструктора `Number`. Цілком очевидно, що значення `true` буде примусово периведене до `1`:

```js
Number(true); // -> 1
```

Одинарний оператор плюс намагається перетворити його значення в число. Він може перетворювати строкові подання цілих чисел і плаваючих значень, а також не строкові значення `true`,`false` та `null`. Якщо він не може проаналізувати певне значення, він оцінить значення `NaN`. Це означає, що ми можемо простіше перетворити `true` до `1`:

```js
+true; // -> 1
```

Коли ви виконуєте додавання або множення, використовується метод `ToNumber`. Відповідно до специфікації, цей метод повертає:

> Якщо `аргумент` є **true**, поверни **1**. Якщо `аргумент` є **false**, поверни **+0**.

Ось чому ми можемо додати булеві значення як звичайні числа і отримати правильні результати.

Відповідні розділи:

- [**12.5.6** Unary `+` Operator](https://www.ecma-international.org/ecma-262/#sec-unary-plus-operator)
- [**12.8.3** The Addition Operator (`+`)](https://www.ecma-international.org/ecma-262/#sec-addition-operator-plus)
- [**7.1.3** ToNumber(`argument`)](https://www.ecma-international.org/ecma-262/#sec-tonumber)

## Коментарі HTML дійсні в JavaScript

Ви будете вражені, але `<! -` (що називається коментарем HTML) є дійсним коментарем у JavaScript.

```js
// valid comment
<!-- також дійсний коментар
```

### 💡 Пояснення:

Вражені? Коментарі, подібні до HTML, мали на меті дозволити браузерам, які не розуміли тег `<script>`, витончено деградувати. Ці браузери, напр. Netscape 1.x більше не популярниі. Тож насправді більше немає сенсу розміщувати коментарі HTML у тегах скриптів.

Оскільки Node.js базується на механізмі V8, HTML-подібні коментарі також підтримуються середовищем виконання Node.js. Більше того, вони є частиною специфікації:

- [**B.1.3** HTML-like Comments](https://www.ecma-international.org/ecma-262/#sec-html-like-comments)

## `NaN` ~~не~~ є числом

Тип `NaN` - це` `число '':

```js
typeof NaN; // -> 'number'
```

### 💡 Пояснення:

Як працюють оператори `typeof` та` instanceof`:

- [**12.5.5** The `typeof` Operator](https://www.ecma-international.org/ecma-262/#sec-typeof-operator)
- [**12.10.4** Runtime Semantics: InstanceofOperator(`O`,`C`)](https://www.ecma-international.org/ecma-262/#sec-instanceofoperator)

## `[]` і `null` - це об'єкти

```js
typeof []; // -> 'object'
typeof null; // -> 'object'

// however
null instanceof Object; // false
```

### 💡 Пояснення:

Поведінка оператора `typeof` визначена в цьому розділі специфікації:

- [**12.5.5** The `typeof` Operator](https://www.ecma-international.org/ecma-262/#sec-typeof-operator)

Відповідно до специфікації, оператор `typeof` повертає строку відповідно до [Table 35: `typeof` Operator Results](https://www.ecma-international.org/ecma-262/#table-35). Для `null`, звичайних, стандартних екзотичних та нестандартних екзотичних об'єктів, які не реалізують`[[Call]]`, він повертає строку `"object "`.

Однак ви можете перевірити тип об'єкта, використовуючи метод `toString`.

```js
Object.prototype.toString.call([]);
// -> '[object Array]'

Object.prototype.toString.call(new Date());
// -> '[object Date]'

Object.prototype.toString.call(null);
// -> '[object Null]'
```

## Чарівним способом збільшується кількість

```js
999999999999999; // -> 999999999999999
9999999999999999; // -> 10000000000000000

10000000000000000; // -> 10000000000000000
10000000000000000 + 1; // -> 10000000000000000
10000000000000000 + 1.1; // -> 10000000000000002
```

### 💡 Пояснення:

Це спричинено стандартом IEEE 754-2008 для двійкової арифметики з плаваючою крапкою. У цьому масштабі він округляється до найближчого парного числа. Детальніше:

- [**6.1.6** The Number Type](https://www.ecma-international.org/ecma-262/#sec-ecmascript-language-types-number-type)
- [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) on Wikipedia

## Точність `0,1 + 0,2`

Загальновідомий "прикол". Додавання `0,1` та` 0,2` є супер точним:

```js
0.1 +
  0.2(
    // -> 0.30000000000000004
    0.1 + 0.2
  ) ===
  0.3; // -> false
```

### 💡 Пояснення:

Відповідь на [”Is floating point math broken?”](https://stackoverflow.com/questions/588004/is-floating-point-math-broken) питання на StackOverflow:

> Константи `0,2` та `0,3` у вашій програмі також будуть наближеними до їх справжніх значень. Трапляється, що найближче до `0.2` значення `double` перевищує раціональне число `0.2`, але найближче `double` до `0,3` менше раціонального числа `0,3`. Сума `0,1` і `0,2` перетворюється на більшу, ніж раціональне число `0,3`, і, отже, не погоджується з константою у вашому коді.

Ця проблема настільки відома, що існує навіть веб-сайт під назвою [0.30000000000000004.com](http://0.30000000000000004.com/). Це відбувається у кожній мові, яка використовує обчислення з плаваючою комою, а не лише у JavaScript.

## Виправлення чисел

Ви можете додати власні методи до обгорткових об'єктів, таких як `Number` або `String`.

```js
Number.prototype.isOne = function () {
  return Number(this) === 1;
};

(1.0).isOne(); // -> true
(1).isOne(); // -> true
(2.0)
  .isOne()(
    // -> false
    7
  )
  .isOne(); // -> false
```

### 💡 Пояснення:

Obviously, you can extend the `Number` object like any other object in JavaScript. However, it's not recommended if the behavior of the defined method is not a part of the specification. Here is the list of `Number`'s properties:

Очевидно, що ви можете розширити об'єкт `Number` як будь-який інший об'єкт у JavaScript. Однак це не рекомендується, якщо поведінка визначеного методу не є частиною специфікації. Ось список властивостей `Number`:

- [**20.1** Number Objects](https://www.ecma-international.org/ecma-262/#sec-number-objects)

## Порівняння трьох чисел

```js
1 < 2 < 3; // -> true
3 > 2 > 1; // -> false
```

### 💡 Пояснення:

Чому це так працює? Ну, проблема в першій частині виразу. Ось як це працює:

```js
1 < 2 < 3; // 1 < 2 -> true
true < 3; // true -> 1
1 < 3; // -> true

3 > 2 > 1; // 3 > 2 -> true
true > 1; // true -> 1
1 > 1; // -> false
```

Ми можемо це виправити за допомогою оператора _Оператор більше чи дорівнює (`>=`)_:

```js
3 > 2 >= 1; // true
```

Детальніше про реляційні оператори читайте у специфікації:

- [**12.10** Relational Operators](https://www.ecma-international.org/ecma-262/#sec-relational-operators)

## Кумедні обчислення

Часто результати арифметичних операцій у JavaScript можуть бути зовсім несподіваними. Розглянемо ці приклади:

```js
 3  - 1  // -> 2
 3  + 1  // -> 4
'3' - 1  // -> 2
'3' + 1  // -> '31'

'' + '' // -> ''
[] + [] // -> ''
{} + [] // -> 0
[] + {} // -> '[object Object]'
{} + {} // -> '[object Object][object Object]'

'222' - -'111' // -> 333

[4] * [4]       // -> 16
[] * []         // -> 0
[4, 4] * [4, 4] // NaN
```

### 💡 Пояснення:

Що відбувається в перших чотирьох прикладах? Ось невелика таблиця, щоб зрозуміти додавання в JavaScript:

```
Number  + Number  -> addition
Boolean + Number  -> addition
Boolean + Boolean -> addition
Number  + String  -> concatenation
String  + Boolean -> concatenation
String  + String  -> concatenation
```

А як щодо інших прикладів? Методи `ToPrimitive` та `ToString` неявно викликаються для `[]` і `{}`перед додаванням. Детальніше читайте у специфікації:

- [**12.8.3** The Addition Operator (`+`)](https://www.ecma-international.org/ecma-262/#sec-addition-operator-plus)
- [**7.1.1** ToPrimitive(`input` [,`PreferredType`])](https://www.ecma-international.org/ecma-262/#sec-toprimitive)
- [**7.1.12** ToString(`argument`)](https://www.ecma-international.org/ecma-262/#sec-tostring)

Notably, `{} + []` here is the exception. The reason why it differs from `[] + {}` is that, without parenthesis, it is interpreted as a code block and then a unary +, converting `[]` into a number. It sees the following:

Примітно, що `{} + []` тут є винятком. Причина, по якій він відрізняється від `[] + {}`, полягає в тому, що без дужок він інтерпретується як блок коду, а потім одинарний +, перетворюючи `[]` у число. Він бачить наступне:

```js
{
  // a code block here
}
+[]; // -> 0
```

Щоб отримати такий самий результат, як `[] + {}`, ми можемо обернути його в дужки.

```js
({} + []); // -> [object Object]
```

## Додавання RegExps

Чи знали ви, що можете додавати такі числа?

```js
// Patch a toString method
RegExp.prototype.toString =
  function () {
    return this.source;
  } /
  7 /
  -/5/; // -> 2
```

### 💡 Пояснення:

- [**21.2.5.10** get RegExp.prototype.source](https://www.ecma-international.org/ecma-262/#sec-get-regexp.prototype.source)

## Строки не є екземплярами `String`

```js
"str"; // -> 'str'
typeof "str"; // -> 'string'
"str" instanceof String; // -> false
```

### 💡 Пояснення:

Конструктор `String` повертає рядок:

```js
typeof String("str"); // -> 'string'
String("str"); // -> 'str'
String("str") == "str"; // -> true
```

Спробуємо з `new`:

```js
new String("str") == "str"; // -> true
typeof new String("str"); // -> 'object'
```

Об'єкт? Що це?

```js
new String("str"); // -> [String: 'str']
```

Більше інформації про конструктор String у специфікації

- [**21.1.1** The String Constructor](https://www.ecma-international.org/ecma-262/#sec-string-constructor)

## Виклик функцій із зворотними позначками

Let's declare a function which logs all params into the console:

Давайте оголосимо функцію, яка виведе всі параметри в консоль:

```js
function f(...args) {
  return args;
}
```

Без сумніву, ви знаєте, що цю функцію можна викликати так:

```js
f(1, 2, 3); // -> [ 1, 2, 3 ]
```

Але чи знаєте ви, що можете викликати будь-яку функцію із зворотними позначками?

```js
f`true is ${true}, false is ${false}, array is ${[1, 2, 3]}`;
// -> [ [ 'true is ', ', false is ', ', array is ', '' ],
// ->   true,
// ->   false,
// ->   [ 1, 2, 3 ] ]
```

### 💡 Пояснення:

Ну, це зовсім не магія, якщо ви знайомі з _Tagged literal template_. У наведеному вище прикладі функція `f` є тегом для літералу шаблону. Теги перед літералом шаблону дозволяють аналізувати літерали шаблонів за допомогою функції. Перший аргумент функції тегу містить масив рядків. Решта аргументів пов’язані з виразами. Приклад:

```js
function template(strings, ...keys) {
  // do something with strings and keys…
}
```

Це [magic behind](http://mxstbr.blog/2016/11/styled-components-magic-explained/) відома бібліотека під назвою [💅 styled-components](https://www.styled-components.com/), яка є популярною у спільноті React.

Посилання на специфікацію:

- [**12.3.7** Tagged Templates](https://www.ecma-international.org/ecma-262/#sec-tagged-templates)

## Виклик виклик виклик

> Знайдено [@cramforce](http://twitter.com/cramforce)

```js
console.log.call.call.call.call.call.apply((a) => a, [1, 2]);
```

### 💡 Пояснення:

Увага, це може зламати вам голову! Спробуйте відтворити цей код у своїй голові: ми застосовуємо метод `call` за допомогою методу` apply`. Детальніше:

- [**19.2.3.3** Function.prototype.call(`thisArg`, ...`args`)](https://www.ecma-international.org/ecma-262/#sec-function.prototype.call)
- [**19.2.3.1 ** Function.prototype.apply(`thisArg`, `argArray`)](https://www.ecma-international.org/ecma-262/#sec-function.prototype.apply)

## Властивість `constructor`

```js
const c = "constructor";
c[c][c]('console.log("WTF?")')(); // > WTF?
```

### 💡 Пояснення:

Давайте розглянемо цей приклад поетапно:

```js
// Declare a new constant which is a string 'constructor'
const c = "constructor";

// c is a string
c; // -> 'constructor'

// Getting a constructor of string
c[c]; // -> [Function: String]

// Getting a constructor of constructor
c[c][c]; // -> [Function: Function]

// Call the Function constructor and pass
// the body of new function as an argument
c[c][c]('console.log("WTF?")'); // -> [Function: anonymous]

// And then call this anonymous function
// The result is console-logging a string 'WTF?'
c[c][c]('console.log("WTF?")')(); // > WTF?
```

`Object.prototype.constructor` повертає посилання на функцію конструктора `Object`, яка створила об'єкт екземпляра. У випадку з рядками це `String`, у випадку з числами це `Number` і тд.

- [`Object.prototype.constructor`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/constructor) на MDN
- [**19.1.3.1** Object.prototype.constructor](https://www.ecma-international.org/ecma-262/#sec-object.prototype.constructor)

## Об'єкт як ключ властивості об'єкта

```js
{ [{}]: {} } // -> { '[object Object]': {} }
```

### 💡 Пояснення:

Чому це так працює? Тут ми використовуємо _Computed property name_. Коли ви передаєте об'єкт між цими дужками, він перетворює об'єкт у строку, тому ми отримуємо ключ властивості `'[object Object]'` і значення `{}`

Ми можемо написати "дужкове пекло":

```js
({ [{}]: { [{}]: {} } }[{}][{}]); // -> {}

// structure:
// {
//   '[object Object]': {
//     '[object Object]': {}
//   }
// }
```

Детальніше про літерали об’єктів читайте тут:

- [Object initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer) at MDN
- [**12.2.6** Object Initializer](http://www.ecma-international.org/ecma-262/6.0/#sec-object-initializer)

## Доступ до прототипів за допомогою `__proto__`

Як ми знаємо, примітиви не мають прототипів. Однак, якщо ми спробуємо отримати значення `__proto__` для примітивів, ми отримаємо таке:

```js
(1).__proto__.__proto__.__proto__; // -> null
```

### 💡 Пояснення:

Це трапляється тому, що коли щось не має прототипу, воно буде загорнуто в обгортковий об'єкт за допомогою методу `ToObject`. Отже, покроково:

```js
(1)
  .__proto__(
    // -> [Number: 0]
    1
  )
  .__proto__.__proto__(
    // -> {}
    1
  ).__proto__.__proto__.__proto__; // -> null
```

Ось додаткова інформація про `__proto__`:

- [**B.2.2.1** Object.prototype.**proto**](https://www.ecma-international.org/ecma-262/#sec-object.prototype.__proto__)
- [**7.1.13** ToObject(`argument`)](https://www.ecma-international.org/ecma-262/#sec-toobject)

## `` `${{Object}}` ``

Який результат виразу нижче?

```js
`${{ Object }}`;
```

Відповідь:

```js
// -> '[object Object]'
```

### 💡 Пояснення:

Ми визначили об'єкт із властивістю `Object`, використовуючи _Shorthand property notation_:

```js
{
  Object: Object;
}
```

Потім ми передали цей об'єкт до літералу шаблону, тому метод `toString` викликає цей об'єкт. Ось чому ми отримуємо рядок `'[object Object]'`.

- [**12.2.9** Template Literals](https://www.ecma-international.org/ecma-262/#sec-template-literals)
- [Object initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer) at MDN

## Деструктуризація зі значеннями за замовчуванням

Розглянемо цей приклад:

```js
let x,
  { x: y = 1 } = { x };
y;
```

Наведений вище приклад є чудовим завданням для співбесіди. Яке значення `y`? Відповідь така:

```js
// -> 1
```

### 💡 Пояснення:

```js
let x,
  { x: y = 1 } = { x };
y;
//  ↑       ↑           ↑    ↑
//  1       3           2    4
```

З наведеним вище прикладом:

1. Ми оголошуємо `x` без значення, тому воно є `undefined`.
2. Потім ми запаковуємо значення `x` у властивість об'єкта` x`.
3. Потім ми витягуємо значення `x`, використовуючи деструктурування, і хочемо призначити його` y`. Якщо значення не визначено, тоді ми будемо використовувати `1` як значення за замовчуванням.
4. Повертаємо значення `y`.

- [Object initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer) at MDN

## Dots and spreading

Interesting examples could be composed with spreading of arrays. Consider this:

```js
[...[..."..."]].length; // -> 3
```

### 💡 Пояснення:

Why `3`? When we use the [spread operator](http://www.ecma-international.org/ecma-262/6.0/#sec-array-initializer), the `@@iterator` method is called, and the returned iterator is used to obtain the values to be iterated. The default iterator for string spreads a string into characters. After spreading, we pack these characters into an array. Then we spread this array again and pack it back to an array.

A `'...'` string consists with three `.` characters, so the length of resulting array is `3`.

Now, step-by-step:

```js
[...'...']             // -> [ '.', '.', '.' ]
[...[...'...']]        // -> [ '.', '.', '.' ]
[...[...'...']].length // -> 3
```

Obviously, we can spread and wrap the elements of an array as many times as we want:

```js
[...'...']                 // -> [ '.', '.', '.' ]
[...[...'...']]            // -> [ '.', '.', '.' ]
[...[...[...'...']]]       // -> [ '.', '.', '.' ]
[...[...[...[...'...']]]]  // -> [ '.', '.', '.' ]
// and so on …
```

## Labels

Not many programmers know about labels in JavaScript. They are kind of interesting:

```js
foo: {
  console.log("first");
  break foo;
  console.log("second");
}

// > first
// -> undefined
```

### 💡 Пояснення:

The labeled statement is used with `break` or `continue` statements. You can use a label to identify a loop, and then use the `break` or `continue` statements to indicate whether a program should interrupt the loop or continue its execution.

In the example above, we identify a label `foo`. After that `console.log('first');` executes and then we interrupt the execution.

Read more about labels in JavaScript:

- [**13.13** Labelled Statements](https://tc39.github.io/ecma262/#sec-labelled-statements)
- [Labeled statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label) at MDN

## Nested labels

```js
a: b: c: d: e: f: g: 1, 2, 3, 4, 5; // -> 5
```

### 💡 Пояснення:

Similar to previous examples, follow these links:

- [**12.16** Comma Operator (`,`)](https://www.ecma-international.org/ecma-262/#sec-comma-operator)
- [**13.13** Labelled Statements](https://tc39.github.io/ecma262/#sec-labelled-statements)
- [Labeled statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label) at MDN

## Insidious `try..catch`

What will this expression return? `2` or `3`?

```js
(() => {
  try {
    return 2;
  } finally {
    return 3;
  }
})();
```

The answer is `3`. Surprised?

### 💡 Пояснення:

- [**13.15** The `try` Statement](https://www.ecma-international.org/ecma-262/#sec-try-statement)

## Is this multiple inheritance?

Take a look at the example below:

```js
new (class F extends (String, Array) {})(); // -> F []
```

Is this a multiple inheritance? Nope.

### 💡 Пояснення:

The interesting part is the value of the `extends` clause (`(String, Array)`). The grouping operator always returns its last argument, so `(String, Array)` is actually just `Array`. That means we've just created a class which extends `Array`.

- [**14.5** Class Definitions](https://www.ecma-international.org/ecma-262/#sec-class-definitions)
- [**12.16** Comma Operator (`,`)](https://www.ecma-international.org/ecma-262/#sec-comma-operator)

## A generator which yields itself

Consider this example of a generator which yields itself:

```js
(function* f() {
  yield f;
})().next();
// -> { value: [GeneratorFunction: f], done: false }
```

As you can see, the returned value is an object with its `value` equal to `f`. In that case, we can do something like this:

```js
(function* f() {
  yield f;
})()
  .next()
  .value()
  .next()(
    // -> { value: [GeneratorFunction: f], done: false }

    // and again
    function* f() {
      yield f;
    }
  )()
  .next()
  .value()
  .next()
  .value()
  .next()(
    // -> { value: [GeneratorFunction: f], done: false }

    // and again
    function* f() {
      yield f;
    }
  )()
  .next()
  .value()
  .next()
  .value()
  .next()
  .value()
  .next();
// -> { value: [GeneratorFunction: f], done: false }

// and so on
// …
```

### 💡 Пояснення:

To understand why this works that way, read these sections of the specification:

- [**25** Control Abstraction Objects](https://www.ecma-international.org/ecma-262/#sec-control-abstraction-objects)
- [**25.3** Generator Objects](https://www.ecma-international.org/ecma-262/#sec-generator-objects)

## A class of class

Consider this obfuscated syntax playing:

```js
typeof new (class {
  class() {}
})(); // -> 'object'
```

It seems like we're declaring a class inside of class. Should be an error, however, we get the string `'object'`.

### 💡 Пояснення:

Since ECMAScript 5 era, _keywords_ are allowed as _property names_. So think about it as this simple object example:

```js
const foo = {
  class: function () {},
};
```

And ES6 standardized shorthand method definitions. Also, classes can be anonymous. So if we drop `: function` part, we're going to get:

```js
class {
  class() {}
}
```

The result of a default class is always a simple object. And its typeof should return `'object'`.

Read more here:

- [**14.3** Method Definitions](https://www.ecma-international.org/ecma-262/#sec-method-definitions)
- [**14.5** Class Definitions](https://www.ecma-international.org/ecma-262/#sec-class-definitions)

## Non-coercible objects

With well-known symbols, there's a way to get rid of type coercion. Take a look:

```js
function nonCoercible(val) {
  if (val == null) {
    throw TypeError("nonCoercible should not be called with null or undefined");
  }

  const res = Object(val);

  res[Symbol.toPrimitive] = () => {
    throw TypeError("Trying to coerce non-coercible object");
  };

  return res;
}
```

Now we can use this like this:

```js
// objects
const foo = nonCoercible({ foo: "foo" });

foo * 10; // -> TypeError: Trying to coerce non-coercible object
foo + "evil"; // -> TypeError: Trying to coerce non-coercible object

// strings
const bar = nonCoercible("bar");

bar + "1"; // -> TypeError: Trying to coerce non-coercible object
bar.toString() + 1; // -> bar1
bar === "bar"; // -> false
bar.toString() === "bar"; // -> true
bar == "bar"; // -> TypeError: Trying to coerce non-coercible object

// numbers
const baz = nonCoercible(1);

baz == 1; // -> TypeError: Trying to coerce non-coercible object
baz === 1; // -> false
baz.valueOf() === 1; // -> true
```

### 💡 Пояснення:

- [A gist by Sergey Rubanov](https://gist.github.com/chicoxyzzy/5dd24608e886adf5444499896dff1197)
- [**6.1.5.1** Well-Known Symbols](https://www.ecma-international.org/ecma-262/#sec-well-known-symbols)

## Tricky arrow functions

Consider the example below:

```js
let f = () => 10;
f(); // -> 10
```

Okay, fine, but what about this:

```js
let f = () => {};
f(); // -> undefined
```

### 💡 Пояснення:

You might expect `{}` instead of `undefined`. This is because the curly braces are part of the syntax of the arrow functions, so `f` will return undefined. It is however possible to return the `{}` object directly from an arrow function, by enclosing the return value with brackets.

```js
let f = () => ({});
f(); // -> {}
```

## Arrow functions can not be a constructor

Consider the example below:

```js
let f = function () {
  this.a = 1;
};
new f(); // -> f { 'a': 1 }
```

Now, try do to the same with an arrow function:

```js
let f = () => {
  this.a = 1;
};
new f(); // -> TypeError: f is not a constructor
```

### 💡 Пояснення:

Arrow functions cannot be used as constructors and will throw an error when used with new. Because has a lexical `this`, and do not have a `prototype` property, so it would not make much sense.

## `arguments` and arrow functions

Consider the example below:

```js
let f = function () {
  return arguments;
};
f("a"); // -> { '0': 'a' }
```

Now, try do to the same with an arrow function:

```js
let f = () => arguments;
f("a"); // -> Uncaught ReferenceError: arguments is not defined
```

### 💡 Пояснення:

Arrow functions are a lightweight version of regular functions with a focus on being short and lexical `this`. At the same time arrow functions do not provide a binding for the `arguments` object. As a valid alternative use the `rest parameters` to achieve the same result:

```js
let f = (...args) => args;
f("a");
```

- [Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) at MDN.

## Tricky return

`return` statement is also tricky. Consider this:

<!-- prettier-ignore-start -->
```js
(function() {
  return
  {
    b: 10;
  }
})(); // -> undefined
```
<!-- prettier-ignore-end -->

### 💡 Пояснення:

`return` and the returned expression must be in the same line:

```js
(function () {
  return {
    b: 10,
  };
})(); // -> { b: 10 }
```

This is because of a concept called Automatic Semicolon Insertion, which automagically inserts semicolons after most newlines. In the first example, there is a semicolon inserted between the `return` statement and the object literal, so the function returns `undefined` and the object literal is never evaluated.

- [**11.9.1** Rules of Automatic Semicolon Insertion](https://www.ecma-international.org/ecma-262/#sec-rules-of-automatic-semicolon-insertion)
- [**13.10** The `return` Statement](https://www.ecma-international.org/ecma-262/#sec-return-statement)

## Chaining assignments on object

```js
var foo = { n: 1 };
var bar = foo;

foo.x = foo = { n: 2 };

foo.x; // -> undefined
foo; // -> {n: 2}
bar; // -> {n: 1, x: {n: 2}}
```

From right to left, `{n: 2}` is assigned to foo, and the result of this assignment `{n: 2}` is assigned to foo.x, that's why bar is `{n: 1, x: {n: 2}}` as bar is a reference to foo. But why foo.x is undefined while bar.x is not ?

### 💡 Пояснення:

Foo and bar references the same object `{n: 1}`, and lvalues are resolved before assignations. `foo = {n: 2}` is creating a new object, and so foo is updated to reference that new object. The trick here is foo in `foo.x = ...` as a lvalue was resolved beforehand and still reference the old `foo = {n: 1}` object and update it by adding the x value. After that chain assignments, bar still reference the old foo object, but foo reference the new `{n: 2}` object, where x is not existing.

It's equivalent to:

```js
var foo = { n: 1 };
var bar = foo;

foo = { n: 2 }; // -> {n: 2}
bar.x = foo; // -> {n: 1, x: {n: 2}}
// bar.x point to the address of the new foo object
// it's not equivalent to: bar.x = {n: 2}
```

## Accessing object properties with arrays

```js
var obj = { property: 1 };
var array = ["property"];

obj[array]; // -> 1
```

What about pseudo-multidimensional arrays?

```js
var map = {};
var x = 1;
var y = 2;
var z = 3;

map[[x, y, z]] = true;
map[[x + 10, y, z]] = true;

map["1,2,3"]; // -> true
map["11,2,3"]; // -> true
```

### 💡 Пояснення:

The brackets `[]` operator converts the passed expression using `toString`. Converting a one-element array to a string is akin to converting the contained element to the string:

```js
["property"].toString(); // -> 'property'
```

## Null and Relational Operators

```js
null > 0; // false
null == 0; // false

null >= 0; // true
```

### 💡 Пояснення:

Long story short, if `null` is less than `0` is `false`, then `null >= 0` is `true`. Read in-depth Пояснення for this [here](https://blog.campvanilla.com/javascript-the-curious-case-of-null-0-7b131644e274).

## `Number.toFixed()` display different numbers

`Number.toFixed()` can behave a bit strange in different browsers. Check out this example:

```js
(0.7875).toFixed(3);
// Firefox: -> 0.787
// Chrome: -> 0.787
// IE11: -> 0.788
(0.7876).toFixed(3);
// Firefox: -> 0.788
// Chrome: -> 0.788
// IE11: -> 0.788
```

### 💡 Пояснення:

While your first instinct may be that IE11 is correct and Firefox/Chrome are wrong, the reality is that Firefox/Chrome are more directly obeying standards for numbers (IEEE-754 Floating Point), while IE11 is minutely disobeying them in (what is probably) an effort to give clearer results.

You can see why this occurs with a few quick tests:

```js
// Confirm the odd result of rounding a 5 down
(0.7875).toFixed(3); // -> 0.787
// It looks like it's just a 5 when you expand to the
// limits of 64-bit (double-precision) float accuracy
(0.7875).toFixed(14); // -> 0.78750000000000
// But what if you go beyond the limit?
(0.7875).toFixed(20); // -> 0.78749999999999997780
```

Floating point numbers are not stored as a list of decimal digits internally, but through a more complicated methodology that produces tiny inaccuracies that are usually rounded away by toString and similar calls, but are actually present internally.

In this case, that "5" on the end was actually an extremely tiny fraction below a true 5. Rounding it at any reasonable length will render it as a 5... but it is actually not a 5 internally.

IE11, however, will report the value input with only zeros appended to the end even in the toFixed(20) case, as it seems to be forcibly rounding the value to reduce the troubles from hardware limits.

See for reference `NOTE 2` on the ECMA-262 definition for `toFixed`.

- [**20.1.3.3** Number.prototype.toFixed (`fractionDigits`)](https://www.ecma-international.org/ecma-262//#sec-number.prototype.tofixed)

## `Math.max()` less than `Math.min()`

```js
Math.min(1, 4, 7, 2); // -> 1
Math.max(1, 4, 7, 2); // -> 7
Math.min(); // -> Infinity
Math.max(); // -> -Infinity
Math.min() > Math.max(); // -> true
```

### 💡 Пояснення:

- [Why is Math.max() less than Math.min()?](https://charlieharvey.org.uk/page/why_math_max_is_less_than_math_min) by Charlie Harvey

## Comparing `null` to `0`

The following expressions seem to introduce a contradiction:

```js
null == 0; // -> false
null > 0; // -> false
null >= 0; // -> true
```

How can `null` be neither equal to nor greater than `0`, if `null >= 0` is actually `true`? (This also works with less than in the same way.)

### 💡 Пояснення:

The way these three expressions are evaluated are all different and are responsible for producing this unexpected behavior.

First, the abstract equality comparison `null == 0`. Normally, if this operator can't compare the values on either side properly, it converts both to numbers and compares the numbers. Then, you might expect the following behavior:

```js
// This is not what happens
(null == 0 + null) == +0;
0 == 0;
true;
```

However, according to a close reading of the spec, the number conversion doesn't actually happen on a side that is `null` or `undefined`. Therefore, if you have `null` on one side of the equal sign, the other side must be `null` or `undefined` for the expression to return `true`. Since this is not the case, `false` is returned.

Next, the relational comparison `null > 0`. The algorithm here, unlike that of the abstract equality operator, _will_ convert `null` to a number. Therefore, we get this behavior:

```js
null > 0 + null = +0;
0 > 0;
false;
```

Finally, the relational comparison `null >= 0`. You could argue that this expression should be the result of `null > 0 || null == 0`; if this were the case, then the above results would mean that this would also be `false`. However, the `>=` operator in fact works in a very different way, which is basically to take the opposite of the `<` operator. Because our example with the greater than operator above also holds for the less than operator, that means this expression is actually evaluated like so:

```js
null >= 0;
!(null < 0);
!(+null < +0);
!(0 < 0);
!false;
true;
```

- [**7.2.12** Abstract Relational Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-relational-comparison)
- [**7.2.13** Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

## Same variable redeclaration

JS allows to redeclare variables:

```js
a;
a;
// This is also valid
a, a;
```

Works also in strict mode:

```js
var a, a, a;
var a;
var a;
```

### 💡 Пояснення:

All definitions are merged into one definition.

- [**13.3.2** Variable Statement](https://www.ecma-international.org/ecma-262/#sec-variable-statement)

## Default behavior Array.prototype.sort()

Imagine that you need to sort an array of numbers.

```
[ 10, 1, 3 ].sort() // -> [ 1, 10, 3 ]
```

### 💡 Пояснення:

The default sort order is built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

- [**22.1.3.25** Array.prototype.sort ( comparefn )](https://www.ecma-international.org/ecma-262/#sec-array.prototype.sort)

### Hint

Pass `comparefn` if you try to sort anything but string.

```
[ 10, 1, 3 ].sort((a, b) => a - b) // -> [ 1, 3, 10 ]
```

## resolve() won't return Promise instance

```javascript
const theObject = {
  a: 7,
};
const thePromise = new Promise((resolve, reject) => {
  resolve(theObject);
}); // -> Promise instance object

thePromise.then((value) => {
  console.log(value === theObject); // -> true
  console.log(value); // -> { a: 7 }
});
```

The `value` which is resolved from `thePromise` is exactly `theObject`.

How about input another `Promise` into the `resolve` function?

```javascript
const theObject = new Promise((resolve, reject) => {
  resolve(7);
}); // -> Promise instance object
const thePromise = new Promise((resolve, reject) => {
  resolve(theObject);
}); // -> Promise instance object

thePromise.then((value) => {
  console.log(value === theObject); // -> false
  console.log(value); // -> 7
});
```

### 💡 Пояснення:

> This function flattens nested layers of promise-like objects (e.g. a promise that resolves to a promise that resolves to something) into a single layer.

&ndash; [Promise.resolve() on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/resolve)

The specification is [ECMAScript 25.6.1.3.2 Promise Resolve Functions](https://tc39.es/ecma262/#sec-promise-resolve-functions). But it is not quite human-friendly.

# 📚 Other resources

- [wtfjs.com](http://wtfjs.com/) — a collection of those very special irregularities, inconsistencies and just plain painfully unintuitive moments for the language of the web.
- [Wat](https://www.destroyallsoftware.com/talks/wat) — A lightning talk by Gary Bernhardt from CodeMash 2012
- [What the... JavaScript?](https://www.youtube.com/watch?v=2pL28CcEijU) — Kyle Simpsons talk for Forward 2 attempts to “pull out the crazy” from JavaScript. He wants to help you produce cleaner, more elegant, more readable code, then inspire people to contribute to the open source community.

# 🎓 License

[![CC 4.0][license-image]][license-url]

&copy; [Denys Dovhan](http://denysdovhan.com)

[license-url]: http://www.wtfpl.net
[license-image]: https://img.shields.io/badge/License-WTFPL%202.0-lightgrey.svg?style=flat-square
[npm-url]: https://npmjs.org/package/wtfjs
[npm-image]: https://img.shields.io/npm/v/wtfjs.svg?style=flat-square
