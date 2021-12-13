## cookie
- flash cookie 同 http cookie一样，旨在记录用户浏览网页信息
- 每个cookie的大小一般不超过4KB，仅在当前域名下使用
- 在application/resources(local storage)
- 通过数据库→WEB存储→cookie
- sessionStorage会话结束时(数据会被清空),而localStorage会长期保存

``` JavaScript
var usen = $("#usen").val();
var saveData = window.localStorage;
$("#usen").val(saveData.getItem("usen"));
$("#btn").on("click", move);
function move() {
  if (!saveData) {
    console.log("没有WEB存储");
    return;
  }
  var tex = $("#usen").val();
  saveData.setItem("usen", txt);
}
```
#### cookie是服务器保存在浏览器端
#### 浏览器端可以设置不接受cookie，也可以设置不向服务器端发送cookie
#### 当前网页cookie：document.cookie；只能写入一个cookie，写入不是覆盖，是添加

<br>

### 属性
- value是键值对，必须指定cookie的值
- expires指定cookie过期的时间，不设置该属性或设置为null，cookie在当前session有效
- domain指定cookie所在的域名
- path指定路径
- secure指定cookie只能在HTTPS协议下发送到服务器。只是一个开关不需要指定值，
- 浏览器对cookie数量没有限制，超过4kb长度的cookie，将会被忽视不会被设置
- 域名和端口一样就能共享cookie
