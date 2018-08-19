# Anki 划词助手 - 用户手册

距离开始开发“Anki 划词助手”已经过去接近一年半了，可是到现在还没有一篇像样的教程之类的东西，今天下了一个大大的决心，准备写一篇出来。

## 这东西是干嘛的啊？

这东西是个安卓 App，是用来配合另一个安卓 App “Ankidroid” 一起使用的。这个叫 Ankidroid 的应用是记忆卡片软件 Anki 的安卓版。Anki 这个软件呢简单来说就是电子化的记忆卡片，类似于
有的四六级词汇书送的那种正面是单词背面是释义的纸质卡片。Anki 这类电子化的记忆卡片相比于纸质卡片的一大优势就是有比较科学的复习算法，像 Anki 里用的复习算法就是基于间隔重复（Spaced Repetition)原理的
SM2 算法。这类算法如果追究细节那么解释起来是比较麻烦的，其实我也不懂。简单来说它就是根据你对某张卡片内容熟悉程度的选择，来安排同一张卡片下一次出现的时间，并且这次和下次的时间间隔会随着你对内容掌握程度的加深变得越来越长，这也就是间隔重复这个名词的由来。比方说我今天往 Anki 里加了一张卡片，正面是“cat”，背面是“猫”。我在复习卡片的时候就可能碰到了这张卡片的正面“cat”，那么此时我就要回忆背面是啥，如果我回忆出来了，我就选“good”这个记忆程度选项，于是这张卡片可能今天就不会再出现了，而是等到我明天复习卡片的时候再出现。第二天我再次碰到 cat 这张卡片的时候，我还是能记起来是啥意思的话，可能这张卡片就是在4天后才出现。等到我 4 天后又回忆出来的话，这个时间间隔可能一下子就变成了 7 天。这个时间间隔会一直增长下去，
直到软件里设定的最长时间间隔（有可能是100年哦）。假如中间哪次没回忆出来 cat 的意思，那么就一夜回到解放前了，时间间隔可能从 1 天开始重新往上涨。

当然这只是对 Anki 的一个很粗糙的介绍，具体的 Anki 教程可以看看知乎上余时行老师的 [Anki 专栏](https://zhuanlan.zhihu.com/-anki)，特别是这篇[终极汇总](https://zhuanlan.zhihu.com/p/21328602)。

有很大一部分人用 Anki 是为了学习语言的，用来学习语言的时候一个很常见的需求就是把阅读文章或者书籍时遇到的生词记录到 Anki 里做成卡片。在电脑上制作这种卡片其实还是比较方便的，把单词复制到卡片正面，然后从词典软件把需要的解释复制到背面即可。同时，在电脑端也有不少简化此类制卡操作的插件，比如 [WordQuery](https://github.com/finalion/WordQuery) 和老黄的 Chrome 插件[在线词典助手](https://github.com/ninja33/ODH)。

但是在安卓手机上情况就变得麻烦多了。假如你在外国新闻网站上读新闻看到一个不认识的单词想把它制作成卡片，由于手机操作的局限性那将是非常痛苦的体验，需要在各种不同的 App 间来回切换，复制过来复制过去，等到做好一张卡，可能刚才新闻读到哪都忘了。所以我在去年开发了“Anki 划词助手”这个应用，用来简化这类痛苦的操作。

## 怎么用啊？

### 如果你是 Anki 新手

如果你以前没用过 Anki，看了上面的介绍，也想试一试在阅读时记录生词并复习这种语言学习方法的话，可以接着往下看。

首先，你需要在安卓手机上装上 Ankidroid（什么？！你没有安卓手机...那你还看到这里了？）。如果在手机自带的应用商店没搜索到的话，可以到酷安网下载（[下载地址](https://www.coolapk.com/apk/com.ichi2.anki)。

打开了 Ankidroid 如果觉得一脸懵逼的话没关系，如果仅仅是为了用划词助手也不需要知道那么多。

接下来需要安装划词助手，同样也是到酷安网下载（[下载地址](https://www.coolapk.com/apk/com.mmjang.ankihelper)。如果你想持续收到更新的话，建议装个酷安的客户端。划词助手不在其他地方上架是因为 1. 上架 google play 需要双币信用卡而我没有 2. 上架华为应用市场这种国内大牌市场需要营业执照之类的东西而我一个个体户也没有 3. 小米商店我好像也申请了，还上传了手持身份证的照片，但是最后也没成功。

![权限授予界面](pics/hello.png)

这时候不要犹豫，一定要选择同意啊。不同意没法用。不同意没法用。不同意没法用。如果手贱点了拒绝，自己到权限管理里改过来。

同意之后，会接着问题是否需要使用默认方案，如果你是第一次使用 Anki，而且你是用来学英语的话，我建议选择确定，对于新手会省去很多配置过程。

![默认方案](pics/model.png)

此时，基本的准备工作其实已经完成了。这时候界面上的几个选项其实只用关注“剪切板查词”这个，我建议把它打开。

![剪切板查词](pics/copy.png)

#### 剪切板划词

现在开始第一次划词，用的是复制句子的方法。划词助手还支持其他多种划词方法，但是复制法是通用型最好的，所以先介绍这个。打开一个能复制英语句子的应用，可以是某个阅读器， 或者某个浏览器（关于浏览器我推荐 chrome，因为它可以在划词助手不在后台的时候调用划词助手。这里特别注意微信的自带浏览器和QQ浏览器可能是用不了复制划词的，所以尽量避免吧）。这里用 chrome 打开 chinadaily 举例子。

假如这篇新闻的第一段话里我不认识 comprehensively 这个单词，可以先把包含有这个单词的句子复制下来。

![复制句子](pics/chrome_copy.png)

这是如果不出意外，就会有一个弹窗从地下冒出来，没错这个就是划词助手的界面了。如果没有弹窗，要检查划词助手是不是被杀了后台，或者主界面剪切板查词的选择没打开。

划词主界面上会看到刚才复制的句子，这里的句子其实每个单词都是可以点的。按照哪里不会点哪里的原则，点击 comprehensively，底下就会出现 comprehensively 的解释，每个释义的右边都有一个“+”按钮，这个按钮就是用来把刚才复制的句子、选定的单词、和当前释义一起送到 Ankidroid 制成卡片的了。对于这里的语境，可以知道第一个释义是最合适的，于是可以点击第一个加号按钮。

这时打开 Ankidroid，就可以看到刚才创建的划词助手默认牌组了，打开这个牌组，就可以看到刚才创建的卡片。正面是单词、音标、发音和句子。背面会多一个解释。要做的就是根据当前句子的语境回忆单词的意思。

正面：

![卡片正面](pics/card_front.png)

背面：

![卡片背面](pics/card_back.png)

#### 几个常见问题

**为什么要复制句子而不是直接复制单词？** 

单词出现的语境是非常重要的，如果仅仅是保存单词而忽略当时在文章里的用法，那还不如直接去背单词书。当然，如果你还是更喜欢直接复制单词，划词助手也是支持这种用法的。

**为什么每次只能保存一个释义而不是所有释义**

Anki 倡导记忆材料最小化原则，所以划词助手目前只能保存某个单词对应于语境的一项释义，这样可以保持卡片上需要记忆的内容尽量短小。以后可能会有同时添加多项释义的功能出现（坑）。

**为什么我点击加号的时候划词助手闪退了？**

保存卡片的时候划词助手需要调用 Ankidroid 的接口，部分手机会对应用间相互调用有较多的限制，所以导致调用不成功。可能的解决方法是：

1. 划词前打开 Ankidroid，并保持在后台（也许需要添加到后台清理白名单）
2. 对于某些应用，可能需要在权限管理之类的地方打开 Ankidroid 的自启动权限。

#### Chrome 弹出菜单划词

对于 Chrome 浏览器，除了用复制的方法划词，也可以在长按句子后弹出的菜单选择那个三个点的按钮，并选择“Anki 划词助手”选项唤出划词助手弹窗。这种方法的好处是不需要划词助手处于后台状态也能调用。

![Chrome 菜单](pics/chrome_dot.png)

![Chrome 调用划词助手](pics/chrome_context.png)

#### FBReader 划词

以上的划词方法虽然大大简化了制卡的步骤，但是仍然需要经过复制句子，选择单词这几个步骤。

如果你平时会看一些英文的电子书，如 epub、mobi、txt 等格式，推荐使用与划词助手配套的 FBReader 来划词。

FBReader 是一个开源的阅读器，支持常见的电子书格式。我通过钻研其源码，实现了这个阅读器与划词助手的联动，可以直接长按单词并调用划词助手，而且能自动识别当前单词所在的句子，不再需要人工复制句子了。

我修改的划词版 FBReader 可以在[这里](https://share.weiyun.com/5ot2Lz4)下载。

这里需要注意，第一次打开看到的会是个黄色的空白界面。不要惊慌，软件没有装错。点击屏幕底部就可以看到主菜单了。

在主菜单选择“本地书柜”就可以打开本地的电子书。阅读时，长按某个生词，在弹出的菜单里会有一个星星一样的图标，选中这个就可以调用划词助手了。