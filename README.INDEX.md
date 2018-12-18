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