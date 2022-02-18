# 4．Js规范：

（1）Js中一致都使用单引号’ ’或者反引号\`\`，而不是使用双引号

&#x20;                 例如 Var name = ‘  ’

（2）      在wxml、wxss、 json 中均使用双引号””

（3）变量命名采用小驼峰命名法---即首字母小写，后每个单词首字母大写

推荐写法 (var myBlogAddress = ‘ ’)   不推荐写法（var myblogaddress = ‘’）

（4）常量命名采用全字母大写命名，以便于与变量区分

推荐写法：常量  （const  PI = 3.141592653）   变量  （let  name = ' '）

（5）函数命名使用小驼峰命名法，条件允许情况下请采用动词前缀方式，确保表达正确意义。

&#x20;        推荐写法 changeColor:function(){}   不推荐写法 changecolor:function({})

（6）在Page的页面中，系统默认的方式如onLoad: function () {}

&#x20;        自定义的方法统一使用  变量名：function(){}

推荐写法：changeValue:function(){}

&#x20;        （7）判断

&#x20;                 比较运算符，推荐使用 '===' 与 '!==' 。

&#x20;                 推荐写法:

if（username===’ ’）{

console.log(‘用户名为空’)

}

If (username !== ’ ’){

&#x20;        Console.log(“用户名为：”+username)

}

&#x20;                 当判断非空时，“!变量”需要考虑变量不为数值0。

&#x20;                         Var a=0;

If(a.toString()==’ ’)    //这一行代码就会判断它是false 因为0与’ ’转换成布尔值都是false

&#x20;        （8）循环

若循环中需使用函数，请将函数定义在循环外部而非内部，这样可以避免函数的反复创建。

推荐写法:

&#x20;let demo = function (i) {

&#x20;       console.log(i)

&#x20;   },

&#x20;   i = 0,

&#x20;   arr = \[1, 2, 3],

&#x20;   len = arr.length;

for (; i < len; i++) {

&#x20;   demo(i);

};

不推荐写法：

let arr = \[1, 2, 3],

&#x20;   i = 0,

&#x20;   len = arr.length;

for (; i < len; i++) {

&#x20;   let demo = function () {

&#x20;       console.log(i);

&#x20;   };

&#x20;   demo();

};

（9）点击事件的命名尽量都起的有意义，知道是什么效果。

&#x20;        例如 改变颜色 changeColor()  改变状态changeStatus()
