﻿# UniGal-supportlist

## UniGal对各引擎的支持详表

| 引擎代系 | 引擎名称             | 引擎主流语言 | 存活状态     | 引擎原生支持             | 双向导入导出 | 可从Unigal导入 | 可导出为Unigal | 暂无支持计划 |
| -------- | -------------------- | ------------ | ------------ | ------------------------ | ------------ | -------------- | -------------- | ------------ |
| UniGal   | UniGal-Prototype     | C++          | 原型         | √（开发中）              |              |                |                |              |
| Krkr     | Krkr                 | TJS          | 已停止维护   |                          |              |                | √（开发中）    |              |
| 面包工坊 | [BKEngine](https://bke.bakery.moe/index.html) | bkspr        | 已停止维护   |                          |              | √（开发中）    |                |              |
| Unity    | [Unity-Nova](https://github.com/Lunatic-Works/Nova) | Lua/C#           | **活跃**     | （正在说服开发者）       | √（开发中）  | √（开发中）    | √（开发中）    |              |
| Python   | [Librian](http://librian.net/) | liber        | **活跃**     | （正在说服开发者）       | √（开发中）  | √（开发中）    | √（开发中）    |              |
| js       | [AVGPlus](https://avg-engine.com/) | json         | **活跃**     | （考虑要不要联系开发者） |              |                | √（开发中）    |              |
| js       | AVG.js               | json         | 未知         |                          |              |                | √（开发中）    |              |
| js       | Renjs                | javascript   | 未知         |                          |              |                | √（开发中）    |              |
| Python   | [Renpy](https://www.renpy.org/) | Python       | **活跃**     |                          |              |                | √（开发中）    |              |
| Strrationalism | Snowing              | C++          | 缓慢，**对开源不积极**，出于基于开放来源的设想考虑移除 |                          |              |                |  √（艰难开发中）              |           |
| json     | [Monogatari](https://monogatari.io) | json         | **活跃**     |                          |              |                | √（开发中）    |              |
| json     | GameCreator          | 未知         | **活跃**     | （考虑要不要联系开发者） |              |                | √（开发中）    |              |
| Unity    | Unity-Utage          | C#           | **活跃**     |                          |              |                |                | √            |
| Unity    | Unity-Fungus         | C#           | **活跃**     |                          |              |                |                | √            |
| Unity    | Unity-Kirino-Engine  | C#           | 已停止维护   |                          |              |                |                | √            |
| Unity    | Unity-XiheAnimation  | C#           | 未知         |                          |              |                |                | √            |
| SDL      | VoidMatrix系列        | C++          | **活跃**     | （正在与开发者合作，已经提供XML读取支持了） | √（开发中）  | √（开发中）    | √（开发中）    |              |
| 橙光     | 橙光文字游戏制作工具 | 可视化       | **生不如死** |                          |              |                |                | √            |
| 橙光     | iFAction             | 可视化       | 活跃         |                          |              |                |                | √            |
| 橙光     | EvkWorld幻境         | 可视化       | 未知         |                          |              |                |                | √            |

## 关于请求各位引擎开发者能够提供的帮助的说明

### 语法方面

有很多语法上面不清晰的地方，还是希望能直接引用文档的，当然大部分引擎的文档都很出色。我们是希望能引用一个开放的文档而不是私有的文档，只是群文件的话，恐怕不便于直接引用和给出参考链接，毕竟互联网是开放的，只要可能，我们没有必要建设一个私域流量的网络吧~

### “引擎自身支持”方面

（已经试着打入各位开发者的交流群并且试着和大家做好友了）但是因为太菜而瑟瑟发抖不敢说话。

此外，最终没有打算提供JSON或者YAML版本的UniGal标准写法，是因为认为这个应该是引擎内完成的事情。有的引擎基于js所以偏向json，有的基于python所以偏向yaml，如果分别维护分支，工作量会很大，会很难维护的过来。

因此，出于可交换性和统一性的考虑，只提供一个XML的写法。因为现在各种常见编程语言下，不论是XML还是JSON，都有很成熟的库可以使用，而且XML和JSON/YAML互转也是有方法的。如果您的引擎确实不能处理XML，可以考虑在引擎读入XML的时候自动转换一个temp的JSON文件。若是需要写入，先写JSON，再写回的时候再把JSON转XML，也是一种引擎内的实现吧。

因此，觉得这将会极大增加各位引擎开发者的工作量。并且，UniGal的语法也会随着演进而不断的滚动变更，要各位开始就实现很多功能但是后期却发生变更的话，想必也是过意不去的。我们只是作为一个标准制定和推行者，不可以也不应该去强制各位遵循的。

不过如果可以，可以从```<text></text>```这块下手，至少text上，UniGal的标准是基本定型了的。而纯粹针对文本的转换和读取，执行，技术上的调整和难度也是最小的。可以以某个确定版本的标准（如0.1.0）来尝试去实现。希望这可以成为大家合作的开始。UniGal社区在此再次感谢各位引擎开发者。



## 关于支持列表的补充说明

### 遇到的困难

1. Strrationalism的Snowing引擎，暂无公开的文档，也没有面向大众统一开放使用的计划。因此对于该引擎的支持将基本依赖大量读代码，而且结构非常繁杂，代码量众多。

有兴趣可以去看看他的Parser，或许可以找到一点思路。（总之感觉需要重点看Yukimi文件夹）https://github.com/Strrationalism/Snowing/blob/master/Yukimi/ScriptParser.cpp

2. Unity系的不少商业框架，文档不便。

### 不会考虑支持的引擎和原因

橙光文字游戏制作工具：**业界毒瘤**，捆绑平台，逼迫作者吊死在自家一颗树上

iFAction：是商业引擎并有基于账号云端验证的加密功能，作品的打开需要掌握在引擎制作方的手里，提供导出工具既与开发者的盈利和用户素材安全违背，又不符合本项目开放的初衷。

EvkWorld：曾经以群邮件的形式大量向使用者推销官方的打卡课程。并且该引擎并非专注于AVG，而是杂糅式的的多功能引擎，但又高度依赖模板，在AVG的可扩展空间不一定足够大。

### 更多支持计划

更多引擎，可以见visual-novel-engine的[Github Topic](https://github.com/topics/visual-novel-engine)。其中已经有一些引擎已在本支持名单中。

我们选择支持一个引擎的理由主要是考虑以下几个因素：

+ 其用户基础和体量
+ 其完成程度
+ 其对开发者的友好程度
+ 其使用的开源协议是否足够开放
+ 其是否有足够的面向中文用户的开发文档
+ 其是否有很好的i18n支持、a11y支持和跨平台支持
+ 其是否有良好的用户社群。

## 注意事项

1. 大小写严格，如果有拼写错误是会报错的。

2. 此外，不正确的缩写和习惯名称也会报错。

我们不是不想做更丰富的支持，更人性化的支持。只是我们实在不能相信前端的输入和用户的输入，为了尽可能减少错误的可能，我们采用了严格的UEP来对异常进行管理。错误的引擎名称将可能导致UEP-E-0006错误。

