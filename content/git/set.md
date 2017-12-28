##### Set数据解构类似数组，但是不能重复，这是一个去重的例子

```
const a = new Set();
	[1,2,3,4,1,12,12].forEach(i =>a.add(i));
	for( let i of a){
		console.log(i)
	}
  // 1,2,3,4,12
```

##### add(value)：添加某个值，返回 Set 结构本身。
##### delete(value)：删除某个值，返回一个布尔值，表示删除是否成功。
##### has(value)：返回一个布尔值，表示该值是否为Set的成员。
##### clear()：清除所有成员，没有返回值。
##### 是否包含对象和Set 的建 的对比
```
// 对象的写法
const properties = {
  'width': 1,
  'height': 1
};

if (properties[someName]) {
  // do something
}

// Set的写法
const properties = new Set();

properties.add('width');
properties.add('height');

if (properties.has(someName)) {
  // do something
}
```
##### Array.from 可以set 转换成数组
```
const a = new Set([1,2,3,3])
const b = Array.from(a)
console.log(b) // [1,2,3]

```
