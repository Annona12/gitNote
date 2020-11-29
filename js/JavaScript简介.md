### JavaScript简史
---
>    `JavaScript的用途不再局限于简单的数据验证，而是具备了与浏览器窗口及其内容等几乎所有方面交互的能力。`

### JavaScript的实现
---
一个完整的 JavaScript 实现应该由下列三个不同的部分组成：
- [ ] `核心（ECMAScript）`
- [ ] `文档对象模型（DOM）`
- [ ] `浏览器对象模型（BOM）`
1. `ECMAScript`
- 语法
- 类型
- 语句
- 关键字
- 保留字
- 操作符
- 对象
(ECMAScript 就是对实现该标准规定的各个方面内容的语言的描述。)
- ECMAScript兼容
ECMA-262 给出了 ECMAScript 兼容的定义。要想成为 ECMAScript 的实现，则该实现必须做到：
- 支持 ECMA-262 描述的所有“类型、值、对象、属性、函数以及程序句法和语义”（ECMA-262
第 1 页）
- 支持 Unicode 字符标准。
此外，兼容的实现还可以进行下列扩展。
- 添加 ECMA-262 没有描述的“更多类型、值、对象、属性和函数”。ECMA-262 所说的这些新增
特性，主要是指该标准中没有规定的新对象和对象的新属性。
- 支持 ECMA-262 没有定义的“程序和正则表达式语法”。（也就是说，可以修改和扩展内置的正
则表达式语法。）
---
2. `DOM`
- (1)文档对象模型（DOM，Document Object Model）是针对 XML 但经过扩展用于 HTML 的应用程序编
程接口（API，Application Programming Interface）
- (2)DOM级别
DOM1级:
- 核心（DOM Core）：DOM 核心规定的是如何映射基于 XML 的文档结构，以便
简化对文档中任意部分的访问和操作；
- DOM HTML：DOM HTML 模块则在 DOM 核心的基础上加以扩展，添加了针
对 HTML 的对象和方法
DOM2级：DOM2 级在
原来 DOM 的基础上又扩充了（DHTML 一直都支持的）鼠标和用户界面事件、范围、遍历（迭代 DOM
文档的方法）等细分模块，而且通过对象接口增加了对 CSS（Cascading Style Sheets，层叠样式表）的
支持
- DOM 视图（DOM Views）：定义了跟踪不同文档（例如，应用 CSS 之前和之后的文档）视图的
接口；
- DOM 事件（DOM Events）：定义了事件和事件处理的接口；
- DOM 样式（DOM Style）：定义了基于 CSS 为元素应用样式的接口；
- DOM 遍历和范围（DOM Traversal and Range）：定义了遍历和操作文档树的接口。
DOM3级：则进一步扩展了 DOM，引入了以统一方式加载和保存文档的方法——在 DOM 加载和保存（DOM Load and Save）模块中定义；新增了验证文档的方法——在 DOM 验证（DOM Validation）模块中定义。DOM3 级也对 DOM 核心进行了扩展
---
3. `BOM`
BOM 只处理浏览器窗口和框架；但人们习惯上也把所有针对浏览器的 JavaScript 扩展算作 BOM的一部分。下面就是一些这样的扩展：
- 弹出新浏览器窗口的功能；
- 移动、缩放和关闭浏览器窗口的功能；
- 提供浏览器详细信息的 navigator 对象；
- 提供浏览器所加载页面的详细信息的 location 对象；
- 提供用户显示器分辨率详细信息的 screen 对象；
- 对 cookies 的支持；
- 像 XMLHttpRequest 和 IE 的 ActiveXObject 这样的自定义对象