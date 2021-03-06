## Interview <img src="https://img.shields.io/badge/license-MIT-brightgreen" alt="license">

- [前端面试知识点目录整理](#前端面试知识点目录整理)
- [前端工程师的自检清单](#前端工程师的自检清单)
- [前端基础拾遗90问](https://juejin.im/post/5e8b261ae51d4546c0382ab4#heading-81)
- [雅虎前端优化的35条军规](https://www.cnblogs.com/xianyulaodi/p/5755079.html)
- [100道+ JavaScript 面试题](https://github.com/Wscats/articles)
- [58 道 Vue 常见面试题集锦](https://mp.weixin.qq.com/s/Nn8AqyW9rrFrsfD_PPT-vg)
- [前端面试题全面整理-带解析 涵盖CSS、JS、浏览器、Vue、React、移动web、前端性能、算法、Node](https://mp.weixin.qq.com/s/MMKYq96EJhbiiHtWH7GP4g)
- [思维导图](#思维导图)
- [摘要](#摘要)
- [书籍](#书籍)
- [其他](#其他)
    

> 面试题总结

## <a id="前端面试知识点目录整理">前端面试知识点目录整理</a>

## 基本功考察

### 一、关于Html
- 1.html语义化标签的理解、结构化的理解；能否写出简洁的html结构；SEO优化。
- 2.h5中新增的属性，如自定义属性data、类名className等；新增表单元素；拖拽Drag。
- 3.h5中新增的API、修改的API、废弃的API稍作了解（离线存储(Storage)、audio、video）。
### 二、关于CSS
- 1.CSS选择器（三大特性）。  
  `继承性 优先级 层叠性`  
- 2.BFC机制。
- 3.盒模型。
- 4.CSS模块化开发（封装）；SCSS和LESS的使用。
- 5.屏幕适配以及页面自适应。  
  `meta  rem+js  @media  %`  
- 6.CSS3中新增的选择器。  
  `属性  结构伪类  状态伪类  其他`  
- 7.CSS3中新增的属性，transform、trasition、animation等。  
### 三、关于布局
- 1.标准文档流（padding + margin + 负margin）+ 浮动float + 定位 left + right + top + bottom。
- 2.百分比布局：px单位用%num代替，占父级元素的百分比。
- 3.flex弹性布局：主轴、辅助轴的几个属性。
- 4.grid栅格布局：使用框架中的类名来替代，本质上还是百分比布局。
### 四、关于JS基础
- 1.变量数据类型及检测：基本 + 引用。
- 2.运算符：算术 + 条件 + 逻辑 + 位 + 短路、隐式转换等。
- 3.条件、循环、异常处理if、switch(){case xxx:}、try、catch、finally、throw。
- 4.函数定义、调用方式（apply、call、直接调用）；传参：实参给形参赋值。
- 5.字符串、数组、对象常用API。
- 6.正则表达式。
### 五、关于JS高级
- 1.作用域、作用域链、闭包。
- 2.原型、原型链、继承。
- 3.函数上下文、this指向。
- 4.js的运行机制、事件队列和循环。
- 5.Ajax原理、axios库。
- 6.同步、异步编程。
- 7.jQuery源码学习。  
### 六、关于浏览器
- 1.浏览器的构成和运行机制。  
　　a.HTML 解释器：将 HTML 文档经过词法分析输出 DOM 树。  
　　b.CSS 解释器：解析 CSS 文档, 生成样式规则。  
　　c.图层布局计算模块：布局计算每个对象的精确位置和大小。  
　　d.视图绘制模块：进行具体节点的图像绘制，将像素渲染到屏幕上。  
　　e.JavaScript 引擎：编译执行 Javascript 代码。  
- 2.浏览器内核。  
`Trident（IE）、Gecko（火狐）、Blink（Chrome、Opera）、Webkit（Safari）`  
- 3.浏览器交互：BOM和DOM相关webApi、监听事件。
- 4.浏览器缓存机制。  
见./image  
- 5.浏览器的渲染原理。  
  1. 解析 HTML
在这一步浏览器执行了所有的加载解析逻辑，在解析 HTML 的过程中发出了页面渲染所需的各种外部资源请求，用HTML解释器生成DOM树。
  2. 解析CSS                                                                      用Css解析器解析css文件生成CSSOM树。
  3. 合并CSS和HTML
浏览器将CSS树与 DOM 树合并，最终生成页面 render 树（:after :before 这样的伪元素会在这个环节被构建到 DOM 树中）。
  4. 计算图层布局
页面中所有元素的相对位置信息，大小等信息均在这一步得到计算，布局渲染树。
  5. 绘制图层
在这一步中浏览器会根据我们的 DOM 代码结果，把每一个页面图层转换为像素，并对所有的媒体文件进行解码，绘制渲染树。
  6. 整合图层，得到页面
最后一步浏览器会合并合各个图层，将数据由 CPU 输出给 GPU 最终绘制在屏幕上。（复杂的视图层会给这个阶段的 GPU 计算带来一些压力，在实际应用中为了优化动画性能，我们有时会手动区分不同的图层）。
- 6.浏览器的安全性：跨域和攻击。  
`jsonp cors  XSS CSRF`  
### 七、关于网络协议
- 1.HTTP协议。
- 2.cookie、session、token。
  - token
    - 1.防止重复提交表单
    - 2.身份验证
### 八、关于ES6语法
- 1.字符串、数组、对象扩展的api。
- 2.变量扩展：let、const解构赋值，块级作用域。
- 3.函数扩展：箭头函数默认参数、rest参数。
- 4.展开运算符、模板字符串。
- 5.set和map数据结构。
- 6.迭代器和生成器函数next和yield的理解。
- 7.proxy对象属性代理器：属性的读取（get）和设置（set）相关操作。
- 8.promise对象、异步编程的解决方案。
- 9.async + await：异步编程的终极方案promise + generator的语法糖。
- 10.class语法、构造函数的语法糖。
- 11.模块化编程export + import的导出和导入。
### 九.VUE基础
- 1.基本指令。
- 2.实例的属性和方法。
- 3.实例的生命周期。
- 4.组件基础：创建、注册、添加属性方法、套用等。
- 5.组件通信传值，父子、兄弟、跨级。
- 6.插槽slot等。
## 十.VUE高级
- 1.vue-router：搭建SPA
  - 1.路由、组件的配置。
  - 2.路由间的传值。
  - 3.路由跳转。
  - 4.路由的导航守卫。
  - 5.记住在router.js和组件页面中的使用方式。  
- 2.vuex：状态管理、数据仓库store  
  - 1.state、getters、mutations、actions、modules。
  - 2.辅助函数mapState等，仓库中计算属性的映射、方便操作。
  - 3.记住在store.js插件和组件中使用方式[传送门](https://blog.csdn.net/xfcy514728/article/details/80278048)
    - 存储数据到本地浏览器
### 十一.VUE深入、源码阅读
- 1.数据响应式原理。
- 2.virtual dom。
- 3.diff 算法。
- 4.nextTick等等。
### 工程能力考察  

### 1、项目能力

- 1.vue-cli脚手架搭建和功能配置vue.config.js。

- 2.webpack的常用配置。

- 3.项目构建打包。

- 4.熟悉各类框架的文档。

- 5.UI框架：Bootstrap、MUI、Element-ui等。

- 6.常用的插件整理；整理一个自己插件库，封装自己的方法库、组件库。

- 7.常用的工具熟练度。

- 8.PC端和移动端开发注意事项。

- 9.经验总结：快速确定项目的技术选型。

- 10.坑点总结：项目遇到坑坑坑！

- 11.项目中的性能优化记录（都是细节点，多记录）。

- 12.需求文档的理解，可以结合项目流程图、UML图。

- 13.问题解决能力：bug定位调试、查找文档、寻求他人。

- 14.记录习惯养成。  
### 2.模块化、组件化开发能力
- 1.项目分类；各类文件整理、分类。
- 2.各类功能封装。
- 3.组件和功能模块的抽离、解耦、复用。
### 内功考察
- 1.面向对象的编程思想
  - 1.类的抽象。
  - 2.对象的封装、继承。
  - 3.为了更好的去管理数据、分类数据，实现高内聚、低耦合。  
- 2.设计模式  
  设计模式感觉也是将面向对象思想再度抽象成现实中某些特定模式。  
- 3.数据结构和算法  
  - 1.学习常用的排序搜索算法、顺序表、链表、栈、队列、树、堆等。
  - 2.考验你的抽象思维和数学功底。
  - 3.将现实需求抽象成计算机代码的思维能力。   
## 附加技能考察
- 1.学习能力
  - 1.持续学习的态度——博客、笔记记录。
  - 2.技术论坛活跃度高、问答多。
  - 3.GitHub开源项目参与。  
- 2.了解一门后端语言
  - 1.python、node.js、php等。
  - 2.数据库mysql、redis、mongodb；sql的操作语句、mongodb的操作语句、redis的操作语句。
  - 3.node + express搭建本地服务等。
  - 4.python + django + request + scrapy。  
- 3.系统编程   
  - 1.Linux命令行操作、系统文件管理。
  - 2.多任务、多线程、多进程、协程、并发、并行、串行、同步、异步等概念的理解。   

[前端面试知识点目录整理](https://segmentfault.com/a/1190000018603454)  

## <a id="前端工程师的自检清单">前端工程师的自检清单</a>

- 开篇  
  实际上，除了坚持学习的强大的自驱力，你还需要一个很简单的学习方法。那就是：建立自己的知识体系。它能帮助你更系统性的学习，同时你也时刻能知道自己哪些地方是不足的。
  我会把我工作和学习中接触到的知识全部归纳到我的知识体系中，其中不仅仅包括我已经学过的，还有很多我没有来得及学习的。
  这不仅仅是我的知识体系，更是我时刻提醒自己的自检清单。
  下面我会把我的自检清单分享给大家，你可以按照清单上的知识检测自己还有哪些不足和提升，我也建议大家建自己的知识体系，这样工作或者学习甚至面试时，你能快速定位到知识清单中的点，如果你有哪些我没归纳到的点，欢迎在评论区告诉我。

## JavaScript基础

#### 变量和类型

- 1.JavaScript规定了几种语言类型

- 2.JavaScript对象的底层数据结构是什么

- 3.Symbol类型在实际开发中的应用、可手动实现一个简单的Symbol

- 4.JavaScript中的变量在内存中的具体存储形式

- 5.基本类型对应的内置对象，以及他们之间的装箱拆箱操作

- 6.理解值类型和引用类型

- 7.null和undefined的区别

- 8.至少可以说出三种判断JavaScript数据类型的方式，以及他们的优缺点，如何准确的判断数组类型

- 9.可能发生隐式类型转换的场景以及转换原则，应如何避免或巧妙应用

- 10.出现小数精度丢失的原因，JavaScript可以存储的最大数字、最大安全数字，JavaScript处理大数字的方法、避免精度丢失的方法

#### 原型和原型链

- 1.理解原型设计模式以及JavaScript中的原型规则

- 2.instanceof的底层实现原理，手动实现一个instanceof

- 4.实现继承的几种方式以及他们的优缺点

- 5.至少说出一种开源项目(如Node)中应用原型继承的案例

- 6.可以描述new一个对象的详细过程，手动实现一个new操作符

- 7.理解es6 class构造以及继承的底层实现原理

#### 作用域和闭包

- 1.解词法作用域和动态作用域

- 2.解JavaScript的作用域和作用域链

- 3.解JavaScript的执行上下文栈，可以应用堆栈信息快速定位问题

- 4.this的原理以及几种不同使用场景的取值

- 5.包的实现原理和作用，可以列举几个开发中闭包的实际应用

- 6.解堆栈溢出和内存泄漏的原理，如何防止

- 7.何处理循环的异步操作

- 8.解模块化解决的实际问题，可列举几个模块化方案并理解其中原理

#### 执行机制

- 1.为何try里面放return，finally还会执行，理解其内部机制

- 2.JavaScript如何实现异步编程，可以详细描述EventLoop机制

- 3.宏任务和微任务分别有哪些

- 4.可以快速分析一个复杂的异步嵌套逻辑，并掌握分析方法

- 5.使用Promise实现串行

- 6.Node与浏览器EventLoop的差异

- 7.如何在保证页面运行流畅的情况下处理海量数据

#### 语法和API

- 1.理解ECMAScript和JavaScript的关系
- 2.熟练运用es5、es6提供的语法规范，
- 3.熟练掌握JavaScript提供的全局对象（例如Date、Math）、全局函数（例如decodeURI、isNaN）、全局属性（例如Infinity、undefined）

- 4.熟练应用map、reduce、filter 等高阶函数解决问题
- 5.setInterval需要注意的点，使用settimeout实现setInterval
- 6.JavaScript提供的正则表达式API、可以使用正则表达式（邮箱校验、URL解析、去重等）解决常见问题
- 7.JavaScript异常处理的方式，统一的异常处理方案

#### HTML

- 1.从规范的角度理解HTML，从分类和语义的角度使用标签

- 2.常用页面标签的默认样式、自带属性、不同浏览器的差异、处理浏览器兼容问题的方式

- 3.元信息类标签(head、title、meta)的使用目的和配置方法

- 4.HTML5离线缓存原理

- 5.可以使用Canvas API、SVG等绘制高性能的动画

#### CSS

- 1.CSS盒模型，在不同浏览器的差异

- 2.CSS所有选择器及其优先级、使用场景，哪些可以继承，如何运用at规则

- 3.CSS伪类和伪元素有哪些，它们的区别和实际应用

- 4.HTML文档流的排版规则，CSS几种定位的规则、定位参照物、对文档流的影响，如何选择最好的定位方式，雪碧图实现原理
  - 文档流
    - 块级元素
    - 内联元素(多个内联元素组成行内元素)
  - 脱离文档流
- 5.水平垂直居中的方案、可以实现6种以上并对比它们的优缺点

- 6.BFC实现原理，可以解决的问题，如何创建BFC

- 7.可使用CSS函数复用代码，实现特殊效果

- 8.PostCSS、Sass、Less的异同，以及使用配置，至少掌握一种

- 9.CSS模块化方案、如何配置按需加载、如何防止CSS阻塞渲染

- 10.熟练使用CSS实现常见动画，如渐变、移动、旋转、缩放等等

- 11.CSS浏览器兼容性写法，了解不同API在不同浏览器下的兼容性情况

- 12.掌握一套完整的响应式布局方案

## 手写

- 1.手写图片瀑布流效果

- 2.使用CSS绘制几何图形（圆形、三角形、扇形、菱形等）

- 3.使用纯CSS实现曲线运动（贝塞尔曲线）

- 4.实现常用布局（三栏、圣杯、双飞翼、吸顶），可是说出多种方式并理解其优缺点


## 计算机基础

关于编译原理，不需要理解非常深入，但是最基本的原理和概念一定要懂，这对于学习一门编程语言非常重要。

## 编译原理

- 1.理解代码到底是什么，计算机如何将代码转换为可以运行的目标程序

- 2.正则表达式的匹配原理和性能优化

- 3.如何将JavaScript代码解析成抽象语法树(AST)

- 4.base64的编码原理

- 5.几种进制的相互转换计算方法，在JavaScript中如何表示和转换

## 网络协议

- 1.理解什么是协议，了解TCP/IP网络协议族的构成，每层协议在应用程序中发挥的作用

- 2.三次握手和四次挥手详细原理，为什么要使用这种机制

- 3.有哪些协议是可靠，TCP有哪些手段保证可靠交付

- 4.DNS的作用、DNS解析的详细过程，DNS优化原理

- 5.CDN的作用和原理

- 6.HTTP请求报文和响应报文的具体组成，能理解常见请求头的含义，有几种请求方式，区别是什么

- 7.HTTP所有状态码的具体含义，看到异常状态码能快速定位问题

- 8.HTTP1.1、HTTP2.0带来的改变

- 9.HTTPS的加密原理，如何开启HTTPS，如何劫持HTTPS请求

- 10.理解WebSocket协议的底层原理、与HTTP的区别

## 设计模式

- 1.熟练使用前端常用的设计模式编写代码，如单例模式、装饰器模式、代理模式等

- 2.发布订阅模式和观察者模式的异同以及实际应用

- 3.可以说出几种设计模式在开发中的实际应用，理解框架源码中对设计模式的应用

## 数据结构和算法

    据我了解的大部分前端对这部分知识有些欠缺，甚至抵触，但是，如果突破更高的天花板，这部分知识是必不可少的，而且我亲身经历——非常有用！


## JavaScript编码能力

- 1.多种方式实现数组去重、扁平化、对比优缺点

- 2.多种方式实现深拷贝、对比优缺点

- 3.手写函数柯里化工具函数、并理解其应用场景和优势

- 4.手写防抖和节流工具函数、并理解其内部原理和应用场景

- 5.实现一个sleep函数   
  ```
  async function test() { 
    console.log('开始啦') 
    await sleep(3000) 
    console.log('这是来自3s之后的问好') } 
    function sleep(ms) { 
      return new Promise(resolve => setTimeout(resolve, ms)) 
    }
  ```
## 手动实现前端轮子

- 1.手动实现call、apply、bind  
  ```
  if (!Function.prototype.bind) {
    Function.prototype.bind = function (oThis) {
      if (typeof this !== "function") {
        // closest thing possible to the ECMAScript 5 internal IsCallable function
        throw new TypeError("Function.prototype.bind - what is trying to be bound is not callable");
      }

      var aArgs = Array.prototype.slice.call(arguments, 1), 
          fToBind = this, 
          fNOP = function () {},
          fBound = function () {
            return fToBind.apply(this instanceof fNOP && oThis
                                  ? this
                                  : oThis || window,
                                aArgs.concat(Array.prototype.slice.call(arguments)));
          };

      fNOP.prototype = this.prototype;
      fBound.prototype = new fNOP();

      return fBound;
    };
  }
  ```
- 2.手动实现符合Promise/A+规范的Promise、手动实现async await
  
- 3.手写一个EventEmitter实现事件发布、订阅
  实际操作有点难度.
- 4.可以说出两种实现双向绑定的方案、可以手动实现
  ```
  <input type="input" id="input">
    <span id="show"></span>
    <script>
        var obj = {};
        Object.defineProperty(obj, 'txt', {
            get: function () {
                return obj;
            },
            set: function (newValue) {
                document.getElementById('input').value = newValue;
                document.getElementById('show').innerHTML = newValue;
            }
        });
        document.getElementById('input').addEventListener('keyup', function (e) {
            obj.txt = e.target.value;
        });
    </script>
    ```
- 5.手写JSON.stringify、JSON.parse

- 6.手写一个模版引擎，并能解释其中原理

- 7.手写懒加载、下拉刷新、上拉加载、预加载等效果

## 数据结构

- 1.理解常见数据结构的特点，以及他们在不同场景下使用的优缺点

- 2.理解数组、字符串的存储原理，并熟练应用他们解决问题

- 3.理解二叉树、栈、队列、哈希表的基本结构和特点，并可以应用它解决问题

- 4.了解图、堆的基本结构和使用场景

## 算法

- 1.可计算一个算法的时间复杂度和空间复杂度，可估计业务逻辑代码的耗时和内存消耗

- 2.至少理解五种排序算法的实现原理、应用场景、优缺点，可快速说出时间、空间复杂度

- 3.了解递归和循环的优缺点、应用场景、并可在开发中熟练应用

- 4.可应用回溯算法、贪心算法、分治算法、动态规划等解决复杂问题

- 5.前端处理海量数据的算法方案


## 运行环境

    我们需要理清语言和环境的关系：

    ECMAScript描述了JavaScript语言的语法和基本对象规范

    浏览器作为JavaScript的一种运行环境，为它提供了：文档对象模型（DOM），描述处理网页内容的方法和接口、浏览器对象模型（BOM），描述与浏览器进行交互的方法和接口

    Node也是JavaScript的一种运行环境，为它提供了操作I/O、网络等API


## 浏览器API

- 1.浏览器提供的符合W3C标准的DOM操作API、浏览器差异、兼容性

- 2.浏览器提供的浏览器对象模型 (BOM)提供的所有全局API、浏览器差异、兼容性

- 3.大量DOM操作、海量数据的性能优化(合并操作、Diff、requestAnimationFrame等)

- 4.浏览器海量数据存储、操作性能优化

- 5.DOM事件流的具体实现机制、不同浏览器的差异、事件代理

- 6.前端发起网络请求的几种方式及其底层实现、可以手写原生ajax、fetch、可以熟练使用第三方库

- 7.浏览器的同源策略，如何避免同源策略，几种方式的异同点以及如何选型

- 8.浏览器提供的几种存储机制、优缺点、开发中正确的选择

- 9.浏览器跨标签通信
  localStorge,cookie,SharedWorker,WebSocket
  
## 浏览器原理

- 1.各浏览器使用的JavaScript引擎以及它们的异同点、如何在代码中进行区分

- 2.请求数据到请求结束与服务器进行了几次交互

- 3.可详细描述浏览器从输入URL到页面展现的详细过程

- 4.浏览器解析HTML代码的原理，以及构建DOM树的流程

- 5.浏览器如何解析CSS规则，并将其应用到DOM树上

- 6.浏览器如何将解析好的带有样式的DOM树进行绘制

- 7.浏览器的运行机制，如何配置资源异步同步加载

- 8.浏览器回流与重绘的底层原理，引发原因，如何有效避免

- 9.浏览器的垃圾回收机制，如何避免内存泄漏

- 10.浏览器采用的缓存方案，如何选择和控制合适的缓存方案

## Node

- 1.理解Node在应用程序中的作用，可以使用Node搭建前端运行环境、使用Node操作文件、操作数据库等等

- 2.掌握一种Node开发框架，如Express，Express和Koa的区别

- 3.熟练使用Node提供的API如Path、Http、Child Process等并理解其实现原理

- 4.Node的底层运行原理、和浏览器的异同

- 5.Node事件驱动、非阻塞机制的实现原理


## 框架和类库

    轮子层出不穷，从原理上理解才是正道

## TypeScript

- 1.理解泛型、接口等面向对象的相关概念，TypeScript对面向对象理念的实现

- 2.理解使用TypeScript的好处，掌握TypeScript基础语法

- 3.TypeScript的规则检测原理

- 4.可以在React、Vue等框架中使用TypeScript进行开发

## React

- 1.React和vue 选型和优缺点、核心架构的区别

- 2.React中setState的执行机制，如何有效的管理状态

- 3.React的事件底层实现机制

- 4.React的虚拟DOM和Diff算法的内部实现

- 5.React的Fiber工作原理，解决了什么问题

- 6.React Router和Vue Router的底层实现原理、动态加载实现原理

- 7.可熟练应用React API、生命周期等，可应用HOC、render props、Hooks等高阶用法解决问题

- 8.基于React的特性和原理，可以手动实现一个简单的React

## Vue

- 1.熟练使用Vue的API、生命周期、钩子函数

- 2.MVVM框架设计理念

- 3.Vue双向绑定实现原理、Diff算法的内部实现

- 4.Vue的事件机制

- 5.从template转换成真实DOM的实现机制

## 多端开发

- 1.单页面应用（SPA）的原理和优缺点，掌握一种快速开发SPA的方案

- 2.理解Viewport、em、rem的原理和用法，分辨率、px、ppi、dpi、dp的区别和实际应用

- 3.移动端页面适配解决方案、不同机型适配方案

- 4.掌握一种JavaScript移动客户端开发技术，如React Native：可以搭建React Native开发环境，熟练进行开发，可理解React Native的运作原理，不同端适配
.- 5.掌握一种JavaScript PC客户端开发技术，如Electron：可搭建Electron开发环境，熟练进行开发，可理解Electron的运作原理

- 6.掌握一种小程序开发框架或原生小程序开发

- 7.理解多端框架的内部实现原理，至少了解一个多端框架的使用

## 数据流管理

- 1.掌握React和Vue传统的跨组件通信方案，对比采用数据流管理框架的异同

- 2.熟练使用Redux管理数据流，并理解其实现原理，中间件实现原理

- 3.熟练使用Mobx管理数据流，并理解其实现原理，相比Redux有什么优势

- 4.熟练使用Vuex管理数据流，并理解其实现原理

- 5.以上数据流方案的异同和优缺点，不情况下的技术选型

## 实用库

- 1.至少掌握一种UI组件框架，如antd design，理解其设计理念、底层实现

- 2.掌握一种图表绘制框架，如Echart，理解其设计理念、底层实现，可以自己实现图表

- 3.掌握一种GIS开发框架，如百度地图API

- 4.掌握一种可视化开发框架，如Three.js、D3

- 5.工具函数库，如lodash、underscore、moment等，理解使用的工具类或工具函数的具体实现原理

## 开发和调试

- 1.熟练使用各浏览器提供的调试工具

- 2.熟练使用一种代理工具实现请求代理、抓包，如charls

- 3.可以使用Android、IOS模拟器进行调试，并掌握一种真机调试方案

- 4.了解Vue、React等框架调试工具的使用


## 前端工程

    前端工程化：以工程化方法和工具提高开发生产效率、降低维护难度

## 项目构建

- 1.理解npm、yarn依赖包管理的原理，两者的区别

- 2.可以使用npm运行自定义脚本

- 3.理解Babel、ESLint、webpack等工具在项目中承担的作用

- 4.ESLint规则检测原理，常用的ESLint配置

- 5.Babel的核心原理，可以自己编写一个Babel插件

- 6.可以配置一种前端代码兼容方案，如Polyfill

- 7.Webpack的编译原理、构建流程、热更新原理，chunk、bundle和module的区别和应用

- 8.可熟练配置已有的loaders和plugins解决问题，可以自己编写loaders和plugins

## nginx

- 1.正向代理与反向代理的特点和实例

- 2.可手动搭建一个简单的nginx服务器、

- 3.熟练应用常用的nginx内置变量，掌握常用的匹配规则写法

- 4.可以用nginx实现请求过滤、配置gzip、负载均衡等，并能解释其内部原理

## 开发提速

- 1.熟练掌握一种接口管理、接口mock工具的使用，如yapi

- 2.掌握一种高效的日志埋点方案，可快速使用日志查询工具定位线上问题

- 3.理解TDD与BDD模式，至少会使用一种前端单元测试框架

## 版本控制

- 1.理解Git的核心原理、工作流程、和SVN的区别

- 2.熟练使用常规的Git命令、git rebase、git stash等进阶命令

- 3.可以快速解决线上分支回滚、线上分支错误合并等复杂问题

## 持续集成

- 1.理解CI/CD技术的意义，至少熟练掌握一种CI/CD工具的使用，如Jenkins

- 2.可以独自完成架构设计、技术选型、环境搭建、全流程开发、部署上线等一套完整的开发流程（包括Web应用、移动客户端应用、PC客户端应用、小程序、H5等等）


## 项目和业务


## 后端技能

- 1.了解后端的开发方式，在应用程序中的作用，至少会使用一种后端语言

- 2.掌握数据最终在数据库中是如何落地存储的，能看懂表结构设计、表之间的关联，至少会使用一种数据库

## 性能优化

- 1.了解前端性能衡量指标、性能监控要点，掌握一种前端性能监控方案

- 2.了解常见的Web、App性能优化方案

- 3.SEO排名规则、SEO优化方案、前后端分离的SEO

- 4.SSR实现方案、优缺点、及其性能优化

- 5.Webpack的性能优化方案

- 6.Canvas性能优化方案

- 7.React、Vue等框架使用性能优化方案

## 前端安全

- 1.XSS攻击的原理、分类、具体案例，前端如何防御

- 2.CSRF攻击的原理、具体案例，前端如何防御

- 3.HTTP劫持、页面劫持的原理、防御措施

## 业务相关

- 1.能理解所开发项目的整体业务形态、业务目标、业务架构，可以快速定位线上业务问题

- 2.能理解所开发项目整体的技术架构、能快读的根据新需求进行开发规划、能快速根据业务报警、线上日志等定位并解决线上技术问题

- 3.可以将自己的想法或新技术在业务中落地实践，尽量在团队中拥有一定的不可替代性


## 学习提升


vczh大神在知乎问题【如何能以后达到温赵轮三位大神的水平？】下的回答：

这十几年我一共做了三件事：

- 1.不以赚钱为目的选择学习的内容；

- 2.以自己是否能造出轮子来衡量学习的效果；

- 3.坚持每天写自己的代码，前10年每天至少6个小时，不包含学习和工作的时间。

上面几点可能有点难，第一点我就做不到，但是做到下面绩点还是比较容易的。

关于写博客说明下，能给别人讲明白的知识会比自己学习掌握的要深刻许多

- 1.拥有自己的技术博客，或者在一些博客平台上拥有自己的专栏

- 2.定期的将知识进行总结，不断完善自己的知识体系

- 3.尽量将自己的知识转换成真实的产出，不要仅仅停留在书面理解层面，更重要的是实际应用

- 4.坚持输出自己的代码，不要盲目的扎进公司业


## 技术之外


这部分可能比上面九条加起来重要！

- 1.了解互联网人员术语：CEO、CTO、COO、CFO、PM、QA、UI、FE、DEV、DBA、OPS等

- 2.了解互联网行业术语：B2B、B2C、C2C、O2O等

- 3.掌握互联网行业沟通、问答、学习的

- 4.有一定的"PPT"能力

- 5.有一定的理财意识，至少了解储蓄、货币基金、保险、指数基金、股票等基本的理财知识

- 6.掌握在繁重的工作和长期的电脑辐射的情况下保持健康的方法，建立正确的养生知识体系  

[前端工程师的自检清单](https://mp.weixin.qq.com/s?__biz=MzAxODE2MjM1MA==&mid=2651556338&idx=1&sn=589976a52b9162ec8d7a9a165cbfac7d&chksm=80255e33b752d7257f4ed1e36560a496c097c77b5ac922adc0f11a7b2c86b7654ba77e1a255a&mpshare=1&scene=1&srcid=0508mNKM4Hy94kZGwq6IjfsR&pass_ticket=YNUF1X84t4HG4DWTW3CfBtvCWazRU89AmjCKPZARR5wMyeHrksl%2FKXnK3EAocUgq#rd)

## <a id="思维导图">思维导图</a>

- ![前端知识思维导图](https://ftp.bmp.ovh/imgs/2020/05/b409a7f0b8788906.png)

## <a id="摘要">摘要</a>

#### 函数节流

```javascript
/*触发第一次有效，间隔时间外才能触发第二次...*/
/*指定时间内执行一次代码*/

function debounce(fn, delay) {
  let timer = null
     return function (timer) {
         timer = setTimerout(() => {
             fn.call(this)
             clearTimeout(timer)
             timer = null
         }, delay)
     }
}
```

#### 函数防抖

```javascript
/*频繁触发,仅执行最后一次出现的事件函数*/

function debounce(fn, delay) {
  let timer = null
  return function (timer) {
    clearTimeout(timer)  // 每次点击把之前的清除
    timer = setTimerout(() => {
       fn.call(this)
    }, delay) 
  }
}
```

#### 排序算法

- 冒泡排序
  - 算法描述
    - 1.比较相邻元素，若第一个大于第二个，交换他们。
    - 2.重复第一步，最后的数将会最大。
    - 3.重复以上步骤，除了最后一个数
    - 4.继续重复以上步骤，直到没有任何一对数需要比较。
    
    ```javascript
    function bubbleSort(arr) {                                          //参数：数组;返回值。
            var len = arr.length;
            for (let i = 0; i < len; i++) {
                for (let j = 0; j < len -1 - i; j++) {
                    if (arr[j] > arr[j + 1]) {                                 //相邻两个元素比较
                        let temp = arr[j + 1];                                 //元素交换
                             arr[j + 1] = arr[j];
                             arr[j] = temp;
                    }
                }
            }
            return arr;                                                              //返回排完序数组
        }
        console.log(bubbleSort([21,78,15,36,59,11,34,25,13]));      //11,13,15,21,25,34,36,59,78
    ```

- 快速排序
    - 算法描述
      - 1.找基准点。
      - 2.建立两个空数组。
      - 3.arr中大于基准点放left,则反之。
      - 4.left,基准点，right连接起来。
      
    ```javascript
    function quicksort(arr) {                                              //参数类型：数组；返回值，数组。
            if (arr.length <= 1) {
                return arr;
            }
            var equally = Math.floor(arr.length / 2);                      //arr中间索引
            var benchmark = arr.splice(equally,1);                         //arr中间值
            var left = [];
            var right = [];
            for (var i = 0,len = arr.length; i < len; i++) {
                if (arr[i] < benchmark) {
                    left.push(arr[i]);
                } else {
                    right.push(arr[i]);
                }
            }
            return quicksort(left).concat([benchmark],quicksort(right));    //不断递归，最后都递归为一个数，然后拼接数组，返回排完序数组。
        }
        console.log(quicksort([21,81,12,85,31,97,18,2,87,75,3]));      //output:2,3,12,18,21,31,75,81,85,87,97
    ```

- 选择排序
  - 算法描述
    - 1.与第一个数比较，如果大于它，则交换位置
    - 2.重复第一步，一遍循环，第一个数是最小值；
    - 3.重复n-1次循环，OK。
    
    ```javascript
     function selectSort(arr) {                                     //参数：数组；返回值：数组。
            var len = arr.length;
            var temp;
            for (var i = 0; i < len - 1; i++) {
                for (var j = j + 1; j < len; j++) {
                    if (arr[j] < arr[i]) {                               //与第一个数比较
                        temp = arr[j];                                  //交换位置
                        arr[j] = arr[i];
                        arr[i] = temp;                                     
                    }
                }
            }
            return arr;                                                   //返回数组
        }
        console.log(selectSort([14,52,18,78,54,114,65,28,56]));  //14,52,18,78,54,114,65,28,56
    ```

- 插入排序
  - 算法描述
    - 1.第一个数a[0]与第二个数a[1]比较，若a[0] > a[1],则 a[1] = a[0]
    - 2.关键是第三个数a[2],a[2]先与a[1]，若a[2] < a[1],则交换位置，此时a[1]再与a[0]比较大小。
    
    ```javascript
     function insertSort(arr) {                            //参数：数组；返回值：数组。
              for (let i = 1,len = arr.length; i < len;i++) {
                  for (let j = i - 1; j >= 0;j--) {        //j--：若a[2] < a[1],指针退1。
                      if (arr[j] > arr[j + 1]) {           //比较相邻两数大小
                          let temp = arr[j + 1];
                          arr[j + 1] = arr[j];
                          arr[j] = temp;
                      }
                  }
              }
              return arr;                                   //返回数组
          }
    console.log(insertSort([12,85,42,67,34,56,19,97,47]));  //12,19,34,42,47,56,67,85,97
    ```

- 归并排序
  - 算法描述
    - 1.把arr分成left,right子序列;
    - 2.比较left,right大小，返回排完序数组，递归两次；
    - 3.递归与栈相关，弹出并返回的值执行其他动作。
    
    ```javascript
    function mergeSort(arr) {                                  //参数类型：数组；返回：数组。
            if (arr.length < 2) {
                return arr;
            }
    
            const middle = Math.floor(arr.length / 2);         //中间值
            const left = arr.slice(0,middle);                  //left[]
            const right = arr.slice(middle);                   //right[]  
            return merge(mergeSort(left),mergeSort(right));    //递归两次
        }
    
        function merge(left,right) {
            var newArr = [];
            while (left.length && right.length) {              
                if (left[0] < right[0]) {                       //子序列比较大小
                    newArr.push(left.shift());
                } else {
                    newArr.push(right.shift());
                }
            }
            return newArr.concat(left,right);                    //返回合并好的了子序列
        }
        console.log(mergeSort([54,24,15,95,75,35,68,78,12,31,108]));   //12,15,24,31,35,54,68,75,78,95,108
    ```

## 书籍

- [ECMAScript 6 入门](http://es6.ruanyifeng.com/)（阮一峰）
- [JS-design-pattern](https://github.com/hzlu/JS-design-pattern)（曾探大牛的设计模式）
- [Learning JavaScript Design Patterns](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)（老外的设计模式）
- [Speaking JavaScript](http://speakingjs.com/)（JS知识点超详细）  

## 其他

 - [一个实用的图表配置](https://gallery.echartsjs.com)
