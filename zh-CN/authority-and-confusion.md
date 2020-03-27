﻿# 权威与混淆

# 问题概述

　　在程序设计语言的学习、程序设计语言理论乃至一般的软件开发领域中，充斥着许多指鹿为马、以讹传讹的现象。虽然这并非这些领域的特色，但存在一些理由使之特别显著，而应当引起重视。

　　这类混淆普遍而基本。这特别体现在[如“变量”这样的基础概念的混淆](variable.md)的问题上。

　　这通常不是有意的；但毫无疑问，这和涉众普遍缺乏独立思考的能力和对理论思辨的不重视有关，而功利、片面而不充分的教学加重了这个问题。

# 具体症状

　　这种共通的问题在不同领域中有相似的来源，但影响略有不同。

## 语言学习

　　这首先体现在程序语言的用户学习语言时，习惯性地参照流行的材料，却并没有足够注意来源的可靠性，不懂什么材料是可信的权威来源。

　　这这些由**人为设计**决定最终“是什么”的领域来说，这是很要命的。因为，这会自然地造成混乱——好比打官司空口无凭不靠成文法和书面的合约，控辩都只凭自己的认知临场自己解释一套。

　　这是没有原则的胡来。健全的法律制度当然会限制这样的迷惑行为，但工程界的很多规范并不够具有强制性；很遗憾，语言规范——程序语言的规格说明(specification) 正是其中差不多最不受重视的一种。

### 学习材料

　　许多用户学习语言时，会使用比较通俗的教科书，而弃置语言规范于一边，认为有一本可靠的书就能充分引导编程实践，而不需要其它参考资料。这不是明智的做法。

　　全面掌握程序语言对缺乏系统理论计算机科学和计算机乃至数学史专业训练的学习者是相当困难的。为了满足现实需要，教科书普遍自降门槛，引导用户入门学会“使用语言编程”——实际只是完成一些比较有普遍性的简单任务——而避免以使读者全面掌握程序设计语言为目标。由于不强调理论积累，用户会被更多地要求通过编程实践的发现和总结遇到的问题来检验学习成果。很遗憾，只靠教科书，这普遍是不可行的。因为教科书不是规格说明文档，它并不要求完整覆盖语言设计中应有的所有内容；一旦用户遇到实现反馈和自身认知不相同的问题时，便容易无所适从，或者在缺乏规范的情况下，自己强行发明教科书中不存在（而语言规范应该保证解决）的内容——曲解了语言本身。这也是造成误导扩散的一个理由。反过来，语言规范如果不能处理这种情形，就应当认为是设计缺陷，需要修正——否则，不止是学习上会遇到问题，语言的实现也会缺乏足够的依据保证预期的行为。

　　读者应当理解教科书的质量参差不齐；但入门者通常不清楚，即便是其中最权威的材料，可靠性也难以和语言规范相提并论。因为历史原因，早期的教科书编写者通常是语言的设计者，著作和使用手册一道还会被作为正式规格的基础。这样的来源自然相对是比较可信的。但随着时间的推移，因为作者逝世等原因不能再维护语言规范，以及其他用户普遍参与语言的修订工作的因素，作者的早期文献不再保持是最可靠的来源。例如，K&R C 是公认权威的关于 C 语言的文献，但[仍然有一些会引起读者困惑的技术性问题](http://bbs.chinaunix.net/forum.php?mod=viewthread&tid=4091259)没有[讲清楚](http://bbs.chinaunix.net/thread-4091259-3-1.html)。这种情况下脱离 C 的正式规范（ISO/IEC 9899）基本是不可能完整解答的；而即便读者自己具有起草规范的能力，脱离现有的规范也是舍近求远。

　　而大多数其他的作者，著作本身是基于上述的文献的二手来源或更多手的间接材料（前者编写的著作，甚至社区讨论的道听途说），在不和第一手来源（尤其是语言规范）校对的情况下，时有出错的可能。作者和作者之间的严谨程度也不一样，对待校订和勘误的程度也大相径庭，使得读者只参考这类文献，学到的内容和效果上会有极大的不确定性；由于这些读者中的一部分还可能自己整理文献甚至出版教科书，而并没有继承来源可靠性，产生以讹传讹的现象就不难理解了。

　　近年来视频教学的流行进一步加重了这种情况。视频适合互动教学和示例引导，但因为技术限制，其中表现的教学内容在准确性上比书面材料通常更难以保证，内容容量也更有限；大部分作者（即便有课堂教学经验）也不习惯使用视频深入地表达准确严肃的议题，更多只是简单介绍和概括重点——这对语言学习来讲是不够的。同时，在线视频内容的创作比一般的出版物的门槛更低，使得内容来源的可靠性进一步降低。这些因素使视频整体比教科书更加不可靠。不少视频观众以视频彻底代替教科书，这是比全然依赖教科书作为参考材料更加错误的学习方法。

　　此外，对专业的读者来说，阅读包括规格说明书在内的技术文档很可能是以后的工作的主要内容的一部分。既然迟早需要适应这种需求而习得类似的技能，为什么不先养成好习惯，知道怎么找到和使用靠谱的来源呢？反过来，使用不可靠的来源进行学习，无疑增大事半功倍乃至无法达到预期学习目的的风险。

### 检验手段

　　对语言学习成果的检验手段和现实业界需求相比是比较初级的，不能满足需要。

　　一般地，标准化应试（不管是学位、资格认证的还是招聘用的，不管是笔试还是在线提交程序的评测）都只能检验比较常规的语言的使用方式。这通常只能覆盖一门（通用目的）语言的非常少的功能点。而实用中更复杂的综合技术无法直接准确地验证。像代码规范这样适应实用规则的能力更加无法被考察。

　　经常有用人单位在实际工作中发现能力不匹配的问题。好在业界大多已经习惯“终身学习”，在职业培训上普遍预留资源，才不至于显得明显尴尬。但这种做法是片面的。因为对语言学习认识的偏差和刻板印象，管理人员容易混淆问题的领域——例如，片面强调“算法”的重要性并认为语言的知识相对更不重要。（不过在实际工作中，大多数算法相关的任务要求认识“新”算法和问题领域的高效匹配，基本上除了本来就是专家的情况，无论如何都要另外学习并容易直接体会到缺乏算法以外的知识的问题，所以造成的后果反而并不严重。）

　　检验学习成果的局促和效果的不显著导致业界不得不减少对语言学习过程的依赖。这又反过来导致应用在职业培训上的学习资源和教学的脱节，不能解决原有问题，反而加大成本。而非技术人员在这样混乱的取向和刻板印象的作用下，更加无法投入合理的资源支持改善现有的状况。这种负反馈是持久的。

## 程序语言

　　在程序语言理论研究中，不遵循规格说明的习惯导致由语言规范约定的语言具体设计和研究的理论之间出现不必要的偏差，削弱理论的适用性。

　　要研究普遍问题而脱离具体语言规范是合理的，但想尽量脱离通过起草规范这种产出来又想体现“设计”，至少在研究怎么设计语言这个议题上，是没有多少现实意义的。

　　比较严重的直接后果是理论研究和应用实践的脱节：理论界说一套，但工程上实用的内容除了几个公共的概念在名字（拼写）上相关，几乎完全改头换面。[OOP 的理论](https://cs.stackexchange.com/questions/18963/is-there-a-theory-abstraction-behind-oop)就是一个例子——已经成为“权威”的理论（如所谓的对象代数）建模的内容和流行的语言中具有的特性差距甚远，而和更接近现实的理论缺乏同行评审和普遍承认。

　　另一方面，工业界流行的语言很多都和理论界无关。指导实用语言设计本应几乎就是这个领域最重要的需要解决的普遍问题（其它问题反倒有交叉学科背景而相对不那么迫切非得依赖这个领域），但实际却几乎没有有效产出——改进语言通常是工业界自行完成的（倒也因此容易理解其中有不少低级理论错误而走了弯路）。这种现象可以认为是一种内卷化(involution) ：许多程序语言理论的子研究领域的成果重要性的评价已经相当不依赖工业界的使用反馈，而以领域内部“学术”的指标（例如论文的影响因子）全然加以评价了。

　　这种问题愈演愈烈，导致了理论界和工业界的互不理解的冲突——即便后者并非不了解如何使用前者的成果，甚至前者内部也存在不小的争议。这里的一个例子是不切实际地鼓吹所谓的纯函数式(pure functional) 编程。应当注意，[这种问题](https://news.ycombinator.com/item?id=10175296)的部分根源是哲学思辨和方法论的，引起成果转化困难的并非只是经济活动意义上的供需失衡。语言相关基础教育的缺失使得部分人员难以掌握评价现实需求的普遍适用性难辞其咎。

　　另一方面的背后的潜在影响重大的问题是（某些子领域的）学术权威对实际解释的理解的片面性造成的偏差。这些偏差不少是基础性的，大致表现分为以下几种：

* 已经导致理论不严谨的认知混乱传递到工业界产生更加不可靠的认知，反过来又逆向带偏部分研究者而增加徒劳的争议。这里的一个典例子是关于语言中[类型](typing-vs-typechecking.md)的理解。
* 尚未被工业界普遍接受，但存在的潜在的问题，而在理论界和工业界都尚未被充分了解的观点，如 Robert Harper 的基于对静态语言和（静态）类型系统必要性的立场出发的一些片面观点：
	* [关于“动态语言”的文章](https://existentialtype.wordpress.com/2011/03/19/dynamic-languages-are-static-languages/)。
	* [关于引用透明性(referntial transparency) 的理解](https://existentialtype.wordpress.com/2012/02/09/referential-transparency/)；其中的明显缺陷可以通过对比该问题上更全面严谨（但仍然不完整）的一个[综合论述](http://www.itu.dk/people/sestoft/papers/SondergaardSestoft1990.pdf)找到。
* 因为种种理由产生的主要在工业界流行的片面的理解，和理论界长久以来的认知产生的新的冲突。虽然已经体现某些习惯的不靠谱，但因为流行而无法纠正。这方面的一个例子如[关于“变量”这个基本概念的定义的重点问题](https://existentialtype.wordpress.com/2012/02/01/words-matter/)（另见[这里](variable.md)）。
	* 对“变量”的问题，存在[反驳意见](https://www.yinwang.org/blog-cn/2013/03/31/purely-functional)，但其中搞错了理论上需要维护概念原始含义的动机，在技术上也是站不住脚的（并不适合所有工业界使用的语言，是一种不必要的削弱）。
* 因为种种理由，大多数用户普遍出现偏差的一些常识，如[关于并发和并行](https://existentialtype.wordpress.com/2014/04/09/parallelism-and-concurrency-revisited/)。

　　这里的“种种理由”，其中较明显的之一，是工业界普遍缺乏规格说明等明确的约定。

　　注意对理论研究来讲，这里关于规格说明的认识的要求比具体语言学习的通常更高，而这和学术立场没有很直接的关系。上面已经引用 Robert Harper 的几个不同场景的举例冲突问题；不仅如此，他还是 [Standard ML](http://sml-family.org/) 规范的主要作者。但他在此的经验不能代替非 ML 风格的语言规范的设计问题；技术上来讲，具体到 SML 语言规范上，规则的可修改性也偏弱（即便排除比大多数工业语言强的严格形式化的风格）。不能适应这种合理的需求正是某些观点不适合整个领域的主要原因。然而，不管是支持还是反对，能够清楚问题何在的用户，还是太少了——这应该有很大程度是程序语言相关的入门基础教学的缺失所致。程序设计语言理论这个领域的教学并不够替代此处基础的缺失（特别是已经自认为入门学会某种具体语言，但实际上学得完全不到家的用户）。

# 概念解释

## 规格说明

　　[规格说明(en-US)](https://en.wikipedia.org/wiki/Specification_(technical_standard)) 是一种技术指导文献，规定设计、产品或其它交付物符合预期的要求。

　　规格说明文档在工程上是常用的必要文件，它经常被协调各方关于技术问题的整体的、正式的规范约定，是评价交付物质量的主要依据。

　　在工程以外，规格说明文档也可被作为公开的设计要求参考，而被不同的涉众实现。这种规格说明文档可能直接称为技术标准。

## 变量

　　关于“变量”这个概念的一般定义和含义，以及 C 和 C++ 语言为例的解释，参见[这里](variables.md)。

　　之前提到，要求变量表示可变状态(immutable state) 的[反驳意见](https://www.yinwang.org/blog-cn/2013/03/31/purely-functional)是站不住脚的。因为这两者历来就没有关系。偶然让“使用”变量和“使用”可变状态想通的，就是类似 C 语言的对象(object) 的概念。很遗憾，这个层面上首先就存在不少流行的理解偏差。

　　讽刺的是，不少半桶水 C 用户还信誓旦旦“C 没有对象”（而且很可能认为“C++ 有”），却不知道[一些他们讨论的语言中的基本常识](variables.md)——荒谬到值得在这里老调重弹一遍：

* “对象”是 C 语言最重要且最常用的基本概念。
* C 语言规范没有严格意义上的“变量”。
* C 的对象和 C++ 的对象原则上是一致的。C++ 语言规范明确定义了“变量”，还包括不是对象的实体如引用（虽然和 C 一样不包括更一般概念上的“函数”）。
* 硬要说 C 没有的“对象”，看来是来自“面向对象”的对象，特别是所谓原生支持面向对象特性的以“类的实例”作为“对象”的定义的 Java 这样的语言。但是就算清楚这些事实的，很大可能也不够清楚：
	* C++ 的“对象”的一部分——类类型(class type) 对象——完全符合这个“对象”的概念（虽然严格来讲，只是一类实现），甚至普遍实现中 C++ 的这种对象的一部分（以前的所谓 POD ，现在的 standard-layout class ）在一定条件下的目标代码和 C 的结构体对应的目标代码二进制兼容。
	* Java 这样的 class-based OO 并没有无可争议地代表所有具有“对象”概念的面向对象语言（例如传统上基于原型(prototype-based) JavaScript ）。发明“面向对象编程”概念的 Alan Kay 对这种认知偏差看来也有[很大意见](http://www.purl.org/stefan_ram/pub/doc_kay_oop_en)。

　　这个现状也一定程度体现出 C 的教学质量堪忧。而作为真正敢自称学会 C 语言（或者 C++ 语言）的用户，请做到不信谣不传谣，不要让谎言披上玩笑的遮羞布，口嗨了一千遍就变成了真理——这是对清楚事实的真正认真学习过基础的用户的侮辱。

　　“变量”替换“可变状态”多少也是类似的谣言。虽然不便追踪具体来源，根据对不同语言用户的观点的考察，有理由相信这是只使用过变量能表示可变状态的对象的语言的用户和/或 C 这样的语言学得不到家的用户以讹传讹的结果。这也能解释为什么反驳意见以 Robert Harper 笃信纯函数式“宗教”入手了，因为纯函数式语言就是最典型地存在不可变的变量的主要实例（如 Haskell 的 type variable ）。

　　但是，这个动机根本是错的。避免变量和表示可变状态的对象的混淆，根本理由是混淆本身就会造成无理的问题。要说“变量”该是什么合理含义，那就该是保持最初的含义——关联可能可变的变量绑定的实体。这个概念在历史上的数学、程序设计语言理论和具体语言的认知都兼容——而且普遍包括“变量”和表示可变状态的对象等义的设计中。不顾这个事实，仅因为个别语言设计上的来源可疑的片面理解就去修改“变量”的概念，在这个意义上就是一种损人不利己的**寻衅滋事**：

* **没事找事**地破坏普适概念对不同领域的兼容性，制造理解偏差和不同语言用户之间的交流障碍。
* 那些因为设计者信谣而把“变量”意思领会错或者随大流等原因在语言规范中将错就错、以讹传讹的例子，应当作为反面教材，本不应该被理智的用户尊重，更不应该被纵容到必须让其它合理设计去兼容它的程度。反客为主宣扬向无知妥协才是“正统”——这是一种**反智**。

　　另外，严格意义上讲，实际问题更加微妙一些——以 [Robert Harper 使用的术语](https://existentialtype.wordpress.com/2012/02/01/words-matter/)，所谓可赋值(assignable) ，是一种接受特定操作的实体，一般意义上并不意味着这种操作必须负责保证确保状态可变，因为状态是不是可变未必是局域特性，还可能是整个语言的语义统筹接管的。如 C++ 可观察行为不包括任意的状态修改；其中的 `std::is_assignable` 并不要求判断是否这样的操作实际修改了对象的值。当然，因为可修改(modifiable) 和可变(mutable) 其实有一些技术上的不同，这里仍然可以做到自洽。而这里的不同其实显示了当前语言设计普遍都不够抽象清楚计算作用(computational effect) 的问题；若是一直稀里糊涂地混用概念，洞察这些问题的可能性会显著缩小。不过，具体如何地有关，这就和“变量”的关系不大了。
