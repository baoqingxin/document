# 知识点整理
## HTML标签
1. `<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">`

    Edge模式告诉IE以最高级 模式渲染文档，也就是任何IE版本都以当前版本所支持的最高级标准模式渲染，避免版本升级造成的影响。这个插件可以让用户的IE浏览器外不变，但用户在浏览网页时，实际上使用的是Google Chrome浏览器内核，而且支持IE6、7、8等多个版本的IE浏览器
 2. 浏览器内核控制标签meta说明(360浏览器)

    浏览器默认内核的指定只需在head标签中添加一行代码即可：<br/>
    若页面需默认用极速核，增加标签：`<meta name="renderer" content="webkit">`<br/>
    若页面需默认用ie兼容内核，增加标签：`<meta name="renderer" content="ie-comp"> `<br/>
    若页面需默认用ie标准内核，增加标签：`<meta name="renderer" content="ie-stand"> `<br/>
    content的取值为webkit,ie-comp,ie-stand之一，区分大小写，分别代表用webkit内核，IE兼容内核，IE标准内核。点击查看[http://se.360.cn/v6/help/meta.html](http://se.360.cn/v6/help/meta.html, "点击查看")  

## CSS
1. css预处理器
   - Sass  
      sass有两种写法，分别以`.sass`和`.scss`为拓展名。Sass 兼容 css ，你可以在 sass 文件里写 css，也可以严格按照 sass 的缩进方式省去「大括号」和「分号」，最终它们都会被编译成标准 css。  
      scss是css拓展语法，sass是缩进语法。
      ### 用法
      
   - Less  
      Less 受 Sass 的影响非常大，以「 *.less 」为扩展名，是 sass 之后的又一款优秀的 css 预处理器。  
      - 变量：就像写其他语言一样，免于多处修改。
      - 混合：class 之间的轻松引入和继承。
      - 嵌套：选择器之间的嵌套使你的 less 非常简洁。
      - 函数&运算：就像 js 一样，对 less 变量的操控更灵活。
   - Stylus  
      相比于 sass 的激进和 less 的常规，Stylus 是一个高效、动态以及丰富的 CSS 预处理器。它同时支持缩进的和通俗的两种风格的 CSS 语法风格。

Stylus 扩展名为「 *.styl 」，跟另外两款 css 预处理器相比略显年轻，社区以及推广程度也不及 sass 和 less，但它的一些优秀特性同样令人着迷。

## JavaScript
1. 按位非运算符"~" 
   位运算 NOT 由否定号（ ~ ）表示，它是 ECMAScript 中为数不多的与二进制算术有关的运算符之一。  
   位运算 NOT 是三步的处理过程：  
      - 把运算数转换成 32 位数字  
      - 把二进制数转换成它的二进制反码（0->1, 1->0）  
      - 把二进制数转换成浮点数  

   简单的理解，对任一数值 x 进行按位非操作的结果为 -(x + 1)，~~x就为 -(-(x+1) + 1)  
   判断数值中是否有某元素时，以前这样判断：
   ```
   if(arr.indexOf(ele) > -1){...} // 易读
   if(~arr.indexOf(ele)){...} // 简洁 
   ```
   对于浮点数，~~value可以代替parseInt(value)，而且前者效率更高些
   ```
   parseInt(-2.99) // -2
   ~~(-2.99) // -2
   ```
2. `includes(searchElement， fromIndex)`方法(数组)  
   用来判断一个数组是否包含一个指定的值，如果包含则返回 true，否则返回false。
   ```
   var arr = [1, 2 ,3]
   console.log(arr.includes(2)) // true
   
   ```