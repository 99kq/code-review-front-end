# <!-- Code Review Checklist for Front-End Developers --> 前端开发者的代码回顾清单


<!-- The goal is not to define a formal definition of practices for code review but to give some checklist for reviewers.  -->
我们的目的并不是定义一套固有的代码回顾实践方式，而是为回顾者 (reviewer) 提供一份清单。

<!-- Of course, it helps a developer to know how the reviewer does his code review. He can so focus on writing a better and simpler code. -->
当然，它也帮助开发者了解在代码回顾时如何扮演好一名回顾者的角色。回顾者本应如此专注于撰写更好更简洁的代码。

<!-- We speak about because the code author doesn't make his own code review. The developer needs a new way. Of course, the developer could continue to refactor his code to improve it. -->
因为代码的作者没有进行自我回顾。所以开发者需要一种新的方式——很显然他们可以持续提炼并改进代码。


## <!-- Philosophy --> 理念


    代码回顾对事不对人 (Code Review is about the code not about the coder)


<!-- Basically, the code review focuses only on code written. -->
首先，代码回顾只专注在写出来的代码上。
 
<!-- It's not the time to blame the author but to verify that the code meets the defined standards, best practices...  -->
这种场合最应该做的是确认代码符合既定标准、最佳实践等等，务必回避指责作者的行为。

<!-- It means that no one escapes the code review: new hire, a senior, the lead developer or even CTO. -->
没有人能够挑战这一原则，不论他是新雇员、老鸟、主管哪怕是 CTO。

<!-- **What must be understood is that there is no written well enough to not be seen code.** -->
**我们必须意识到，没有任何代码是足够优秀到不需要回顾的。**

<!-- This is also the time to share development techniques, tips ... and why not initiate discussions or debate on a particular way of coding. -->
同时，这也是分享开发技术技巧的绝佳时机，再顺便探讨一下当下流行的编码方式，何乐而不为呢？



## <!-- Checklist --> 清单

<!-- The checklist is a set of points that are checked during code review.  -->
这里的清单是指一套代码回顾时遵循的要点集合。

<!-- So it helps developers to understand what will be reviewed. -->
同时这份清单也会帮助开发者理解哪些东西需要回顾。


### 0. <!-- Style and Code Guidelines --> 编码规范

<!-- In fact, this item is value 0 because it does not fit in the checklist itself: it has to be followed everytime. -->
这件事情排在步骤 0，因为实际上它并不算在清单本身的范畴内：编码规范是需要时刻遵守的。

<!-- It means each developer has to follow the defined Coding Guidelines. -->
也就是说，每一名开发者都必须遵循既定的编码规范。

### 1. <!-- Code Quality --> 代码质量

<!-- The code quality allows two things:  -->
代码质量能够确保：

<!-- * One, reduce the rate of bugs -->
<!-- * Two, to make the code readable by everyone. -->
1. 减少 bug 数量；
2. 让每个人都读得懂。
 
<!-- The front-end team could use some tools like [JSHint](http://www.jshint.com/) or [Plato](https://github.com/es-analysis/plato) to monitor code quality in JavaScript. -->
前端团队可以通过 [JSHint](http://www.jshint.com/) 或 [Plato](https://github.com/es-analysis/plato) 等类似的工具来监控 JavaScript 代码的质量。
 
 
### 2. <!-- Consistency --> 一致性

<!-- The reviewer obviously ensures that the written code responds well to the problem of features or defects. -->
回顾者要确保写出的代码能够满足需求，正常工作。


### 3. <!-- Simple --> 简单

<!-- The reviewer ensures that the code gets straight to the point.  -->
回顾者要确保代码直接有效的解决了问题。

<!-- We can then help the cyclomatic complexity calculated by JSHint (see point 2).  -->
然后我们可以通过 JSHint (详见第 2 条) 来计算条件复杂度。

<!-- There is a correlation between complexity and the likely bugs rate.  -->
复杂度和 bug 的出现频率是由相关性的。

<!-- Basically, the more complicated it is, the more simplified. -->
基本上，越是复杂的地方，就越要简化。


### 4. <!-- Maintainability --> 可维护性

<!-- The reviewer ensures that another developer can change the code in a small time.  -->
回顾者确保另一名开发者也可以对现有代码进行快速修改。

<!-- The code is modular (with pattern, for example) and the variables or methods names are explicit.  -->
回顾者确保代码是 (比如通过一些模式达到) 模块化的，并且变量和方法的命名是清晰的。

<!-- This is true for the CSS or HTML with explicit selectors. We must be able to understand what name the class or method performs.  -->
HTML 和 CSS 选择器也同样如此。我们必须能够理解 class 或方法表现出的含义。

<!-- It also checks the rule of **One method, one thing**. -->
还要确保**一个方法做一件事**的原则。


### 5. <!-- Performance --> 性能

<!-- Performance is not limited to the minification of js or css files and use sprites for images.  -->
性能问题不仅限于 js 或 css 文件的压缩比率以及对图片精灵的使用。

<!-- This also happens in loops, array access, DOM access...  -->
它还存在于循环、数组操作、DOM 操作等方方面面……

<!-- jsPerf is an excellent online tool that allows you to test the performance of a piece of code on different browsers : [http://jsperf.com/](http://jsperf.com/) -->
jsPerf 是一个非常棒的工具，它可以在线测试一段代码在各种浏览器中的性能：[http://jsperf.com/](http://jsperf.com/)。

<!-- Example : [Comparing the performance difference of varied jQuery 1.7 selectors ?](http://jsperf.com/id-vs-class-vs-tag-selectors/2) -->
例如 : [比较 jQuery 1.7 中各种选择器的性能差异](http://jsperf.com/id-vs-class-vs-tag-selectors/2)

## <!-- Deep diving --> 延伸阅读

<!-- * CodeShip Code Review: [http://blog.codeship.io/2013/08/22/the-codeship-workflow-part-2-pull-requests-and-code-review.html](http://blog.codeship.io/2013/08/22/the-codeship-workflow-part-2-pull-requests-and-code-review.html) -->
* CodeShip 的代码回顾: [http://blog.codeship.io/2013/08/22/the-codeship-workflow-part-2-pull-requests-and-code-review.html](http://blog.codeship.io/2013/08/22/the-codeship-workflow-part-2-pull-requests-and-code-review.html)

<!-- * Code Review with Microsoft tools: [http://msdn.microsoft.com/en-us/library/hh474795.aspx#code_review_request](http://msdn.microsoft.com/en-us/library/hh474795.aspx#code_review_request) -->
* 微软的代码回顾工具: [http://msdn.microsoft.com/en-us/library/hh474795.aspx#code_review_request](http://msdn.microsoft.com/en-us/library/hh474795.aspx#code_review_request)

<!-- * Checklist example: [http://courses.cs.washington.edu/courses/cse403/12wi/sections/12wi_code_review_checklist.pdf](http://courses.cs.washington.edu/courses/cse403/12wi/sections/12wi_code_review_checklist.pdf) -->
* 一个清单示例: [http://courses.cs.washington.edu/courses/cse403/12wi/sections/12wi_code_review_checklist.pdf](http://courses.cs.washington.edu/courses/cse403/12wi/sections/12wi_code_review_checklist.pdf)

<!-- * Hadoop Code Review: [https://wiki.apache.org/hadoop/CodeReviewChecklist](https://wiki.apache.org/hadoop/CodeReviewChecklist) -->
* Hadoop 的代码回顾: [https://wiki.apache.org/hadoop/CodeReviewChecklist](https://wiki.apache.org/hadoop/CodeReviewChecklist)

## <!-- Authors and contributors --> 作者与贡献者

### <!-- Current --> 当前
* [Yassine Azzout](http://yass.io) (创建者)
* [勾三股四](http://jiongks.name) (中文翻译)

### <!-- License --> 协议
[MIT license](http://www.opensource.org/licenses/Mit)