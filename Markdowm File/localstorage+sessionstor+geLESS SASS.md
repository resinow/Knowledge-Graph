# localstorage sessionstorage 
LESS SASS

## web Storage

### 类型

#### localStorage

##### 持久化的本地储存

#### sessionStorage

##### 临时的本地储存，随着页面关闭会清空

### 操作

#### setItem()储存value

##### 示例

###### sessionStorage.setItem( "key", "value" );

###### localStorage.setItem("site", "js8.in");

#### getItem()获取value

##### 示例

###### sessionStorage.getItem( "key");

###### localStorage.getItem("site");

#### removeItem()删除key

##### 示例

###### sessionStorage.removeItem( "key");

###### localStorage.removeItem("site");

#### clear()清除所有的key/value

##### 示例

###### sessionStorage.clear();

###### localStorage.clear();

#### 像普通对象一样用点(.)操作符，及[]的方式进行数据存储

##### var storage = window.localStorage; storage.key1 = "hello"; storage["key2"] = "world"; console.log(storage.key1); console.log(storage["key2"]);

#### localStorage和sessionStorage的key和length属性实现遍历

##### var storage = window.localStorage; for (var i=0, len = storage.length; i  <  len; i++){     var key = storage.key(i);     var value = storage.getItem(key);     console.log(key + "=" + value); }

#### storage事件

## CSS预处理器

### 一种用来为 CSS 增加一些编程特性的语言

### LESS & SASS

#### 声明变量

##### 在整个样式单中使用变量，修改时只需要修改一个地方

##### SASS 的变量名使用 $ 符号开始

###### $mainColor: #0982c1; 

##### LESS 的变量名使用 @ 符号开始

###### @mainColor: #0982c1; 

##### $mainColor: #ccc; body{ border:1px $mainColor solid;}

#### 允许嵌套

##### 减少代码，父子节点关系一目了然 

###### section{ color: #ccc; nav{ color:#666; a{ color:#999; } } }

#### Mixins (混入)

##### 某段 CSS 经常需要在多个元素中使用时可以为这些共用的 CSS 定义一个 Mixin，在需要引用这些 CSS 的地方调用该 Mixin

##### SASS

###### @mixin error($borderwidth: 2px; ){ border:$borderwidth solid #ccc; } .login{ left: 12px; @include error(5px); }

##### LESS

###### .error(@borderwidth: 2px; ){ border:@borderwidth solid #ccc; } .login{ left: 12px; .error(5px); }

#### 继承（注意优先级）

##### SASS

###### .block{ margin:10px 20px;} ul,ol{ @extend .block; color:#ccc; }

##### LESS

###### 类似于mixins

####### .block{ margin:10px 20px;} ul,ol{ .block; color:#ccc; }

#### 导入

##### @import "css.css"; @import"file.{type}';

#### 颜色函数

##### CSS 预处理器一般会内置一些颜色处理函数用来对颜色值进行加亮、变暗、颜色梯度等处理。

###### SASS

###### LESS

#### 运算符

##### 可以直接在 CSS 预处理器中进行样式的计算

### 前端构建工具

#### gulp

#### grunt

#### webpack（页面打包工具，具有一部分构架工具的功能）
