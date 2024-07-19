# MC各种服务端

这里是说明文档，这里会简单介绍各个核心以及插件。了解更多请自行bing，百度是个**。  
部分介绍收集自网络

# 核心介绍

核心是一个.jar文件，使用启动命令将其启动并完成配置就可以开服开服教程可以看我的blog文章：[使用mcsm面板搭建我的世界服务器|meiのblog (mmeiblog.cn)](https://mmeiblog.cn/archives/shi-yong-mcsmmian-ban-da-jian-wo-de-shi-jie-fu-wu-qi)

## 原版

由mojang官方制作的核心，不推荐使用。

## Hose

Java版 核心

> MITE 是一款提高游戏的生存方面难度的综合类 MOD，通过重新定义并调整游戏机制来增加生存的难度。此为 MITE 官方服务端，无法安装其他任何 MOD 包括 Forge。  
> 作者：PixelBBS https://www.bilibili.com/read/cv19386482/ 出处：bilibili

### Vanilla

我的世界Vanilla核心是官方提供的原版游戏服务器核心，它是最基本的服务器核心，可以提供原版游戏的所有功能。Vanilla有着简单的配置方式和不错的稳定性，但功能不够强大，无法满足大多数服务器的需求。

## Fabric

Fabric服务端需要搭配Fabric API才可以安装mod，本站不提供Fabric服务端下载，因为你可以在官网自行搭配Fabric组合。  
[Download Minecraft Server Launcher | Fabric (fabricmc.net)](https://fabricmc.net/use/server/)

> Fabric是一个轻量级的MOD API，用于Minecraft1.14及以上版本，主要作者是asiekierka和modmuss50。  
> Fabric由两部分组成，包括Fabric API和Fabric Loader，Fabric Loader主要用来实现MOD加载功能，Fabric提供一些基础的接口供开发者使用，允许其他MOD注册物品、模型、方块、图形界面等，允许MOD通过SpongePowered Mixin修改Minecraft字节码，这一点相对于Forge来说更加安全，因为Mixin能够更好的控制字节码的改动。  
> Fabric并不采用 Mod Coder Pack。它有自己的反混淆工程，名叫“yam”（原名 pomf）。yarn 是开源的，任何人可以贡献，开源协议是 CC0 1.0 Universal。因为 Mod Coder Pack 协议限制，给 Fabric 的贡献的内容不能来源于 Mod Coder Pack。  
> Fabric更新的速度非常快，基本上党最新版本的Minecraft发行的时候，Fabric会在最短的时间内跟进，真的非常方便！---zeruns

## Forge

Forge服务端，支持Forge mods

### 介绍

> 目前 Minecraft 的主流 API，目前有半数以上的模组都在使用 Forge，以易于与 Minecraft Java Edition 的驳接。  
> 一般情況下 Forge 的更新速度很快，一般在 Minecraft 正式版本发布后的一天内更新，偶尔有出现因为一些测试需求在 Minecraft 快照发布后更新的（出现过适用于特定快照版本的 FML）。  
> Forge 是一个版本支持度极高的 API，远古版本 ~ 最新版本 均有支持。  
> 运行任何带有 Forge 的 Minecraft 时，在主界面点击“Mods...”按钮均可显示正在运行的模组，其中 Minecraft、Minecraft Forge、Forge Mod Loader (FML) 和 Mod Code Pack (MCP) 都是 Forge 的核心模组（旧版没有 Minecraft，新版没有 FML 和 MCP），必定默认出现在模组列表。---mcbbs

## 混合端

同时支持模组和插件的服务端

### Kcauldron

#### 支持

Forge模组，Spigot插件

#### 介绍

老式 Forge 服务端，兼容插件 + Mod

### Thermos

#### 支持

Forge模组和Bukkit插件

#### 介绍

1.7.10 Forge 服务端，兼容插件 + Mod，兼容性好.KCauldron的优化版本

### Uranium

#### 支持

Bukkit, Spigot 插件以及 1.7.10 的 Forge mod

#### 介绍

1.7.10 Forge 服务端，兼容插件 + Mod。Uranium端（不断更新）是kc（停止更新）以及Thermos（停止更新）的优化以及后续版本，修复了更多的mod以及服务器bug，稳定性和适用性更强，并且是国人制作的服务端，更适合中国的腐竹。Uranium 是一款基于 KCauldron 进行大量修复以及优化的服务端，并且整合了部分 Thermos 对服务端进行的修复，能够兼容 Bukkit, Spigot 插件以及 1.7.10 的 Forge mod，并没有计划向高版本兼容

### Arclight

#### 支持

Arclight支持Forge模组，Bukkit插件。

#### 介绍

我的世界Arclight核心是一个开源的我的世界服务器核心，它是为那些寻求一个轻量级、可扩展的我的世界服务器核心而设计的。它包括了原版游戏的全部功能，并且拥有高度的自定义和扩展性。

### Catserver

#### 支持

CatServer支持Forge模组，Bukkit+Spigot插件。

#### 介绍

国内最早开发的高版本核心, 支持大部分MOD和插件同时稳定运行

### Mohist

#### 支持

Mohist支持Forge模组，Paper系列插件。

#### 介绍

> Mohist 是一个全新的 Minecraft Forge 服务端，核心采用 Forge + Paper 结构，开发环境使用 ForgeGradle，支持 Forge mod 和 Paper 系列插件。Mohist 目前稳定性良好，仍在不断更新。---zeruns  
> ps:据说现在mod开发者都很讨厌mohist

### SpongeForge

#### 支持

SpongeForge支持Forge模组，Sponge插件。

#### 介绍

> Sponge 是一个全新的服务端，支持 Sponge 的专用插件，可装 Mod，兼容性比 Cauldron 相比提高了不少，适合开 MOD 服，支持的版本非常高，是目前支持 MOD 的服务端里兼容版本最高的服务端。  
> 但是 Sponge 本身不支持 Bukkit 插件（即使有兼容层，效果也不是很好，只能支持一般的插件），需要服务器的配置比较高，启动速度不佳。---zeruns

## 插件服

顾名思义，支持插件的服务端，很多。

### CubeRite

#### 支持

Bukkit插件

#### 介绍

> CubeRite 是一个基于 C++ 编写的开源高性能 Minecraft 服务端  
> 目前 Cuberite 已经可以做到大部分的基于 Bukkit 架构的 Minecraft 服务端（例如 Spigot）的功能，并且在性能方面具有更大的优势。  
> 作者：PixelBBS https://www.bilibili.com/read/cv19386482/ 出处：bilibili

### GlowStone

#### 支持

Sponge,Bukkit插件

#### 介绍

> GlowStone 萤石是一款开源的 Bukkit 服务端，开发者可以根据自己需求修改或制作一个服务端，内置了 Sponge 支持的插件。  
> 作者：PixelBBS https://www.bilibili.com/read/cv19386482/ 出处：bilibili

### Akarin

#### 支持

Paper系列插件

#### 介绍

基于 Paper 进行优化的服务端，性能较好

### Folia

#### 支持

Folia支持Paper系列插件

#### 介绍

> Folia是PaperMC组织最新的项目，旨在实现真正的多线程和区域化心跳。该项目的目标是提供更好的可伸缩性和性能，并修复一些长期以来限制Minecraft服务器扩展的问题。Folia是由Minecraft优化传奇Spottedleaf开发的Paper的分支版本，旨在为真正多线程的服务器提供无妥协的解决方案，通过全新的API集成，实现了每个区域都具有自己的独立线程池和心跳循环的实现。本文旨在以易于理解的方式呈现信息，并提供一些在官方公告中可能没有涵盖的详细见解。  
> Folia项目的优势包括：可有效缩放的性能、局部化的性能优化、更加接近Vanilla单人游戏的实体生成行为、TPS报告的增强以及支持Folia的插件。Folia适用于中型到大型服务器，尤其是那些拥有足够硬件（线程）支持的服务器。对于那些散落的玩家比较多的游戏模式，如生存多人游戏、空岛等，Folia可以完全利用Regioniser提供的性能优势。同时，对于那些想要扩大运营规模的小型服务器网络来说，Folia可以使他们不必过多地复杂化设置。  
> Folia项目是一个有着革命性意义的项目，旨在提升Minecraft服务器的性能表现，让游戏体验更加顺畅。  
> 原文：Folia - Multithreading Coming to your Minecraft server | Paper Chan hideout (paper-chan.moe)  
> 作者：contextual_bandit  
> 链接：https://juejin.cn/post/7216594359115726904  
> 来源：稀土掘金  
> 著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

### Paper

#### 支持

Paper支持Paper系列插件

#### 介绍

> PaperMC 通过快速、安全的软件和扩展的插件 API 改进了 Minecraft 的生态系统，作为使用最广泛、性能最稳定、最稳定的软件，提供快速发布和有用的支持。---paper官网

### Pufferfish

#### 支持

Pufferfish支持Paper系列插件

#### 介绍

Pufferfish是Paper的高性能分支，旨在提供企业功能并最大限度地提高性能。

#### Pufferfish Plus

Pufferfish Plus是我们Pufferfish的改进版本，其中包括企业支持和其他异步功能，例如异步实体跟踪器和异步寻路系统。在基准测试中，它比标准版本的河豚快约 25-30%。

### Mirai

**已停止更新**

#### 支持

支持Paper系列插件

#### 介绍

来自“未来”的服务器核心,基于 Pufferfish.此项目是实验性的，如果您还没有准备好面对可能的错误，则不鼓励在生产环境中使用它。

### Purpur

#### 支持

Purpur支持Paper系列插件

#### 介绍

> Purpur 是 Paper 服务器的直接替代品，专为可配置性和新的、有趣的、令人兴奋的游戏玩法而设计 特征。---purpur官网介绍机翻