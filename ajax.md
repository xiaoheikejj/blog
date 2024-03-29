## 设计模式的例子工厂模式
``` JavaScript
function factory(name, age) {
  var obj = {};
  obj.name = name;
  obj.age = age;
  obj.fun = function() {
    console.log("工厂方法");
  }
  return obj;
}
var student = factory("张三",10);
```
<br>

> 面向对象编程思想（oop）。对象指的是单个实物的抽象，比如人（种类）。通常需要一个模板，表示某一类实物的共同特征，对象就是根据这个模板生成的。
构造函数就是专门生成对象的函数。java基于类，js基于构造函数和原型链。构造函数的两大特点（1.函数体内部使用了this关键字，代表对象生成的实例。2.
生成对象的时候，必须使用new命令，调用xx函数）

<br>

## 关于Ajax
- 全称是asynchronous Javascript And XML
- 核心对象是XMLHTTPRequest，后台与服务器进行少量数据交换，使网页实现异步更新
### 步骤如下
1. 创建新的XMLHTTPRequest对象
2. 发送Ajax请求
	- open方法
	- send方法
4. 接受请求 onreadystatechange

#### 同源策略/同域 包括以下3点相同 域名，端口，协议
#### 关于
``` JavaScript
try {
 // success
} catch(e) {
 // error handle
}
``` 

#### 响应时间：timeout

## Ajax的核心代码
<br>

``` JavaScript
var xhr;
if (window.XMLHttpRequest) {
  xhr = new xXMLHttpRequest();
} else {
  xhr = new AActiveXObject("Microsoft.XMLHTTP");
  xhr.onreadystatechange = function();
  if(xhr.readyState === 4 && xhr.status === 200){
    console.log(xhr.response);
  }
}
xhr.open("GET/post", "http://www.exmple.com/test.php", true);
xhr.send();
```


###### 解析JSON数据用eval或者JSON.parse
###### eval方法会解析JSON字符串当中的方法

###### cookie是保存在浏览器中一小段文本信息，每个cookie大小不大于4kb,浏览器每次向服务器发送请求就会附上这段信息
###### 包括名字，值，到期时间，所属域名，生效的路径
###### 浏览器可以不设置cookie，也可以不向服务器发送cookie
###### 浏览器的同源策略规定：端口和域名相同，可以共享cookie；协议不相同也可以共享cookie
###### web storage 浏览器端数据存储机制
###### 分为sessionStorage和localStorage
###### sessionStorage当回话结束，数据被清空
###### localStorage数据被长期保存，在下一次访问网站的时候，网页可以直接读取以前保存的数据
###### 他们可以视为强化版的cookie，能够动用大的多的空间，
###### 存入数据使用setItem（），接受两个参数，第一个是键名，第二个是要保存的数据。
###### 读取数据使用getItem（），接受一个参数，键名
###### 清除数据用removeItem（），接受一个参数，键名
###### clear（）用来清除所有保存的数据
###### 当粗存的数据发生“storage”事件
###### 浏览器安全的基石是同源策略（same-origin policy）


## js执行过程
1. 语法分析
2. 预编译
3. 解析执行
4. 预编译过程
5. 创建AO对象
6. 找形参和变量声明，将变量和形参名变为AO属性值，值为undefined
7. 将实参值和形参统一
8. 在函数体里找函数声明，值赋予函数体

###### 数字 0、一个空字符串 ""、null、undefined 和 NaN 都会转换成 false。因为他们被称为 “falsy” 值。
###### 其他值变成 true，所以它们被称为 “truthy”。

## number 类型转换规则：
| 转化前 | 转化后 |
| :----: | :----: |
| undefined | NaN |
| null | 0 |
| true/false | 1/0 |
| string | 去掉首尾空格后的纯数字字符串中含有的数字。如果去掉空格后的字符串只由空格字符组成，返回 0。如果字符串不是纯数字，则返回 NaN |

