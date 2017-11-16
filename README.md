来宝：开源人工智能
=================

[![Build Status](https://travis-ci.org/jjwang/laibot.svg?branch=master)](https://travis-ci.org/jjwang/laibot)

## 这码农咋想的？

来宝项目的由来是因为2017年智能音箱太火了！当我在看基于淘宝可购买的硬件电路板以及免费语音服务如何构建智能音箱时，我找到了[japser-client](https://github.com/jasperproject/jasper-client)和[dingdang-robot](https://github.com/wzpan/dingdang-robot)这两个项目。Jasper完成了一个大概的框架，但是没有集成对应的汉语服务；Dingdang基于Jasper继续演进。不得不说，Dingdang开发的确实非常好，集成了很多的服务、编写了大量的文档，使得一个新手很容易入门。

但是，Dingdang并不是我想要的。就智能音箱这个方向来说，众多巨头涌入的是一个2亿的小市场，小市场的由来是因为用户接受度不高（画外音：什么？天猫双十一卖了一百万台？OMG，我可什么都没说）。归根结底，就是现在的汉语普通话智能音箱方案用户体验不佳，说是智能、经常情况下是智障。如果方案在用户体验上没有任何优势，集成了再多的服务实际上用处并不大。

说了这么多，那么来宝想干嘛？其实很简单，来宝就是想试一下基于当前可用的开源软硬件和免费语音服务，能打造的语音助理最好能到什么样子？Jasper和Dingdang从优化的角度来说还做的不够，这些是来宝所想做的。

好吧，这就是来宝的由来！能做到什么程度，说实在的，我也不知道，走走看吧！和Dingdang一样，来宝也基于Jasper。

## 先选定硬件

硬件肯定是基于树莓派了。树莓派是台全功能卡片尺寸电脑，可以运行多种操作系统，支持键盘、鼠标、显示器等。选择树莓派的好处就是即使觉得这个音箱没啥用，还有好多其他有意思的玩法。小朋友可以玩，装个Scratch。喜欢小米产品的大朋友可以玩，装个Home Assistant，恩，成了智能家居控制中心；话说，智能音箱的理想不就是智能家居控制中心么？

既然是智能音箱，音频输入音频输出必不可少。我的选择是：麦克先用单麦，后面再尝试多麦，树莓派的多麦解决方案现在也是多如牛毛了啊。外放用USB微型音箱，不需要外接电源的那种。这样，整个音箱就可以用一根Mini USB线给点亮啦！

另外的一个大问题是造型！无论是Jasper但是Dingdang Robot，造型太挫或是没有造型。一堆线连来连去，看起来乱糟糟的，处女座那是相当的烦心。所以，咱们需要一个专业的外壳。咱没必要外壳用金属，再类似小米发布会普及的、用6000目砂纸细细打磨，说实在的，磨的再亮也没用。那咋搞？3D打印机，咱打印个外壳。

网上可以下载到各种各样的外壳文件去打印，这里不一一赘述了。第一个版本我选的是IBM的TJBot，看起来也是蛮酷的，有个胳膊还能动。

## 项目的规矩

- 确保通过单元测试。

        python -m unittest discover
- Python 代码需符合 PEP 8 编程规范，检查工具使用 flake8。

