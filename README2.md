:::info
VSCode 輸入 ! 即可直接把框架建立，如下

```htmlembedded=
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css" />
  <!-- 網頁名稱 -->
  <title>Document</title>
  </head>
</head>
<body>

</body>
</html>
```

:::

:::info

```htmlembedded=
<!-- Title的文字 -->
<head>
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
</head>
```

HTML 的 class 與 id 是給 CSS 風格做使用的
class 可以重複
id 一個 page 最多一個 id
基本上很少使用 id 來做風格設定
大部分都是用 class 來設定

```htmlembedded=+
<body>
<!-- 內文 -->
    <p class="first">1111</p>
<!-- 以下是標頭大小，有h1~h6的size
    <a>是超連結 -->
    <h6 class="second">
      tetete1 <a href="https://hackmd.io/9qgm7OmzRJOWbQ03Yt2gWQ?both">AAA</a>
    </h6>

<!-- 以下為Image -->
    <img
      id="image_src"
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9bPyKbojb2XDlQ59skQQDI8Ez-rqOd6w8tRfYhpNYACmo1ZDLd9cx&usqp=CAE&s"
    />
    <h2 class="first">Test</h2>
<!-- 以下form是一個框架，input是輸入框、button是按鈕 -->
    <form id="name">
      <h2>Your name</h2>
      <input type="text" placeholder="XXXWW" />
      <button>OK!</button>
    </form>
</body>
```

:::

:::info

### style.css 如下

body 設定
class(first)設定
id(name)設定

```css=
* {
  margin: 0px;
  padding: 0px;
}
body {
  background-color: blanchedalmond;
}

.first {
  color: red;
}

/* border-box是指寬固定為200px
padding左+右假如是50
實際內部僅剩150px的空間可以擺放

content-box是指寬固定為200px
padding左+右假如是50
實際內部依然還有200px的空間可以擺放
且實際大小會變成200+padding-left+padding-right
*/
#name {
  width: 400px;
  height: 200px;
  background-color: pink;
  border: 5px solid #444;
  padding: 30px;
  border-radius: 10px;
  box-sizing: border-box;
}
```

:::

:::info
開發人員模式裡面的 Elements 裡面可以將設定的 style 中，把指定的參數取消打勾，也會即時反應
![](https://i.imgur.com/cjCyF40.png)
:::
