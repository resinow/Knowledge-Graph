# Javascript 语法

## 数据类型

JS中有5种简单数据类型，也称基本数据类型和一种复杂数据类型Object

### Null

#### 表示一个空指针对象，运用typeof检测会得到object返回值

### Undefined

#### 表示未定义或为赋值的变量

### Boolean

#### .toString()

### Number

#### 原生方法

##### .toPrecision(number)

##### .toExponential(number) 返回指数表示法的字符串，参数用来指定输出结果中的小数位数

##### .toFixed(number) 返回指定小数位数（number）的字符串

##### .toString(进制)

#### 相关方法

##### isNaN(param)

##### Number(param)

##### parseInt(param)

### Object

### String

#### 方法

##### .indexOf(string) 指定字符首次出现的位置

##### String.fromCharCode(字符编码)  将字符编码转换为字符串

##### 正则匹配

##### .toLowerCase()/.toLocaleLowerCase()

##### .toUpperCase()/.toLocaleUpperCase()

##### .trim() 去掉字符串首尾空格

##### .lastIndexOf(string) 指定字符最后一次出现的位置

##### .localeCompare(string) 和传入的string比较首字符在字母表中的先后顺序

##### .substr(startIndex,length)

##### .substring() 同上

##### .slice(startIndex,endIndex) 切割字符串生成新的字符串

##### .concat(string) 拼接字符串

##### .charCodeAt(index)

##### .charAt(index)

#### 属性

##### .length

## 引用类型

### Object

### Array

### Date

### Regexp

### Function
