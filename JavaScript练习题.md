# JavaScript 练习题

这份练习题会持续更新！

## 1. 计算两个日期的天数差

### 函数模板
```javascript
function daySpan (date1, date2) {
  // your code
}
```

### 函数参数
* `date1: Date` 第一个日期
* `date2: Date` 第二个日期

### 调用样例
```javascript
daySpan(new Date(2016, 2, 7), new Date(2016, 4, 12))     // 66
daySpan(new Date(2016, 4, 12), new Date(2016, 2, 7))     // 66
```

## 2. 计算两个日期的天数差 - 高级版

### 函数模板
```javascript
function daySpan (date1, date2) {
  // your code
}
```

### 函数参数
* `date1: String` 第一个日期
* `date2: String` 第二个日期

这两个日期字符串都会按照`YYYY-MM-DD`的格式输入，如`2016-10-09`

### 调用样例
```javascript
daySpan('2016-02-07', '2016-04-12')     // 65
daySpan('2016-04-12', '2016-02-07')     // 65
```

## 3. 计算数组中元素重复次数

### 函数模板
```javascript
function countRepeat (arr) {
  // your code
}
```

### 函数参数
* `arr: Array<Number>` 仅包含数字的数组

### 调用样例
```javascript
countRepeat([2, 9, 8, 4, 5, 3, 4, 8, 9, 9, 1, 0, 2, 1])
/* 顺序不影响结果
{
  '0': 1,
  '1': 2,
  '2': 2,
  '3': 1,
  '4': 2,
  '5': 1,
  '8': 2,
  '9': 3
} */
```

## 4. 驼峰转换函数

在代码的世界里，标识符中不能有空格，
但有时一个变量必须由两个或更多个单词来表达，如`count repeat`、`get own poperty descriptor`等。
这时候就必须把他们写成**第一个单词全小写，第二个以及后面的单词，除了首字母全小写**的形式（即**驼峰**），
如`countRepeat`、`getOwnPropertyDescriptor`

下面你需要编写一个函数来实现这个功能

### 函数模板
```javascript
function camelCase (str) {
  // your code
}
```

### 函数参数
* `str: String` 要转换的字符串，可能的形式看下面的例子

### 调用样例
```javascript
camelCase('hey guys')           // 'heyGuys'
camelCase('HELLO-world')        // 'helloWorld'
camelCase('oh  mY---gOd')       // 'ohMyGod'
```

## 5. 寻找字符串中第一个未重复的字符

寻找字符串中第一个未重复的字符，如果没有找到，则返回一个空字符串（`''`）

### 函数模板
```javascript
function firstNonRepeat (str) {
  // your code
}
```

### 函数参数
* `str: String` 要寻找的字符串，可能是任何内容

### 调用样例
```javascript
firstNonRepeat('aaabccc')     // 'b'
firstNonRepeat('aabccbd')     // 'd'
firstNonRepeat('aabxbcc')     // 'x'
firstNonRepeat('6666666')     // ''
```

## 6. 展平数组

数组中可以嵌套数组，要嵌套多少层都可以，比如`[1, 2, [[3], 4]]`。
这样看起来很不爽，所以我们要把它展开，只留下一层数组: `[1, 2, 3, 4]`

提示：判断`xxx`是否是数组的方法为 `Array.isArray(xxx)`

### 函数模板
```javascript
function flatten (arr) {
  // your code
}
```

### 函数参数
* `arr: Array` 包含嵌套数组的数组

### 调用样例
```javascript
flatten([1, 2, 3])                // [1, 2, 3]
flatten([1, 2, [3]])              // [1, 2, 3]
flatten([1, 2, [[3], 4]])         // [1, 2, 3, 4]
flatten([1, [2, [[3], [4]]]])     // [1, 2, 3, 4]
```
## 7. 判断空对象

在 JavaScript 编程中，经常我们要判断某个变量是否为空对象，而不是 `null` 或者 `undefined`，那么，请实现一个函数判断变量是否为空对象。

### 函数模板

```javascript
function isEmptyObject (obj) {
  // your code
}
```

### 函数参数

- `obj: mixed` 可能为空对象的任何类型变量

### 调用样例

```javascript
isEmptyObject({})              // true
isEmptyObject(null)            // false
isEmptyObject(undefined)       // false
isEmptyObject('{}')            // false
isEmptyObject([])              // false
isEmptyObject(true)            // false
```

## 8. 数组去重

返回一个无重复值的数组

### 函数模板

```javascript
function unique (arr) {
  // your code
}
```

### 函数参数

- `arr: Array` 反正就是一个数组

### 调用示例

```javascript
unique([1, 2, 3, 4, 4, 5, 8, 6, 3, 2, 1])   // [1, 2, 3, 4, 5, 8, 6]
```

## 9. 实现一个 `reduce` 函数

`reduce` 是函数式编程中十分重要的一个函数，请实现一个 `reduce` 函数，可以参考 `[].reduce` 。

### 函数模板

```javascript
function reduce (arr, func, initialValue) {
  // your code
}
```

### 函数参数

- `arr: Array` 调用 `reduce`  的数组
- `func: Function` `reduce` 执行数组中每个值的函数，包含两个参数
  - `previousValue` 上一次调用回调返回的值，或者是提供的初始值（`initialValue`）
  - `currentValue` 数组中当前被处理的元素
- `initialValue：mixed` 作为第一次调用 `callback` 的第一个参数。

### 调用示例

```javascript
var total = reduce([0, 1, 2, 3], function (previousValue, currentValue) {
  return previousValue + currentValue
}, 0)
// total === 6
```
