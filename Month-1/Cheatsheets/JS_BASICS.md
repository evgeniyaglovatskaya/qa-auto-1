# JavaScript Basics

## Navigation in cheetsheet
[Занятие 1 - Переменные и типы данных](#занятие-1---переменные-и-типы-данных)

[Занятие 2 - Условия и логические операторы](#занятие-2---условия-и-логические-операторы)

[Занятие 3 - Функции](#занятие-3---функции)

[Занятие 4 - Массивы (Arrays) и Циклы](#занятие-4---массивы-arrays-и-циклы)

[Занятие 5 - Объекты](#занятие-5---объекты)

## Занятие 1 - Переменные и типы данных

`Переменная (variable)` - область памяти, в которой мы храним данные.

![variable](./img/variable.png)

`Типы` переменных

```js
let // Может менять значение
const // Не может менять значение, константа, всегда должна быть инициализирована
var // Старый стандарт ES5, может менять значение, не рекомендуется к использованию
```

Для названия переменных используем `camelCase`

```js
let myAwesomeVariable; // первое слово с маленькой буквы, остальные с большой
```

Вывод данных в командную строку

```js
console.log('Some text'); // 'Some text' отобразился в консоли

let name = 'Stas';
console.log(name); // 'Stas' (значение переменной name) отобразилось в консоли 
```

## Для имен переменных должны выполняться следующие правила:

 - Имя каждой переменной должно быть уникальным; дубликаты имен не допускаются.
 - Имена переменных не могут содержать пробелов.
 - Нельзя начинать имя переменной с служебных или системных символов- таких как # $ 
 - Имена переменных не должны начинаться или заканчиваться точкой.
 - Следует избегать имен переменных, заканчивающихся символом подчеркивания, поскольку возможен конфликт с именами, созданными автоматически командами и процедурами.
 - В именах переменных не могут использоваться зарезервированные ключевые слова. Зарезервированными словами являются ALL, AND, BY, EQ, GE, GT, LE, LT, NE, NOT, OR, TO и WITH.
 - Имена переменных могут состоять из любого сочетания символов в верхнем и в нижнем регистрах. Регистр сохраняется при выводе на экран имен переменных.
 - В именах нельзя использовать точку - так как может быть воспринято системой как вызов функции.


## Типы данных

**string** - тип string - строка (слово, фраза, предложение, абзац, любой текст)

```js
let cat = 'Iko'; // строка всегда берется в кавычки 
```
**number**  - тип number число (если нет кавычек)

```js
let age = 5; // число без кавычек
age = '5'; // cтрока c числом внутри
```

**boolean** - Булевые значения (логические: true/false)

```js
let isCold = true; // True  - истина
isCold = false; // False - Ложь
```

### Значение `null`

```js
let forest = null; // "Ничего", "Пусто" или "Значение не известно"
```

### Значение `undefined`

```js
let column; // undefined  -  oзначает что "значение не было присвоено" или если переменная была объявлена, но ей не было присвоено никакого 
значения, функция ничего не вернула
```

## Определение типа переменных с помощью оператора `typeof`

```js
let language = 'Italian';
console.log(typeof language); // string
```

## Операторы сравнения

```js
>, <, >=, <= - больше, меньше, больше или равно, меньше или равно

== - Нестрогое сравнение
=== - Строгое сравнение
!= - Нестрогое неравенство
!== - строгое неравенство
```

## Занятие 2 - Условия и логические операторы

### Логические операторы

```js
&& - Логическое И
|| - Логическое ИЛИ
!true - Логическое НЕ 

let index= 11;

if(index < 5){
    console.log('Первый блок')
} else if (index > 5 && index <10) {
    console.log('Второй блок');
} else {
    console.log('Третий блок');
};
```

### Тернарный оператор - Ternary operator 


![Ternary operator](./img/ternary_operator.png)

```js
 (условие) ? (если условие верно) : (если условие Не верно);

// Часто используется в качестве укороченного варианта условного оператора if

50 < 50 ? console.log('Условие верно') : console.log('Условие Не верно');

// Преобразуем конструкцию if в Тернарный оператор

const time = 5

if (time < 10) {
    console.log('Первый блок');
} else {
    console.log('Второй блок')
};

time < 10 ? console.log('Первый блок') : console.log('Второй блок');
```

### Операторы переключения - switch statements

`switch` - они принимают на вход одно выражение/значение, а затем перебирают несколько вариантов, пока не найдут тот,
 который соответствует этому значению, и выполняют соответствующий код.

```js
switch ('переменная') {
    case 'значение1': // если переменная имеет значение 1;
break;
    case 'значение2': // если переменная имеет значение 2;
break;
    default: // если переменная не совпала ни с одним значением;
break;
}
 ```
 `default:` - использовать всегда, так как если не будет выполнено ни одно из условий код ничего не вернет.(default - и есть условия для конструкции)

 `break;` - нужно использовать для завершения обработки определенного оператора с меткой в операторе `switch`. 
 Он выполняет ветвление до конца оператора `switch`. 
 Без оператора `break` выполнение программы продолжается до следующего оператора с меткой.

### Конкатенация строк и шаблонные строки - Concatenation

Конкатена́ция — операция склеивания объектов линейной структуры, обычно строк.

```js
let firstName = 'Bob ';
let lastName = 'Charles';

let user = firstName + lastName;
console.log(user);
```

Шаблонные строки и интерполяция

```js
console.log(`Пользователя с таким id- ${idUser} не найдено`);
```

## Занятие 3 - Функции

### Function Declaration

Функции, объявленные как `Function Declaration`, создаются кодом до выполнения кода.

```js
function nameFunction (){
    console.log('Функция вызвалась');
};

nameFunction(); // Вызов функции где угодно и сколько угодно
```

### Function Expression

Функцию можно создать и присвоить переменной как самое обычное значение.

```js
const functions = function(){
    console.log('function expression');
};

functions();
```
!!! В чем разница? **function expression** нельзя вызвать до инициализации переменной, а **function declaration** можно!

### Параметры и аргументы для функции 

В функции мы указываем какой параметр необходим для выполнения, что нужно передать в функцию и потом обработать внутри функции
При вызове функции мы передаем аргументы функции.

```js
function findElement (parameterName){
    console.log(`На странице'${parameterName} элемент не обнаружен`);
};

let homePage = 'Home Page';
findElement(homePage);
nameFunction('Registration page');
```
### Стрелочные функции - arrow function

Синтаксис стрелочной функций (arrow function):

```js
(argument1, argument2, ... argumentN) => {
  // тело функции
}
```

Это очень похоже на то, как устроены обычные функции, главные отличия заключаются в том, что здесь опущено ключевое слово `function` и добавлена стрелка после списка аргументов. 

```js
1. обычная функция:

let func1 = function(num1, num2) {
	let result = num1 * num2;
console.log(result)	
}

2. стрелочная функция:

let func2 = (num1, num2) => {
	let result = num1 * num2;
	console.log(result)	
}
Обе функции выполняют одинаковые действия.
```

### Ключевое слово Return

Используем `return` если нужно вернуть результат выполнения функции, 
все что будет написано после ключевого слова `return` будет игнорироваться и не будет выполняться, 
так как `return` останавливает дальнейшее выполнение и возвращает результат.

```js
function test (parametrName1, parametrName2, parametrName3){
   const result = parametrName1 + parametrName2 + parametrName3;
   return result;
};
```

## Занятие 4 - Массивы (Arrays) и Циклы

Структура данных
Kак выглядят переменные:

```js
const automobile1 = 'BMW';
const automobile2 = 'Mercedes';
const automobile3 = 'Volvo';
const automobile4 = 'Volkswagen';
```
Как выглядит массив:

```js
const allCars = ['BMW', 'Mercedes', 'Volvo', 'Volkswagen'];
console.log(allCars);
```

Порядок массива:
```js
index 0 - BMW
index 1 - Mercedes
index 2 - Volvo
index 3 - Volkswagen
```

```js
console.log(allCars[0]); // Вывести один элемент из массива
console.log(allCars.length); // Определение длины массива
```

### Методы массивов

```js
allCars.push(...items) - // добавить элемент в конец массива
.pop() - // удалить элемент из конца массива
.shift() - // удалить элемент из конца массива
.unshift(...items) - // добавить элемент в начало массива
.splice([start]), ([deleteCount, newElements]) - // с какого индекса начать удаление, кол-во элементов которые нужно удалить
.includes - // проверить содержит ли массив элемент
.length - // длинна массива
```

### Циклы

let i = 0;  - присваиваем начальное значение переменной " начальный счетчик" - i
i < 10; - условие по которому цикл будет выполнять
i++ - итератор, как будет i изменяться после каждой единицы "будет увеличиваться"

```js
for (let i = 0; i < 10; i++) {
    console.log(i);
}
```

### Обход массива циклом for

```js
const allGermanCars = ['BMW', 'Mercedes', 'Volvo', 'Volkswagen', 'Toyota'];
```

Перебор массива циклом:

```js
for (let i = 0; i < allGermanCars.length; i++) {
    console.log(allGermanCars[i]);
};
```

### Обход массива циклом for (of)

Запись с массива в переменную item: 

```js
const allItalianCars = ['Pagani', 'Mazzanti', 'Ferrari', 'Lamborghini', 'Maserati']; 
for (let item of allBritishCars){
    console.log(item);
}
```

Пример - функции которая проверяет и возвращает определенное значение массива

```js
const assert = searchForCar('Pagani');
console.log(assert);

function searchForCar(nameAuto){
    for (let item of allItalianCars) {
    if(item.includes(nameAuto)){
        let auto = item;
        return auto;     
    }   
}
};
```

# Занятие 5 - Объекты

```js
const userName = {
    name : 'Bob',
    age : '18',
    flat : 'yes'
};
```

```js
console.log(userName); or console.log(userName.name); // Вывод данных из объекта
userName.profession = 'true'; // Добавить объект
delete userName.profession; // Удалить объект
```

```js
let objectOne = new Object(); // синтаксис “конструктор объекта” 
let objectTwo = {}; // синтаксис “литерал объекта”
```

Вывод данных из объекта где ключ - строка:

```js
const userInfo = {
    name : 'Bob',
    age : '18',
    flat : 'yes',
    'My car': true
};

console.log(userInfo["My car"]);
```

Вывод данных объект в объекте:

```js
let user = {
    name : 'Bob',
    age : '18',
    flat : 'yes',
    address : {
        city : 'Berlin',
        country : 'Germany'
    }
};

console.log(user.adress.country);
```

### Обход цикла методом for in

```js
const userData = {
    name : 'Bob',
    age : '18',
    flat : 'yes'
};
```
`index` - вывод ключей,  userData[index] - вывод значений

```js
for (let index in userData){
   console.log(index , userData[index]);
};
```

### Методы объекта и this

Пример использования ключевого слова `this`:

```js
const person = {
    name : 'Bob',
    age : '18',
    color : function(){
        console.log(this.name);
    }
};

person.color();
```
