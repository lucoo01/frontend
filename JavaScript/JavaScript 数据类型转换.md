JavaScript 中有两种主要的数据类型转换：隐式转换和显式转换。

1. **隐式转换（Implicit Conversion）:**
   - 隐式转换是在运行时自动发生的，由 JavaScript 引擎执行。
   - 当操作涉及不同数据类型的值时，JavaScript 会尝试自动转换其中一个或多个值，以便它们的类型匹配。
   - 例如，数字和字符串相加时，数字会被隐式转换为字符串。

   ```javascript
   let num = 5;
   let str = "10";
   let result = num + str; // 隐式转换，result 的值为 "510"
   ```

2. **显式转换（Explicit Conversion）:**
   - 显式转换是由开发人员明确执行的，通过使用内置的转换函数或操作符。
   - 常见的显式转换包括：
     - **字符串转数字：** 使用 `parseInt()` 或 `parseFloat()` 函数，或者 `Number()` 构造函数。
       ```javascript
       let strNumber = "25";
       let num = parseInt(strNumber); // 显式转换，num 的值为 25
       ```

     - **数字转字符串：** 使用 `String()` 构造函数或者将数字与空字符串相加。
       ```javascript
       let num = 42;
       let str = String(num); // 显式转换，str 的值为 "42"
       ```

     - **布尔值转换：** 使用 `Boolean()` 构造函数。
       ```javascript
       let value = 0;
       let booleanValue = Boolean(value); // 显式转换，booleanValue 的值为 false
       ```

     - **数组转换：** 使用 `toString()` 或 `join()` 方法。
       ```javascript
       let arr = [1, 2, 3];
       let str = arr.toString(); // 显式转换，str 的值为 "1,2,3"
       ```

显式转换通常用于确保变量或值的类型符合预期，以避免意外的隐式转换导致错误或不确定的行为。
