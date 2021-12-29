# 1. Объекты
### Используйте синтаксис с фигурными скобками вместо Object() для создания объектов
### Good:
```
 let user = {};
```
### Bad:
```
 let user = new Object();
```
# 2. Массивы
### Используйте синтаксис с квадратными скобками вместо Array() для создания массивов
### Good:
```
let arr = [];
```
### Bad:
```
let arr = new Array();
```
# 3. Строки
### Используйте одинарные кавычки ‘ ’
### Good:
```
const name = 'Capt. Janeway';
```
### Bad:
```
const name = "Capt. Janeway";
```
# 4. Функции
### Используйте названые выражения функций вмест объявления функций
### Good:
```
const short = function longUniqueMoreDescriptiveLexicalFoo() {
      // ...
};
```
### Bad:
```
function foo() {
      // ...
}
```
# 5. Стрелочные функции
### Если вы используете функции без имени, то лучше использовать стрелочные функции
### Good:
```
[1, 2, 3].map((x) => {
  const y = x + 1;
  return x * y;});
```
### Bad:
```
[1, 2, 3].map(function (x) {
  const y = x + 1;
  return x * y;});
```
# 6.Классы
### Всегда используйте класс. Избегайте прямых манипуляций с прототипом.
### Good:
```
class Queue {
  constructor(contents = []) {
    this.queue = [...contents];
  }
  pop() {
    const value = this.queue[0];
    this.queue.splice(0, 1);
    return value;
  }}
```
### Bad:
```
function Queue(contents = []) {
  this.queue = [...contents];}Queue.prototype.pop = function () {
  const value = this.queue[0];
  this.queue.splice(0, 1);
  return value;};
```
# 7. Переменные
### Всегда используйте const и let для объявления переменных.
### Good:
```
const superPower = new SuperPower();
```
### Bad:
```
superPower = new SuperPower();
```
# 8. Пробелы
### Используйте расстояние в 2 пробела
### Good:
```
function baz() {
∙∙let name;
}
```
### Bad:
```
function foo() {
∙∙∙∙let name;
}
```
# 9. Блоки
### Используйте фигурные скобки со всеми многострочными блоками.
### Good:
```
function bar() {
  return false;
}
```
### Bad:
```
function foo() { return false; }
```
# 10. Комментарии
### Используйте /** ... */ для многострочных комментариев.
### Good:
```
/** 
* make() returns a new element 
* based on the passed-in tag name 
*/
```
### Bad:
```
// make() returns a new element
// based on the passed in tag name//
// @param {String} tag
```