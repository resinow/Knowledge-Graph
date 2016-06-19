# CSS3

##  opicity 和 rgba的区别

### opacity只能设定整个元素的透明值，而alpha通道可以特定对元素的某个属性设定透明值，比如上面的背景、边框、文字等

## transform变形

### transform: rotate(angle); 旋转

#### 如：transform: rotate(9deg)

### transform: translate(length); 平移

#### transform: translate(100px,50px); 水平垂直同时移动

#### transform: translateX(100px); 水平移动

#### transform: translateY(50px); 垂直移动

### transform: scale(number); 缩放

#### transform: scale(2,1.5); 水平垂直同时缩放

#### transform: scaleX(2); 水平缩放

#### transform: scaleY(2); 垂直缩放

### transform: skew(angle); 扭曲

#### transform: skew(30deg,10deg); 水平垂直同时扭曲

#### transform: skewX(30deg); 水平扭曲

#### transform: skewY(30deg); 垂直扭曲

### transform: matrix(<number>,<number>,<number>,<number>,<number>,<number>); 矩阵

### transform-origin(X,Y): length; 改变元素变换基点

## rem单位

### font size of the root element

#### px、em、rem的区别

##### px，像素，相对长度单位，相对于屏幕分辨率

##### em，相对长度单位，相对父节点的字体尺寸，如未设置则相对于浏览器默认字体尺寸

###### 一般浏览器默认值为16px

##### rem仍然是相对长度单位，但只相对于HTML根元素

#### 通过修改根元素就可以成比例地调整所有字体尺寸

#### 设置 html{ font-size: 10px; } 则1rem=10px

## fixed布局

### 任何一个容器都可以指定为Flex布局 display: flex;

### 行内元素也可以指定为Flex布局 display: inline-flex;

### 设置为flex布局后子元素的float、clear、vertical-align属性将失效

### 采用flex布局的元素称为flex container，简称容器，它的所有子元素自动成为容器成员，称为flex item，简称项目

#### 容器默认存在两根轴

##### 水平的主轴（main axis），开始位置为main start，结束位置为main end

##### 垂直的主轴（cross axis），开始位置为cross start，结束位置为cross end

##### 项目默认按主轴排列

##### 单个项目占据的主轴空间叫做main size，占据的交叉轴空间叫做cross size

#### 可以在容器上设置6种属性

##### flex-direction

###### flex-direction决定主轴的方向（即项目的排列方向）

####### flex-direction: row; 默认值，主轴水平方向，以左端为起点

####### flex-direction: row-reverse;  主轴水平方向，以右端为起点

####### flex-direction: column; 主轴垂直方向，以左端为起点

####### flex-direction: column-reverse; 主轴垂直方向，以右端为起点

##### flex-wrap

###### flex-wrap定义如何换行

####### flex-wrap: nowrap; 默认值，不许换行

####### flex-wrap: wrap; 换行，第一排在上方

####### flex-wrap: wrap-reverse; 换行，第一排在下方

##### flex-flow

###### flex-direction和flex-wrap的缩写

####### flex-flow:<flex-direction> <flex-wrap>; 如flex-flow: row-reverse nowrap; 

##### justify-content

###### justify-content定义在主轴上的对齐方式

####### justify-content: flex-start; 默认值，左对齐

####### justify-content: flex-end; 右对齐

####### justify-content: center; 居中

####### justify-content: space-between; 两端对齐

####### justify-content: space-around; 项目之间间隔相等

##### align-items

###### align-items定义在交叉轴上的对齐方式

####### align-items: flex-start; 交叉轴起点对齐

####### align-items: flex-end; 交叉轴终点对齐

####### align-items: center; 交叉轴中点对齐

####### align-items: baseline; 第一行文字的基线对齐

####### align-items: stretch; 默认值，若项目未设置高度或为auto，将占满整个容器高度

##### align-content

###### align-content定义多根轴的对齐方式

####### flex-start、flex-end、center、space-between、space-around、stretch（默认值）

#### 可以在项目上设置6种属性

##### order

###### order定义项目的排列顺序

####### order: <integer>; 数值越小排列越靠前，默认值0

##### flex-grow

###### flex-grow定义项目的放大比例

####### flex-grow: <number>; 默认为0

##### flex-shrink

###### flex-shrink定义项目的缩小比例

####### flex-shrink: <number>; 默认为1，负值无效

##### flex-basis

###### flex-basis定义在分配空余空间之前项目占据的主轴空间

####### flex-basis: <length>; ，默认值为auto

##### flex

###### flex-grow、flex-shrink和flex-basis的缩写

####### flex: <flex-grow> <flex-shrink> <flex-basis>; 建议优先使用这个属性

##### align-self

###### align-self允许单个项目拥有与其他项目不同的对齐方式，可覆盖align-items

####### 可取6个值，除了默认值auto都与align-items相同

## animate动画

### animate是一个简写属性，用于设置6大动画属性

#### animate-name 规定@keyframes动画名称

##### animate-name: keyframename; 动画名称

##### animate-name: none; 无动画效果，可用于覆盖来自级联的动画

#### animate-duration: time; 一个动画周期持续的时间，默认值为0

#### animation-timing-function 速度曲线

##### ease，默认值，以低速开始加速，结束前变慢

##### ease-in，以低速开始

##### ease-out，以低速结束

##### ease-in-out，以低速开始结束

##### linear，整个过程速度不变

##### cubic-bezier(n,n,n)，以cubic bezier函数来生成一个速度函数，可能的值是1到0

#### animation-delay:time; 何时开始，允许负值

#### animation-iteration-count播放次数

##### n，播放次数，默认值1

##### infinite，无限次播放

#### animation-direction规定动画在下一周期是否逆向播放

##### normal，默认值，正常播放

##### alternate，轮流反向播放

### animation-play-state规定动画正在运行还是暂停

#### paused，已暂停

#### running，正在播放

### @keyframes规则创建动画

#### @keyframes keyframename{ keyframes-selector{css-styles;}} 

##### 如：@keyframes myfirstmove{ 0%{ top:0px; background:red; } 100%{ top:100px; background:yellow; }}

### animation-fill-mode规定动画在播放之前或之后，其动画效果是否可见

#### none，不改变默认行为

#### forwards当动画完成后，保持最后一个属性值（在最后一个关键帧中定义）

#### backwards在 animation-delay 所指定的一段时间内，在动画显示之前，应用开始属性值（在第一个关键帧中定义）

## transition过渡

### transition是一个简写属性，用于设置4个过渡属性

#### transition-property: width; 用于设置产生变形的CSS属性

#### transition-duration: time; 用于设置过渡时间，是必须设置的，否则不会产生过渡效果

#### transition-timing-function类似于animate-timing-function

#### transition-delay: time; 效果开始前需要等待的时间

## media queries

### 工作方式

#### 直接在link中判断设备尺寸然后引用不同的css文件

##### <link rel="stylesheet" type="text/css" href="#" media="screen and (min-width:400px ) and (max-width:600px)">

#### 直接写在<style>标签里

##### @media screen and (max-width:600px){ } 

### media属性中

#### 十种media type：all、screen、print、tv、handheld等

#### 关键字：and、only（限定某种媒体）、not（排除某种媒体）

#### 媒体特性，放在一对（）中，如(min-width:600px)
