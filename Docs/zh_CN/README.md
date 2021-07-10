# UniGal-中文文档

## **【一定要看】**[UniGal-guideline.md](UniGal-guideline.md)

暂不创建这个文件，而是把纲领和注意事项直接列举。因为**一定要看**

>
>1. UniGal-Script/Diagram的后缀名为.unigal
>
>2. UniGal-Script文件分为```<head></head>```与```<body></body>```，其中```<head></head>```不涉及具体内容，而是存储各类配置，而```<body></body>```则是脚本的具体内容。
>
>3. UniGal-Script提供注释
>
>给电脑看的需要展示出来的注释用```<comment></comment>```封装
>
>给人看的纯粹开发的时候方便了解是啥的，今后统一用```<!-- {{comment_content}} -->```写，就不要暴露出来给解析脚本的时候添麻烦了。已有的存量代码逐步实行更改。
>

**接下来的工作重点将在codeblock和resource上**

此外，没有特殊规定的话，引擎名称均遵守首字母大写，在```<head></head>```中的引擎名称应保持与这里一致，作为本框架对大家的官方称呼。

## [UniGal-main.md](UniGal-main.md)

如果要整体了解所有各类已经有的原子操作，相当于以下resource、text、layer、code的总大纲。

但是都不够详细，适合形成大致印象。

## [UniGal-resource.md](UniGal-resource.md)

想看资源调度和素材管理相关的部分，可以参考本文档。

+ [BKEngine](UniGal-resource.md#BKEngine)
+ [Librian](UniGal-resource.md#Librian)
+ [Nova](UniGal-resource.md#Nova)
+ [AVGPlus](UniGal-resource.md#AVGPlus)

## [UniGal-text.md](UniGal-text.md)

本文档重点强调了各个引擎中的文本控制方式，也是Galgame的核心——文字。

+ [BKEngine](UniGal-text.md#BKEngine)
+ [Nova](UniGal-text.md#Nova)
+ [Librian](UniGal-text.md#Librian)
+ [Renpy](UniGal-text.md#Renpy)
+ [AVGPlus](UniGal-text.md#AVGPlus)
+ [Monogatari](UniGal-text.md#Monogatari)
+ [GameCreator](UniGal-text.md#GameCreator)
+ [iFAction](UniGal-text.md#iFAction)

## [UniGal-EnforcementProposal.md](UniGal-EnforcementProposal.md)
UniGal的异常处理提案。用于解决不同引擎间转换不完美的问题和处理错误。
若要详细了解建议移步[Uni-Gal/UniGal-EnforcementProposal](https://github.com/Uni-Gal/UniGal-EnforcementProposal/)。

## [UniGal-layer.md](UniGal-layer.md)
想看图层的实验性选项，看layer。目前尚不够完善，欢迎您来开荒式的定义。

## [UniGal-codeblock.md](UniGal-codeblock.md)
想看内嵌代码段，看codeblock。目前尚不够完善，欢迎您来开荒式的定义。

## [UniGal-reference.md](UniGal-reference.md)
啥都不想看只看还有什么需要拆分操作，看reference

animation.md

action.md

environment.md

顺序有待调整，是按照字母顺序还是按照重要性，有待研究。但如果按照重要性，resource要放在text之后了？

## [UniGal-keyword.md]

关于UniGal中的可互换关键词
可以是因为英式美式英文差异造成的近义词，也可以是因为主观感受造成的近义词

总之，它们可以被互换（在编译器里的后果就是需要多加一层if了）

+ Opacity/Transparent
+ Effect/Ambient

此外，有同行提到的关于unigal中的关键词问题，unigal中如果说是描绘一个功能的关键词，您可以看main这个文档和resource、layer、text

但是如果是说保留字关键词的话，我想unigal不存在保留字的问题，因为它的内容一定是被xml的令牌封装起来的。## UniGal中的可互换关键词

可以是因为英式美式英文差异造成的近义词，也可以是因为主观感受造成的近义词

总之，它们可以被互换（在编译器里的后果就是需要多加一层if了）。如果同时出现，需要按照优先级解析。根据计算机行业的事实规范，虽然不愿承认，但应以en_US的写法优先。

即：均空则空，一空则另，均有则美式优先。

|词汇|en_US|en_UK|
|--|--|--|
|透明度|Opacity|Transparent|
|颜色|Color|Colour|
|中心|Center|Centre|

对于因主观感受造成的近义词，我们采用在大部分引擎文档中出现次数多少来规定。

+ Effect/Ambient （其中Effect优先）

此外，有同行提到的关于unigal中的关键词问题，unigal中如果说是描绘一个功能的关键词，您可以看main这个文档和resource、layer、text

但是如果是说保留字关键词的话，我想unigal不存在保留字的问题，因为它的内容一定是被xml的令牌封装起来的。

## UniGal不会涉及的

UniGal不会涉及DRM加密方面的内容，也不会涉及已编译完成的游戏解包并转换格式的内容。

一是不同引擎之间的DRM加密实现方法存在巨大的差异，粒度也各有千秋，难以统一。且这方面的实现和细节对于引擎间迁移并无帮助，有时这就是可以防止迁移而涉及的。

二是关于DRM实现方面的标准，若以具体引擎作为例子，将会助长反编译和破解的势头，对游戏开发者不利。同时容易让引擎作者和游戏开发者因为利益相关而冒犯。

三是该部分研究不存在也不应存在通用标准。DRM加密就本应当是站在出其不意的地方验证来恶心破解者的，因此我们若非破解者，对这部分进行定义和规范是没有任何必要的。

但我们仍无法百分百的阻止有心之人基于本标准开发破解技术，因为没有百分百可靠的技术。
