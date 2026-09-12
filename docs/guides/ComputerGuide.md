# 也许是一篇计算机指南

`更新中。上一次更新日期：2026.9.12`

`本文档原本发布于班级周刊，现发布于网络供大家参考。`

作者：Copy&Paste

## 0. 前言

本文内容大幅度摘抄参考的文献有：[北京大学计算机基础能力手册](https://github.com/ZangXuanyi/getting-started-handout)、[LCPU Getting Started](https://missing.lcpu.dev/)以及[《【网络基础】通俗易懂的搞明白什么是IP地址（大白话版）》](https://blog.csdn.net/pagnzong/article/details/112127329)等网络文章。

很多人在经过了约7.5年的计算机学习后，除了掌握了信息技术会考内容以外，甚至可能连正确安装软件都做不到。本文正是为了解决这个问题而写。考虑到大家的学习能力较强，本文包含一些扩展内容，但是我认为这些内容对大家以后使用计算机同样有帮助，因此建议阅读全篇。

为了提高信息密度，有很多重要的内容做成了练习，强烈建议看一下，尤其是基本常识部分。


## 1. 获取信息

### 1.1 搜索

搜索是现代人类的必备技能。遇到不懂的问题，首先要么考虑搜索，要么考虑询问大语言模型（Large Language Models，LLM），相比于询问他人，这两条途径有更高的效率，也有更高的获得答案的几率。本文有很多的搜索小练习帮助你掌握搜索技能。

搜索引擎推荐必应（Bing，[www.bing.com](www.bing.com)，国内版[cn.bing.com](cn.bing.com)）和谷歌（Google，[www.google.com](www.google.com)，如果你能访问的话）。大语言模型更新迭代较快，这里不做推荐。

#### 1.1.1 搜索技巧

1. 关键词：我们使用完整句子进行搜索的时候，搜索引擎会利用语言模型将其拆分成多个关键词进行搜索，而语言模型总会导致一定的偏差。所以搜索的时候请用关键词而不是用一个问句！！！不同的关键词之间用一个空格隔开。
2. 使用英文：中文互联网的一大特点是信息向应用内部收缩，形成无法被搜索引擎检索到的「深网」，导致中文开放互联网的信息量小于英文开放互联网的信息量。（点名批评微信、小红书……）并且英语依然是世界上最通用的语言，尤其在技术、科学等领域，大部分的文献、资料、教程、说明等都是用英文写的；相关领域的研究材料往往也先以英文发表。因此搜索时使用英文往往能够得到更好的结果。

3. 双引号：将关键词放入英文双引号中，可实现精确匹配，搜索结果必须包含完全一致的内容。例如搜索「"人工智能发展历程"」，只会返回包含该完整短语的页面。（其实不好说，但是这个技巧是有帮助的）

4. 减号：排除不需要的关键词，如「人工智能 -深度学习」，可过滤掉包含「深度学习」的页面。

5. filetype:：指定文件类型搜索，如「时间简史 filetype:pdf」，只返回PDF文件。

6. site:：限定搜索特定网站，如「CS50P site:github.com」，只在GitHub上搜索相关内容。

7. 同义词搜索：尝试不同表达方式或同义词组合，扩大搜索覆盖面。

8. 时间与范围限制：部分搜索引擎支持按时间或特定范围筛选结果，便于获取最新或特定时期的信息。

9.  更换搜索引擎：实在搜不到可以试试。

10. 特定的搜索工具：可以搜索一些特定的信息，例如Google学术和微软学术可以高速查找论文和引用；GitHubCodeSearch可以帮助我们搜索GitHub上的代码片段；GoogleLens、Bing Visual Search 等可以帮助我们通过图片搜索相关信息。

11. 再不行去找LLM吧。



#### 1.1.2 信息的可靠性

其实大家都具备一定的信息判断能力，最没判断能力的是那种拿着豆包生成的信息到处乱来的。以下几个方面有助于判断信息的可靠性：

1. 来源：信息的来源是否可靠？是否来自权威机构、专家或者知名网站？

2. 时间：信息是否及时？是否过时？

3. 评价：其他人对该信息的评价如何？是否有很多人认可？

4. 完整性：信息是否完整？是否有遗漏？

5. 可验证性：信息是否可以被验证？是否有相关的证据？



#### 1.1.3 小游戏

现在是头脑风暴时间！本关不考验你的搜索能力，尽情通灵吧！下面这个小游戏摘抄自Jack Lance的解谜作品[Rt3](https://jacklance.github.io/rt3)。小游戏没有标准答案，你可以在搜索引擎自行验证，我推荐使用Google[^1]，访问不了的话就用Bing。

[^1]: 我做的时候用的Google，两个搜索引擎的效果不一样。如果你使用的是Google，请在你的浏览器中安装“显示Google搜索结果数量”插件。

为了让大家获得原汁原味的体验，我们把英文原文放上来。

***\*Q1：\****

This theme of this riddle search's intermission is finding phrases that fit constraints on how many google results they have.

For this first riddle, the goal is to find something such that if you google it in quotes before " dog", it has over a million results, but if you google it in quotes before " cat", it has less than a hundred thousand results. For example, if "cute dog" had over 1,000,000 results but "cute cat" had less than 100,000 results, then "cute" would complete the riddle.

Some notes:

1.  There must be a space before the word "dog" and "cat"

2.  It is allowed to be more than one word (e.g. "what to feed my dog" & "what to feed my cat")

3. You don't have to use Google, you can use your favorite search engine as long as it shows the number of results for your query.

4. I wrote the words "a million" and "a hundred thousand" out in words to bring attention to the fact that they are different numbers with different amount of zeros, because otherwise it was missable, and am writing this bullet point for the same purpose.

***\*Q2：\****

I'll stop writing "when searched in quotes" for the rest of these riddles, but know that every time I talk about searching, I'm mean searching in quotes

For this riddle find a phrase that has:

1. More than a million results when preceded by "blue "

2. More than a million results when preceded by "red "

3. Less than a million results when preceded by "green "

4. Less than a million results when preceded by "yellow "

### 1.2 信息平台

#### 1.2.1 官方文档、Wiki、论坛

如果我们希望获取某软件等的信息，最好的地方往往是其官方文档；对于纯由社区维护的项目，其官方Wiki与论坛也是获取信息的最佳选择之一。但是！官方文档可能晦涩难懂，你可以选择其他地方的更加易读的指南，但请确保其可信度。如果你在学一门技术，你最好还是得看看官方文档，哪怕晚一点也没事。

如果你在请求问题的时候，遇到了诸如「RTFM」（Read The F**king Manual）的回应，这说明回答者认为你需要搜索官方文档和使用手册。当然在这种情况下，他大概率是对的，你应该去读一读。同样道理的还有STFW（Search The F**king Web）和RTFSC（Read The F**king Source Code）。而通过这种方式搜索信息，你能够学到的内容比往往直接告诉你答案要多得多。

#### 1.2.2 GitHub

但凡接触编程就不能不接触的平台，事实上没接触编程也可能接触GitHub。

GitHub是一个代码托管平台，用户可以在上面存储和分享代码。GitHub上有很多开源[^2]项目，用户可以在上面找到相关的代码和文档。同时，它也是一个非常重要的开源社区，当你对某个项目有疑问或者发现Bug的时候，你可以对该项目提出Issue，只要项目没「死」，总会有人告诉你答案。

[^2]: 开源软件的源代码任何人都可以审查、修改和增强。

#### 1.2.3 Wikipedia

维基百科是一个百科全书网站~~，爆杀\*\*百度百科~~。维基百科是一个社区驱动的网站，用户可以在上面编辑和修改条目。维基百科的内容是由志愿者编写和维护的，因此它的准确性和可靠性可能较低（但是我看也比百度百科好用），不过它仍然是一个非常有用的信息来源。维基百科的搜索功能也很强大，可以帮助用户快速找到相关的条目。

最大的问题是，很可能无法访问。

#### 1.2.4 其他平台

国内能够算上优质平台的有：博客园、哔哩哔哩、知乎……。这些平台普遍是免费的，你可以找到许多关于技术、编程、科学等方面的文章和视频。它们的内容质量参差不齐，也不乏卖课的，但是它们仍然是一个非常有用的信息来源。我们在接受信息的时候，仍然需要判断其可靠性。

CSDN上虽然也有不少信息，但是该平台质量较低，我们必须在海量的AI水文、抄袭博客、低质付费文字、商业广告等无用信息中找到夹缝中的少数高质量文章，这是一件极为痛苦的事情。虽然在少数情况下我们最终能够找到一些有用的信息，但是高质量的平台能节约鉴别信息的精力。（上文有个方法可以帮你从搜索结果中去除CSDN的内容）

### 1.3 LLM

LLM是大语言模型的英文简写。LLM的输出除了受到语法、语义等语言学因素的影响和模型本身的影响以外，还受到输入的Prompt（提示词）的影响，因此我们可以通过优化Prompt来在不改进模型性能的条件下尽量优化LLM的输出。这个领域被称为「提示词工程」（Prompt Engineering）。

我们在使用LLM时应当遵循以下原则：

1. 具体性：使用LLM的时候提问应该极为具体，避免使用模糊、省略的语言或者关键字。例如我们如果想要获取改善睡眠质量的信息，应该使用「如何改善睡眠质量」而不是「改善睡眠」等关键字组合。这和搜索引擎不一样。

2. 明确性：在使用LLM的时候，我们的Prompt应该明确无歧义。相信大家的语文水平都没有问题。一个小技巧是我们可以在Prompt中规定其输出格式，例如提供一个示例，这对获得期望的输出非常有效。

3. 简单化：目前的AI依然缺乏处理复杂问题的能力。当我们提出一个复杂的问题时，LLM往往会混乱，进而得出错误答案。这时，我们可以把一个大问题分成多个小问题，然后让LLM分别解决这些小问题，然后合并答案。

4. 你可能需要通过搜索等途径确认LLM提供的信息的真实性。

5. 在对提高你的工程能力等的课程作业等上面不要使用LLM！否则等于自废武功。

最后，关于提示词工程，请参见[菜鸟教程](https://www.runoob.com/ai-agent/prompt-engineering.html)等，这里不做说明，因为我也不会。

`小练习：对于LLM而言，什么是「上下文」（context）？`

### 1.4 提问

请参见[《提问的智慧》](https://lug.ustc.edu.cn/wiki/doc/smart-questions/)。


