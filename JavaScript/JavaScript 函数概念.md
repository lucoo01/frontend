**JavaScript 函数概念：**

函数是 JavaScript 中的一等公民，它是可执行的代码块，用于执行特定任务或操作。函数有输入参数和返回值，并可以包含一系列语句。在 JavaScript 中，函数是对象，因此可以存储在变量中、作为参数传递、或者作为返回值。

**自定义函数：**

自定义函数是由开发人员创建的函数，用于执行特定的任务。函数定义使用 `function` 关键字，可以有参数和返回值。

```javascript
function add(a, b) {
    return a + b;
}
```

**调用方式：**

1. **全局调用：**
   全局调用是在全局作用域中直接调用函数。

   ```javascript
   add(2, 3); // 返回 5
   ```

2. **构造函数调用：**
   使用 `new` 关键字创建函数的实例，称为构造函数调用。

   ```javascript
   let result = new add(2, 3); // 返回一个新对象，通常不推荐在这里使用函数
   ```

3. **函数方法调用：**
   函数可以作为对象的方法调用。

   ```javascript
   let obj = {
       calculate: add
   };
   obj.calculate(2, 3); // 返回 5
   ```

4. **apply 和 call 方法调用：**
   `apply` 和 `call` 是函数对象的方法，用于在特定的作用域中调用函数。

   ```javascript
   let obj = {
       value: 10
   };

   function multiply(a, b) {
       return a * b * this.value;
   }

   multiply.apply(obj, [2, 3]); // 使用 apply，返回 60
   multiply.call(obj, 2, 3); // 使用 call，返回 60
   ```

   这两者的区别在于传递参数的方式：`apply` 接收一个参数数组，而 `call` 接收多个参数。

函数是 JavaScript 编程中的核心概念，它们提供了模块化、封装和重用代码的能力，是构建复杂应用程序的重要组成部分。
