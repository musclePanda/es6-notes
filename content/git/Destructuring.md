##### 数组和对象的解构赋值
```
let [a,b,c] = [1,2,3]
let { foo, bar } = { foo: "aaa", bar: "bbb" };

let [head, ...tail] = [1, 2, 3, 4];
head // 1
tail // [2, 3, 4]

```
##### 解构允许默认值
```
let [foo = true] = [];
foo // true

let [x, y = 'b'] = ['a']; // x='a', y='b'
let [x, y = 'b'] = ['a', undefined]; // x='a', y='b'

```
##### 默认值可以引用解构赋值的其他变量，但该变量必须已经声明

```
let [x = 1, y = x] = [];     // x=1; y=1
let [x = 1, y = x] = [2];    // x=2; y=2
let [x = 1, y = x] = [1, 2]; // x=1; y=2
let [x = y, y = 1] = [];     // ReferenceError
var {x = 3} = {};            // x=3
var {x, y = 5} = {x: 1};      // x=1; y=5
var {x: y = 3} = {};          // y=3
var {x: y = 3} = {x: 5};      // y=5

```
##### 对象的解构赋值的内部机制，是先找到同名属性，然后再赋给对应的变量。真正被赋值的是后者，而不是前者。
```
let { foo: baz } = { foo: "aaa", bar: "bbb" };
baz // "aaa"
foo // error: foo is not defined

```
##### 遍历 Map 结构
```
const map = new Map();
map.set('first', 'hello');
map.set('second', 'world');

for (let [key, value] of map) {
  console.log(key + " is " + value);
}
// first is hello
// second is world

```
##### 输入模块的指定方法

```
const { SourceMapConsumer, SourceNode } = require("source-map");

```
