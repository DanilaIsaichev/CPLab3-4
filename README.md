# Отчёт по лабораторным работам 3 и 4

## Цель:

Транспиляция с помощью Babel, развёртывание проекта на JavaScript, включающего модули.

## Файл index.js до выполнения транспиляции:

```js
16 |> Math.sqrt |> console.log
```

## Файл index.js после выполнения транспиляции:

```js
var _ref, _;

_ref = (_ = 16, Math.sqrt(_)), console.log(_ref);
```

## Файл main.js до выполнения транспиляции:

```js
import moment from 'moment';
import name from './name';
console.log(name);
console.log(moment.unix('1500514362').format('DD.MM.YYYY HH:mm:ss'));
```

## Файл main.js после выполнения транспиляции:

```js
'use strict';

var _moment = require('moment');

var _moment2 = _interopRequireDefault(_moment);

var _name = require('./name');

var _name2 = _interopRequireDefault(_name);

function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }

console.log(_name2.default);
console.log(_moment2.default.unix('1500514362').format('DD.MM.YYYY HH:mm:ss'));
```

## Файл name.js до выполнения транспиляции:

```js

```

## Файл name.js после выполнения транспиляции:

```js
'use strict';

Object.defineProperty(exports, "__esModule", {
  value: true
});
exports.default = 'D. O. Isaichev';
```

## Вывод:

В ходе выполнения работ были получены навыки работы с транспилятором Babel. Была выполнена транспиляция файлов index.js, main.js, name.js.
