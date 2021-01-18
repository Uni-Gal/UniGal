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

## [UniGal-main.md](UniGal-main.md)

如果要整体了解所有各类已经有的原子操作，相当于以下resource、text、layer、code的总大纲。

但是都不够详细，适合形成大致印象。

## [UniGal-resource.md](UniGal-resource.md)

想看资源调度和素材管理相关的部分，可以参考本文档。

+ [BKEngine](UniGal-resource.md#BKEngine)
+ [Librian](UniGal-resource.md#Librian)
+ [Nova](UniGal-resource.md#Nova)

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

此外，没有特殊规定的话，本名称均遵守首字母大写，在```<head></head>```中的引擎名称应保持与这里一致，作为本框架对大家的官方称呼。

## [UniGal-layer.md](UniGal-layer.md)
想看图层的实验性选项，看layer。目前尚不够完善，欢迎您来开荒式的定义。

## [UniGal-codeblock.md](UniGal-codeblock.md)
想看内嵌代码段，看codeblock。目前尚不够完善，欢迎您来开荒式的定义。

## [UniGal-reference.md](UniGal-reference.md)
啥都不想看只看还有什么需要拆分操作，看reference