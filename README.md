# function-js
#### В JavaScript функции – это объекты. Можно представить функцию как «объект, который может делать какое-то действие». Функции можно не только вызывать, но и использовать их как обычные объекты: добавлять/удалять свойства, передавать их по ссылке и т.

# Condition
### Мы можем передать внутрь функции любую информацию, используя параметры. 

#### Функция в JavaScript специальный тип объектов, позволяющий формализовать средствами языка определённую логику поведения и обработки данных. Для понимания работы функций необходимо (и достаточно?) иметь представление о следующих моментах:
способы объявления
способы вызова
параметры и аргументы вызова (arguments)
область данных (Scope) и замыкания (Closures)
объект привязки (this)
возвращаемое значение (return)

# Объявление функций
## Функции вида function declaration
Объявление функции (function definition, или function declaration, или function statement) состоит из ключевого слова function и следующих частей:
Имя функции.
Список параметров (принимаемых функцией) заключённых в круглые скобки () и разделённых запятыми.
Инструкции, которые будут выполнены после вызова функции, заключают в фигурные скобки { }.
function square(number) {
  return number * number;
}

## function expression
Функция вида "function declaration statement" по синтаксису является инструкцией (statement), ещё функция может быть вида "function definition expression". Такая функция может быть анонимной (она не имеет имени). Например, функция square может быть вызвана так:
let square = function (number) {
  return number * number;
};
let x = square(4);
Однако, имя может быть и присвоено для вызова самой себя внутри самой функции и для отладчика (debugger) для идентифицированные функции в стек-треках (stack traces; "trace" — "след" / "отпечаток").
let factorial = function fac(n) {
  return n < 2 ? 1 : n * fac(n - 1);
};
console.log(factorial(3));
Функции вида "function definition expression" удобны, когда функция передаётся аргументом другой функции. Следующий пример показывает функцию map, которая должна получить функцию первым аргументом и массив вторым.
