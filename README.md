# Lecture-3-
# Сегодня мы с вами познакомимся с последущими темами:
* scope
* hoisting
* TDZ

###  <span style="font-weight:bold; color: red;"> *Что такое Scope?*</span>
Scope (предел,прицел)-означает область видимости, то есть какие-то границы. <br>
Мы прошли с вами три вида:
 *  global scope
 *  local scope, which has two types:
     *  function scope
     *  block scope
  * module scope


 <span style="font-weight:bold; color: red;">*Global scope*</span>  - *глобальным скопом называют пустую консоль или же приведем пример возьмем две функции , в которой одна находится в другой, первая функция для второй, которая внутри ее является глобальной, а первому вторая является локальной, также сама первая функция находится в глобальном скопе, то есть в консоли, отсюда можно сказать что сама консоль эта самая первая граница любого вашего кода. Переменные, объявленные в глобальной области действия, доступны из любой части вашего кода, будь то функции, условные
операторы, циклы или другие блоки кода.* <br>

 <span style="font-weight:bold; color: red;">*Local scope*</span> -
 локальным так как мы сказали сверху является вторая функция для первой. Локальная в свою очередь состоит из двух других:
  *  <span style="font-weight:bold; color: red;">*Function scope*</span> - *область действия функции в JavaScript относится к области действия переменных и функций, которые определены
внутри функции. Переменные и функции, объявленные с ключевым словом var, имеют область действия функции. Переменные, объявленные внутри функции, доступны только внутри этой функции и любых вложенных
функций. Они недоступны за пределами функции, в которой они определены. Это
означает, что к переменным, объявленным внутри функции, нельзя получить доступ до их
объявления или за пределами функции*
``` js 
function polozhNumber(num){
   if(num%4==0) return true;
   else return false
}
console.log(polozhNumber(2016));
``` 
*Function for if and else  was a global and also function in a global scope. It all about function scope.*

*  <span style="font-weight:bold; color: red;">*Block scope*</span> -  *Область действия блока в JavaScript относится к области действия переменных и функций, которые определены
внутри блока кода, например, внутри пары фигурных скобок {}. Переменные и функции,
объявленные с помощью ключевых слов let и const, имеют область действия блока. Переменные, объявленные внутри функции,
доступны только внутри этой функции и любых вложенных функций. Они не доступны
за пределами функции, в которой они определены. Это означает, что переменные, объявленные внутри функции, не могут быть доступны до их объявления или за пределами функции.Переменные, доступные только внутри
блока (область действия блока). ОДНАКО это применимо только к переменным let
и const*
``` js 
if(true) {
    let a="something"
}

for(let i=1; i<=10; i++){
    console.log(i);
    
}
```

*Also we have a module scope, but we learn it in future lessons.*



## <span style="font-weight:bold; color: red;"> *What is a Hoisting?*</span>
*Hoisting — это механизм JavaScript, при котором переменные и объявления функций перемещаются в
верх их области действия перед выполнением кода.*

*Hoisting в JavaScript — это поведение, при котором функция или переменная может использоваться до
объявления.*

*Declaration fumction поднимаются вместе с их значением и могут быть вызваны в любом месте их области действия. В JavaScript declaration function полностью поднимаются. Это означает, что и имя функции, и ее определение перемещаются в верхнюю часть
области действия, делая функцию доступной для вызова в любом месте этой области действия, даже
до ее фактического объявления в коде.*
``` js 
console.log(pycharm("hello"));
function pycharm(){
    return "hello"
}
```

*С переменными, объявленными как var ,
объявление переменной поднимается, но
со значением по умолчанию undefined.*
``` js 
if(true) {
    console.log(a); // undefined
    
    var a="something"
}
```


## <span style="font-weight:bold; color: red;"> *TDZ (Tempalare dead zone let and const)*</span>

*И напоследок поговорим об TDZ: <br>
TDZ: термин для описания состояния, в котором
переменные недоступны. Они находятся в
области действия, но не объявлены. Переменные let и const существуют в TDZ с начала их охватывающей области действия до тех пор,
пока они не объявлены.*

*То есть при ошибке нам tdz выдает две ошибки в двух разных случаях:*
1. *когда мы даем перемннойц одно имя, затем хотим вывести перемнную с другим именем которой у нас нет, нам оно выдаст ошибку:             <br> ReferenceError: b is not defined*
``` js 
console.log(b);
let a=1
```
2.  *когда мы сначала выводим потом создаем переменную нам также выдаст ошибку: <br> ReferenceError: Cannot access 'a' before initialization*
 ``` js 
 console.log(a);
let a=1
```
## <span style="font-weight:bold; color: red;"> *На этом все! Спасибо за внимание!!*</span>
