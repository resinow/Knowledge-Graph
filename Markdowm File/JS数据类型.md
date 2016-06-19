# JS数据类型

## Undefined

### 只有一个值：undefined，变量不需要显性设置为undefined值

### 声明但未初始化的变量和未声明的变量都返回undefined

## Null

### 空对象指针，只有一个值null

### typeof 返回"object"，准备用于保存对象的变量初始化时最好为null

### undefined值派生自null值，undefined==null返回true

## Boolean

### 两个字面值true和false，ECMAScript中所有类型的值都有与这两个值等价的值

### 不同数据类型转换为Boolean

#### String类型：任何非空字符串可转换为true，""(空字符串)转换为false

#### Number：任何非零数字值可转换为true，0和NaN转换为false

#### Object：任何对象可转换为true，null转换为false

#### Undefined：n/a（not applicable，“不适用”）可转换为true，undefined可转换为false

## Number

### 整数

#### 进制表示格式

##### 十进制

##### 八进制字面值第一位为0，然后是八进制数字序列（0~7）

##### 十六进制前两位为0x，后面跟十六进制数字（0~f），字母大小写都可以

#### 进行算术计算时所有以八进制和十六进制表示的数值都将被转换为十进制

### 浮点数值

#### 浮点数值必须有一个小数点，小数点后必须有至少一位小数，最高精度是17位小数

#### e表示法（科学记数法）：3.125e7=3.125*10^7=31250000

#### 浮点数值计算会产生舍入误差如0.1+0.2=0.30000000000000004不等于0.3，所以不要用特定浮点数值进行测试

### NaN（非数值）

#### 表示一个本来要返回数值的操作数未返回数值的情况

#### 任何涉及NaN的操作都会返回NaN，同时NaN与任何数值包括自身都不相等（NaN==NaN返回false）

#### isNaN()函数：接收一个值后，尝试将其转换为数值。不能被转换为数值的值会导致这个函数返回true

### 数值转换函数

#### parseInt()

#### Number()

#### parseFloat()

## String

### 以引号（单双引号都可以但是要配对）表示

### 字符串一旦创建，值就不可变

### 转换为字符串

#### toString()方法，适用于数值、布尔值、对象和字符串值

##### 调用数值的toString()方法时可以传递一个参数，来输出以二进制、八进制等进制格式表示的字符串

## Object

## typeof操作符

### 返回给定变量的数据类型

### var message="some string"; alert( typeof message);alert( typeof 110);

## 引用类型（对象定义）

### Object类型 

#### 创建方法

##### 使用new操作符跟Object构造函数

###### var person=new Object(); person.name="Nick"; person.age=29;

##### 对象字面量表示法

###### var person={ name: "Nick", age:29}; 花括号内可以为空，属性名可以使用字符串如"name": "Nick"

#### 访问方法

##### 点表示法 person.name

##### 属性名中包含易导致语法错误的字符或使用变量时可以用方括号表示法 person["first name"]

### Array类型

#### 数组的每一项可以保存任何类型的数据

#### 创建方法

##### 使用Array构造函数

###### var colors= new Array(); new操作符可省略，可以给构造函数传递要保存的项目数量，该数量会自动成为length属性的值

##### 数组字面量表示法

###### var colors=["red", "blue", "green" ]

#### 数组的length属性可以修改，通过设置这个属性可以从数组末尾移除或添加项

##### 利用length属性的值也可以方便地添加新项，因为数组最后一项的索引始终是length-1

##### var colors=["red", "blue", "green" ]; colors[colors.length]= "black"; colors[colors.length]= "brown";

#### 检测方法

##### Array.isArray()

##### instanceof只适用于一个全局执行环境

#### 转换方法

##### toLocaleString()/toString()/valueOf()

#### 栈方法（Last-In-First-Out后进先出）

##### push()方法：接受任意数量的参数，逐个添加到数组末尾并返回修改后的数组长度

##### pop()方法：从数组末尾移除最后一项，减少数组的length值并返回移除的项

#### 队列方法FIFO（先进先出）

##### shift()方法：移除数组中的第一个项，减少数组长度并返回移除的项

##### shift()方法和push()方法合用可以像使用队列一样使用数组

##### unshift()方法：在数组前端添加任意个项并返回数组的length

##### unshift()方法与pop()方法合用可以从反方向模拟队列

#### 重排序方法

##### reverse()方法：反转数组项的顺序

##### sort()方法：按升序排列数组项

###### 通过调用每个数组项的toString()方法来比较得到的字符串，很多情况下不符合要求

###### 可以接收一个比较函数作为参数，方便指定数组项排序

#### 操作方法

##### contact()方法基于当前数组所有项创建一个新数组

###### var colors2=colors1.concat("yellow", ["black", "brown"]); 返回新构建的数组

##### slice()方法基于当前数组的一个或多个项创建一个新数组

###### var colors2=colors1.slice(1);一个参数情况下返回该参数指定位置到当前数组末尾所有项

######  var colors3=colors1.slice(1, 4); 两个参数情况下返回起始位置和结束位置之间的项，不包括结束位置的项

##### splice()方法

###### 删除

####### 指定2个参数：要删除的第一项的位置和要删除的项数，删除任意数量的项

######## .splice(1, 4);

###### 插入

####### 指定3个参数：起始位置、0（要删除的项数）、要插入的项

######## .splice(2, 0, "yellow", "orange");

###### 替换

####### 指定3个参数：起始位置、要删除的项数、要插入的项

#### 位置方法

##### indexOf()方法

###### 接收两个参数，分别表示要检索的项和索引起始位置

##### LastindexOf()方法

###### 同上

#### 迭代方法

##### every()

##### filter()

##### forEach()

##### map()

##### some()

#### 归并方法

### Date类型

#### 创建方法

##### 使用new操作符和Date构造函数

###### var now= new Date();

###### 传参数的方法

####### Date.parse()方法

######## 接受一个表示日期的字符串，尝试根据字符串返回相应日期的毫秒数，未定义支持的日期格式

######## var someDate= new Date(Date.parse("May 25, 2004")); 如字符串不能表示日期，返回NaN

######## var someDate=new Date("May 25, 2004);直接将表示日期的字符串传给Date函数会在后台直接调用Date.parse()方法

####### Date.UTC()方法

######## var someDate=new Date(Date.UTC(2005,4,5,17,55,55));

######## 参数分别是年、月、日、小时、分钟、秒、毫秒等，其中月份从0开始

######## 也可以直接将表示日期的字符串传给Date函数

##### Date.now()返回表示调用这个函数的日期和时间
