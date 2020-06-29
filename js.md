JavaScript函数式编程指南
1. 什么是函数式编程
函数式编程(Functional Programming, FP)，FP是编程范式之一，我们常听说的编程范式还有面向过程编程、面向对象编程。
面向对象编程的思维方式: 把现实世界中的事物抽象成程序世界中的类和对象，通过封装、继承和多态来演示事物事件的联系。
函数式编程的思维方式: 把现实世界的事物和事物之间的联系抽象到程序世界(对运算过程进行抽象)

程序的本质: 根据输入通过某种运算获得相应的输出，程序开发过程中会涉及很多有输入和输出的函数

x -> f(联系、映射) -> y, y=f(x)

函数式编程中的函数指的不是程序中的函数(方法)，而是数学中的函数即映射关系，例如: y = sin(x), x和y的关系
例子来看一下函数式和非函数式：

非函数式：

let num1 = 2
let num2 = 3
let sum = num1 + num2
console.log(sum)
函数式：

function add (n1, n2) {
  return n1 + n2
}
let sum = add(2, 3)
console.log(sum)
2. 
函数是一等公民
高阶函数
闭包

2.1 函数是一等公民(MDN First-class Function)
函数可以存储在变量中
函数作为参数
函数作为返回值

在JavaScript中函数就是一个普通的对象(可以通过new Function()生成)，我们可以把函数存储到变量/数组中，它还可以作为另一个函数的参数和返回值，甚至我们可以在程序运行的时候通过new Function('alert(1)')来构造一个新的函数。
把函数赋值给变量:

let fn = function() {
    console.log('Hello First-class Function')
}



