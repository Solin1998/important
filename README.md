# important
前端笔记
configuration：控制删除和修改
enumerable:控制遍历
object.seal 防扩展 防删除
object.seal(obj).
function(){};记得加引号
------------------------
1-22
call和apply比如三个数字和不同变量直接的差别

bind是永久绑定 不能更改

let与for循环可以形成闭包的效果

arguments=参数！
bind=捆绑！

javascript中的obj到底什么意思？

你这里obj 说白了就是 
document.getElementById(whichlink + "menu")
这里相当于把document.getElementById(whichlink + "menu")
的值赋给obj  
一个变量而已

            
如果 obj 不是 Function 的话，根本不存在 obj.prototype。
其实关键问题是你要分清楚类和实例。类在 JavaScript 里面其实就是作为 constructor 的那个 Function。类是有 prototype 的。
实例则是 constructor 执行返回的那个 Object。
这个 Object 有个非标准的属性 __proto__ 指向 constructor 的 prototype，但它自己没有 prototype。处。
http://www.w3school.com.cn/jsref/jsref_prototype_array.asp
对象解构：属性对属性
------------------------
prev=previous
val=value

DOM =document object model

DOM API属于原生的JS
每个节点都是NODE类型的对象

一般不拿属性节点当节点看
------------------
HTML代码片段  elem.innerHTML 获取源代码
纯文本内容	elem.textContent 获取文本内容
表单元素的值 elem.value

string 和数组API不通用！！！

+= x+=y x=x+y x=15

变为字符串最有效的办法是加空字符串！！

从Unicode号逆向转回字


var char=String.fromCharCode(u);

20170262020005100048000560003200119000560005200117

--------------------
下取整首选parseInt
上取整 Math.ceil

n.toFixed(d);
d=小数位数

！！！！控制台蓝色是数字，黑色一般为字符串
------
听到了DAY2 JS下午32分钟!
判断质数只要小于平方根！

函数

参数：定义参数要函数是否需要！！

返回值：调用者是否需要执行结果！

整体称为声明！！

用let 代替var 来解决变量var 声明提前
原理：再LET前面不准存在未声明的变量

var 函数名=function

arguments一般只用在重载时

return a-b:!!
因为sort()函数使用的是冒泡排序，冒泡排序会重复地走访要排序的数列，一次比较两个元素，如果他们的顺序错误就把他们交换过来，一直重复地进行直到说该数列已经排序完成。
如果a-b>0(即正数)就把a和b的位置交换，也就是较小的一个数会排到前面；
如果b-a>0就把a和b的位置交换，也就是较大的一个数会排到前面。

不加cmp（）;//给的意思
即整个函数给你 不是只调用一次
几乎所有的匿名函数就是回调函数
比如这个cmp放在window里面！！！！
仔细看图 非常经典
-----------------
变量的使用 优先使用活动对象中的局部变量

局部变量不可重用

活动对象=函数作用域
window=全局作用域

看到function就会在内存中创建一个function地址的感觉

main（）==》永远引用window

闭包比普通函数占用内存空间 即那个AO!!

有东西指向就不能走 ！

释放闭包 将保存内存函数的变量 赋值为null；

 参数和var 都是局部变量

闭包把变量和函数绑在一起

如果给一个不带var 的变量强行赋值 那么会在全局创建该变量！！
04-下午121分钟
-------------------------
没有.的变量只能从作用域中找
在对象中找必须加.
调用前 .前是谁 那么this就指向谁
JS一切对象底层都是关联数组

用for in 遍历对象每个属性！

构造函数就像是户型图

继承是因为代码重用和节约内存
JS中继承都是继承原型对象!

定义构造函数 赠送原型对象

构造函数.prototype.成员名=值/function（）{}；

prototype==老公 	__proto__==爹

构造函数定义属性结构
prototype原型对象保存方法对象
、

JS中内置对象/内置类型的原型对象（即JS已经帮你创建好了的）：
String Number Boolean
Array Date RegExPMath
 Error Function Object 
Global
(背诵)
API 都由构造函数和原型对象组成

wwwh回答方式
what why when how 

window 是一个全局对象 无需创建 不是构造函数 也没有原型对象

indexof（3，3）从3位置开始找3

||0 在变量中经常做默认值

this只有在调用的时候在知道自己指向的是谁！

object原型对象是所有对象的祖宗

作用域链和原型链！！！

Array.prototype.isPrototype0f(obj);
判断是不是某个obj的父对象

instance 实例 情况

找DNA class属性即 用toString

多态：1重载overload 
    2重写override

call（）抢：让一个对象强行调用，本来无法调用到的任何函数

重写call

两种类型间包含相同的的属性和方法时 抽象出一个公共的父类型
记得查找抽象父类型

prototype 属性使您有能力向对象添加属性和方法
飞机小程序 day5最后call

arguments.callee 可自动获取当前函数名
专门做递归调用

递归都用循环代替
------------------------------------
解构下标对下标

按值传递 for of是按值传递

使用DOM来操作网页API

查找-修改-添加/删除

DOM 网页中一切内容都是节点对象

nodeName! 节点类型的检查

---------
jquery
中$就是new 创建对象的意思


ul,li{}：设置所有ul和li元素的样式
 <style>
    ul,li{color:red}
</style>
<ul><li>红色</li></ul>
<ol><li>红色</li></ol>

ul li{}：只设置ul下的li元素
 <style>
    ul li{color:red}
</style>
<ul><li>红色</li></ul>
<ol><li>浏览器默认颜色，黑色，而不是红色</li></ol>

ul>li{}：设置ul标签下的直接li元素，这个样式没多大意义，因为ul的合法子元素是li，应该用其他元素来举例好点，不过你硬要插入不合法元素也可以，如下面的
 <style>
    ul>li{color:red}
</style>
<ul>
    <li>红色</li>
    <div>
        <li>黑色</li>
    </div>
</ul>

直接子元素示例你可以看这个多明显
 <style>
    div>b{color:red}
</style>
<div>
    <b>红色</b>
    <span><b>黑色</b></span>
</div>


--------------------
table>(thead>tr>td*4)+(tbody>tr*4>td*4)！！
回车快捷打表格
+号表示同意级别 td就是一个个的格子
tr 行

--------------
#是ID 
.是class！！！

attr 属性

data-toggle










 





























