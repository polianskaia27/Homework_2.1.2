# Типы операторов в JavaScript

## Операторы присваивания
В результате операции присваивания операнду слева от оператора присваивания (знак "=") устанавливается значение , которое берётся из правого операнда. Основным оператором присваивания является `=`, он присваивает значение правого операнда операнду, находящемуся слева. Таким образом, выражение `x = y` означает, что `x` присваивается значение `y`.

## Операторы сравнения
Оператор сравнения сравнивает свои операнды и возвращает логическое значение, базируясь на истинности сравнения. Операнды могут быть числами, строками, логическими величинами или объектами. Строки сравниваются на основании стандартного лексикографического порядка, используя Unicode-значения.
```
var var1 = 3,`
var2 = 4;
```
1. __Равно (==)__	Возвращает true, если операнды равны.	`3 == var1 "3" == var1 3 == '3'`
2. __Не равно (!=)__	Возвращает true, если операнды не равны.	`var1 != 4 var2 != "3"`
3. __Строго равно (===)__	Возвращает true, если операнды равны и имеют одинаковый тип.	`3 === var1`
4. __Строго не равно(!==)__ 	Возвращает true, если операнды не равны и/или имеют разный тип.	`var1 !== "3" 3 !== '3'`
5. __Больше (>)__	Возвращает true, если операнд слева больше операнда справа.	`var2 > var1 "12" > 2`
6. __Больше или равно (>=)__	Возвращает true, если операнд слева больше или равен операнду справа.	`var2 >= var1 var1 >= 3`
7. __Меньше (<)__	Возвращает true, если операнд слева меньше операнда справа.	`var1 < var2 "2" < 12`
8. __Меньше или равно (<=)__	Возвращает true, если операнд слева меньше или равен операнду справа.

## Арифметические операторы
Арифметические операторы используют в качестве своих операндов числа (также литералы или переменные) и в качестве результата возвращают одно числовое значение. Стандартными арифметическими операторами являются сложение (`+`), вычитание (`-`), умножение (`*`), и деление (`/`). При работе с числами с плавающей точкой эти операторы работают аналогично их работе в большинстве других языках программирования (обратите внимание, что деление на ноль возвращает бесконечность Infinity).

## Битовые (поразрядные) операторы
Битовые операторы обрабатывают свои операнды как последовательности из 32 бит (нулей и единиц), а не как десятичные, шестнадцатеричные или восьмеричные числа. Например, десятичное число 9 имеет двоичное представление 1001. Битовые операторы выполняют операции над таким двоичным представлением, но результат возвращают как обычное числовое значение JavaScript.

## Логические операторы
Логические операторы обычно используются с булевыми (логическими) значениями; при этом возвращаемое ими значение также является булевым. Однако операторы `&&` и `||` фактически возвращают значение одного из операндов, поэтому, если эти операторы используются с небулевыми величинами, то возвращаемая ими величина также может быть не булевой.

1. Логическое __И(`&&`)	`expr1 && expr2`	Возвращает операнд `expr1`, если он может быть преобразован в `false`; в противном случае возвращает операнд `expr2`. Таким образом, при использовании булевых величин в качестве операндов, оператор `&&` возвращает `true`, если оба операнда `true`; в противном случае возвращает `false`.
2. Логическое ИЛИ(`||`)	`expr1 || expr2` Возвращает операнд `expr1`, если он может быть преобразован в `true`; в противном случае возвращает операнд `expr2`. Таким образом, при использовании булевых величин в качестве операндов, оператор `||` возвращает `true`, если один из операндов `true`; если же оба `false`, то возвращает `false`.
3. Логическое НЕ (`!`)	`!expr`	Возвращает `false`, если операнд может быть преобразован в `true`; в противном случае возвращает `true`. 

## Строковые операторы
В дополнение к операторам сравнения, которые могут использоваться со строковыми значениями, оператор (`+`) позволяет объединить две строки, возвращая при этом третью строку, которая представляет собой объединение двух строк-операндов.

## Условный (тернарный) оператор
Условный оператор является единственным оператором JavaScript, который использует три операнда. Оператор принимает одно из двух значений в зависимости от заданного условия. Синтаксис оператора:
```
condition ? val1 : val2
```
Если condition (условие) - истина, то оператор принимает значение `val1`. В противном случае оператор принимает значение `val2`. Вы можете использовать условный оператор во всех случаях, где может быть использован стандартный оператор.

## Оператор запятая
Оператор запятая (`,`) просто вычисляет оба операнда и возвращает значение последнего операнда. Данный оператор в основном используется внутри цикла `for`, что позволяет при каждом прохождении цикла одновременно обновлять значения нескольких переменных.

## Унарные операторы

1. Оператор `delete` выполняет удаление объекта, свойства объекта, или элемента массива с заданным индексом. Синтаксис оператора:
```
delete objectName;
delete objectName.property;
delete objectName[index];
delete property; // допустимо только внутри with
```
где `objectName` представляет собой имя объекта, `property` - свойство объекта, а `index` - целое число, указывающее на положение (номер позиции) элемента в массиве.

2. Оператор `typeof` используется одним из следующих способов:
```
typeof operand
typeof (operand)
```
Оператор `typeof` возвращает строку обозначающую тип невычисленного операнда. Значение `operand` может быть строкой, переменной, дескриптором, или объектом, тип которого следует определить. Скобки вокруг операнда необязательны.

3. Оператор `void` используется любым из следующих способов:
```
void (expression)
void expression
```
Оператор `void` определяет выражение, которое должно быть вычислено без возвращения результата. `expression` - это выражение JavaScript, требующее вычисления. Скобки вокруг выражения необязательны, но их использование является правилом хорошего тона.
Вы можете использовать оператор void для указания на то, что операнд-выражение является гипертекстовой ссылкой. При этом выражение обрабатывается, но не загружается в текущий документ.

## Операторы отношения
Оператор отношения сравнивает свои операнды и возвращает результат сравнения в виде булева значения.

1. Оператор `in` возвращает `true`, если указанный объект имеет указанное свойство. Синтаксис оператора:
```
propNameOrNumber in objectName
```
где `propNameOrNumber` - строка или числовое выражение, представляющее имя свойства или индекс массива, а `objectName` - имя объекта.

2. Оператор `instanceof` возвращает `true`, если заданный объект является объектом указанного типа. Его синтаксис:
```
objectName instanceof objectType
```
где `objectName` - имя объекта, тип которого необходимо сравнить с `objectType`, а `objectType` - тип объекта, например, `Date` или `Array`

[Ссылка на источник.](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Expressions_and_operators#%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B_%D0%BF%D1%80%D0%B8%D1%81%D0%B2%D0%B0%D0%B8%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F) 

# Динамическая типизация
Это свойство языка, позволяющее переменным менять свой тип данных в процессе выполнения программы. Переменная связывается с типом в момент присваивания значения, а не в момент объявления переменной. 

```javascript
let dynamicTyping;

dynamicTyping = "string";
console.log(typeof dynamicTyping);

dynamicTyping = 10;
console.log(typeof dynamicTyping);
```

OUTPUT
```
string
number
```