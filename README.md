# JavaScriptBasic2

{%hackmd BJrTq20hE %}

:::success
嚴格模式開啟
'use strict';
開啟後未定義的，一些原本不會跳錯的，因為檢查變嚴格了，將會跳錯
:::

:::info
function 不需要宣告變數型態與返回型態

```javascript=
//function declaration，並由下方呼叫
function processData(data1, data2) {
  const content = `data1 = ${data1}, data2 = ${data2}`;
  return content;
}

const result = processData(5, 0);
console.log(result);
//輸出data1 = 5, data2 = 0
```

```javascript=
//匿名的function給予processData2，下方呼叫processData2
//function expression，常用於callback
const processData2 = function (data1, data2) {
  const content = `data1 = ${data1}, data2 = ${data2}`;
  return content;
}

const result2 = processData2(5, 0);
console.log(result2);
```

Arrow function 由 ES6 以上提供

```javascript=
const processData3 = (data1, data2) => `data1 = ${data1}, data2 = ${data2}`;
console.log(processData3(5, 0))

const processData4 = (data1, data2) => {
  const content = `data1 = ${data1}, data2 = ${data2}`;
  return content
}
console.log(processData4(5, 0))
```

:::

:::info
Array

```javascript=
const numberList = [1, 2, 3, 4, 6];
const arrays = new Array(2, 3, 4, 5, 8);
console.log(numberList[2])
console.log(arrays[2])

console.log(numberList.length)
console.log(arrays.length)

//允許多型態組合
const list = [12, 'apple', [2, 3, 4]]
console.log(list)
```

```javascript=
const list = ['apple', 'google', 'youtube']
//由右邊插入資料
list.push('momo')

//由右邊推出資料
const item = list.pop()
console.log(item)//輸出momo
console.log(list)//['apple', 'google', 'youtube']

//由左邊推出資料
const item2 = list.shift()
console.log(item2)//輸出apple
console.log(list)//['google', 'youtube']

//由左邊插入資料
list.unshift("123")
console.log(list)//['123', 'google', 'youtube']

//由左邊推出資料
const item3 = list.shift()
console.log(item3)//輸出123
console.log(list)//['google', 'youtube']

//找不到回傳-1，找到回傳index
console.log(list.indexOf('google'))//0
console.log(list.indexOf('ooo'))//-1


//找不到回傳false，找到回傳true
console.log(list.includes('google'))//true
console.log(list.includes('ooo'))//false
```

:::

:::info
Dictionary 與輸入提示視窗

```javascript=
const dictionary = {
  name: '1234',
  data: 24,
  age: 18,
  ageFunc: function () {
    return this.age > 30
  }
}

console.log(dictionary)

//出現提示視窗，並可以輸入參數
const interestedIn = prompt("please!")
if (dictionary[interestedIn]) { //找不到會是undefined
  console.log(dictionary[interestedIn])
} else {
  console.log("NO!")
}
```

執行 Dictionary 的 Func

```javascript=+
console.log(dictionary.ageFunc())//false
dictionary['age'] = 31
console.log(dictionary['ageFunc']())//true

```

:::

:::info
for、while 與 java 一樣

```javascript=
const list = []

for (let i = 0; i < 10; i++) {
  // console.log(i)
  list.push(typeof i)
}

console.log(list)
```

:::

###### tags: `JavaScript`
