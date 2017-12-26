##### 字符串的方法查找方法
```
let s = 'Hello world!';
console.log(s.indexOf('llo',0))  //2 下标 第二位的参数是开始搜索的下标
console.log(s.startsWith('Hello')) // true
console.log(s.endsWith('!')) // true
console.log(s.includes('o')) // trues

```
##### 字符串的重复的方法
```
'x'.repeat(3) // "xxx"
'hello'.repeat(2) // "hellohello"
'na'.repeat(0) // ""
```
##### 字符串中嵌入变量,还可以表达式，调用方法， 注意是波浪号那个按钮
```
var a = 12;
var c = 12;
var b = `a is ${a*c}`
console.log(b)  //this is 144
```
