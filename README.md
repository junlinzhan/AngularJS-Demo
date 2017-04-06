# AngularJS-Demo
AngularJS学习 一些示例

通过数据绑定和依赖注入减少了大量代码，而这些都在浏览器端通过JavaScript实现，能够和任何服务器端技术完美结合。
Angular是为了扩展HTML在构建应用时本应具备的能力而设计的。对于静态文档，HTML是一门很好的声明式的语言，但对于构建动态WEB应用，它无能为力。所以，构建动态WEB应用往往需要一些技巧才能让浏览器配合我们的工作。Angular通过指令（directive）扩展HTML的语法

> # 一、AngularJS四大核心特性
> ## 1.MVC
> 指Model View Controller

> ## 2.模块化和依赖注入
> 模块用于单独的逻辑表示服务，控制器，应用程序等，并保持代码的整洁。我们在单独的js文件中定义的模块，并将其命名为按照module.js文件形式
> #### 模块化的好处
> 1.1 增加了模块的可重用性
>
> 1.2 通过定义模块，实现加载顺序的自定义
>
> 1.3 在单元测试中，不必加载所有的内容
> #### 依赖注入
> Dependency Injection (DI,依赖注入)是一种软件设计模式,用于处理如何让程序获得其依赖(对象的)引用
 
> ## 3.双向数据绑定
> 一但建立双向绑定，使用者输入，会由Angular自动传到一个变量中，再自动读到所有绑到它的内容，更新它，效果上就是立即的资料同步， 在程式码中修改变量，也会直接反应到呈现的外观上。

> ## 4.指令
> 指令是DOM元素上的标记，使元素拥有特定的行为。举例来说，静态的HTML不知道如何来创建和展现一个日期选择器控件。让HTML能识别这个语法，我们需要使用指令。指令通过某种方法来创建一个能够支持日期选择的元素。我们会循序渐进地介绍这是如何实现的。 如果你写过AngularJS的应用，那么你一定已经使用过指令，不管你有没有意识到。你肯定已经用过简单的指令，比如 ng-mode, ng-repeat, ng-show等。这些指令都赋予DOM元素特定的行为。例如，ng-repeat 重复特定的元素，ng-show 有条件地显示一个元素。如果你想让一个元素支持拖拽，你也需要创建一个指令来实现它。指令背后基本的想法很简单。它通过对元素绑定事件监听或者改变DOM而使HTML拥有真实的交互性。

---

> # 二、AngularJS 表达式
> AngularJS 使用 表达式 把数据绑定到 HTML。
>
> AngularJS 表达式写在双大括号内：{{ expression }}。
>
> 与 ng-bind 指令有异曲同工之妙。
>
> 类似JavaScript 表达式，可以包含文字、运算符和变量。
> ### 1.示例（数字、字符串、对象、数组）
> 实例 {{ 5 + 5 }} 或 {{ firstName + " " + lastName }}
>
> 	1.<body>
		<div ng-app="" ng-init="quantity=1;cost=5">
		<p>总价： {{ quantity * cost }}</p>
		</div>
	</body>
	2.<body>
		<div ng-app="" ng-init="quantity='firstName';cost='lastName'">
		<p>字符串拼接： {{ quantity + cost }}</p>
		</div>
	</body>
	3.<body>
		<div ng-app="" ng-init="person={firstName:'John',lastName:'Doe'}">
		<p>姓名： {{ person.firstName + person.lastName }}</p>
		</div>
	</body>
	4.<body>
		<div ng-app="" ng-init="points=[1,15,19,2,40]">
		<p>第三个值为 {{ points[2] }}</p>
		</div>
	</body>
>
> ### 2.AngularJS 表达式 与 JavaScript 表达式
> 类似于 JavaScript 表达式，AngularJS 表达式可以包含字母，操作符，变量。
> 与 JavaScript 表达式不同，AngularJS 表达式可以写在 HTML 中。
> 与 JavaScript 表达式不同，AngularJS 表达式不支持条件判断，循环及异常。
> 与 JavaScript 表达式不同，AngularJS 表达式支持过滤器。
