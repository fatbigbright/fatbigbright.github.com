---
layout: post
title: iOS用户界面指南
permalink: ios-human-interface-guidelines
description: iOS应用界面设计指南
date: 2013-03-15 09:42:58 +08:00
tags: "iOS dev UI"
---

##iOS用户界面指南（中文翻译）

####译者言  

这篇文章译自苹果官方的开发文档：[iOS Human Interface Guidelines](https://developer.apple.com/library/ios/#documentation/UserExperience/Conceptual/MobileHIG/Introduction/Introduction.html)，一切图片资源及内容的版权全归苹果公司所有。翻译这篇文档的目的只是为了个人加深理解和技术交流，无任何商业目的。同时翻译这篇文档也为了督促自己改正做事半途而废的习惯（不过也不排除翻译半途而废啦~）。

另外，个人英语水平实在有限，也希望看到这篇文章的朋友能够花出宝贵的时间给文中错误或不当的翻译予以指摘，请随意喷。

######2013-05-15 更新
刚刚发现苹果的开发者官网上已经提供了这篇文章的一个[简化翻译版](http://developer.apple.com/library/ios/#referencelibrary/GettingStarted/RoadMapiOSCh/chapters/RM_iHIG_Station/Fundamentals/Fundamentals.html)。可喜的是我对某些名字的译名和官方的译名还算接近。不管人家官方的了，自己翻自己的，本来这也是自娱的一次翻译训练。

##简介

*iOS用户界面指南*提供了详细的指南与设计原则，旨在帮助你为你的iOS应用设计出优秀的交互界面和良好的使用体验。
![iPhoneLineUp]({{ BASE_PATH }}/assets/images/iPhoneLineUp.jpg)

*iOS用户界面指南*并不描述如何实现界面设计。当你准备好了进行编码时，请阅读*[iOS应用编程指南](https://developer.apple.com/library/ios/#documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)*。

###概览

了解并熟悉平台的一些约定俗成的惯例，可以帮助你更好地在创建应用的过程中找到自己的定位。

<h3 id="great_definition">优秀的iOS应用是拥抱平台和界面设计原则的</h3>

用户总是青睐那些用起来就像是为了设备专门量身打造的应用。比如，当一款应用能够良好地适配设备的显示屏并且能够自然地对用户已知的一些手势作出反应，它就提供了用户需要的大部分体验了。并且，虽然用户意识不到界面设计的诸如操作的直观性或连续性等原则，他们仍然能够分辨应用程序什么时候遵循着这些原则，而什么时候没有遵循。当你开始设计一款iOS应用时，你需要理解到底是什么使得基于iOS的设备如此地与众不同，需要学习如何遵循并活用界面设计原则，从而令你的应用能够提供优秀的用户体验。

***
相关章节： [“平台特性”](#platform_characteristics) 及 [“用户界面设计原则”](#human_interface_principles)

***

<h3 id="great_design">优秀的应用设计始于某些明确的定义</h3>

当你拥有一个制作应用的创意时，明确你的应用要有哪些特性，要给哪些用户使用，这两件事是至关重要的。当这两点明确之后，你需要确定如何定制应用的外观和体验，从而使它能够适配所运行的设备和它所能完成的功能。
如果你是要将一个已有的软件移植到iOS平台，你会面对许多同样的挑战。随着你对已有软件的重新设计，你会从其它成功实现跨平台迁移的软件（比如Mail和Keynote）中学习到一些设计原则。

***
相关章节：[“应用设计策略”](#app_design_strategies)及[“迁移案例研究”](#transition_case_studies)

***

###优秀的用户体验来源于你对细节的关注

在设计应用的过程中，不论是任务的运行，或是应用的启动与退出，抑或按钮的使用，你都应将保持良好的用户体验放在最为首要的位置。先概览，然后仔细研读这些会影响你的应用的外观和行为的指南内容吧。

***
相关章节：[“用户体验指南”]()及[“iOS界面元素使用指南”]()

***

###人们期望从应用的使用中发现iOS技术

iOS提供了许多能够为应用增加价值的技术，比如iCloud，多任务，Passbook，还有VoiceOver。虽然用户可能只把这类技术当作他们设备上默认自动可用的技术，但如果你需要让你的应用与它们协作，仍需要做一些工作才可以。如果一款应用要适配某项iOS技术，一定要保证这项技术的引入在设计上遵循了相关的使用指南。

***
相关章节：[“iOS技术使用指南”]()

***

###所有的应用至少都需要一些定制的美术工作

即使你的应用只提供一项严肃、具有生产性的应用任务，并且只使用一些标准的用户界面元素，你至少仍然要提供一个漂亮的定制的图标，可以供用户在App Store和他们的设备桌面上查看。不论你的应用拥有大量的美工定制，还是只有一点点，你都需要知道哪些图标和图片是必须，还要知道应该如何适当地创建它们。并且，当你为Retina屏幕进行美工设计时，你需要借助某些技术简化相关工作。

***
相关章节：[“图标定制和图片创建指南”]()

***

<h2 id="platform_characteristics">平台特性</h2>
[<<返回](#great_definition)

iOS设备分享了几项独特的特性，这些特性影响着该平台上运行的应用的用户体验。最成功的应用无一不积极拥抱这些特性，并提供了与设备紧密整合的用户体验。

###不论设备大小，显示屏最重要

iOS设备的显示屏是用户体验的核心。通过显示屏，用户不但能看到漂亮的文本、图片或媒体，而且可以通过多点触摸来与显示屏进行物理交互，来获得体验（有时甚至不需要看屏幕）。

不同的iOS设备可以显示不同维度和分辨率，不过所有的iOS设备都通过下述相同的方式来影响着用户的体验：

* 44 × 44点是可舒适地点击的界面元素的最小尺寸  
* 用户十分在意应用的美工质量  
* 显示屏鼓励用户忘记设备本身而专注于它的内容或执行的任务。

***
**备注：**当你与人讨论一个设备屏幕的尺寸或是一个图形编辑软件的图标大小，抑或是将要绘制到屏幕的一块区域的尺寸时，**点**是一个恰当的度量单位。

在一个标准分辨率的设备屏幕上，一个点就是一个象素，但对于其它的分辨率，点和象素却是存在与此不同的对应关系。比如，在一个Retina屏上，一个点相当于两个象素。

对于这一概念的完整讨论，请参考[View Programming Guide for iOS](https://developer.apple.com/library/ios/#documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009503)中的[“点与象素”](https://developer.apple.com/library/ios/#documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/WindowsandViews/WindowsandViews.html#//apple_ref/doc/uid/TP40009503-CH2-SW15)部分

***

###可变的设备旋转方向
用户可以在任何时候或因许多原因旋转iOS设备。比如，有时用户在执行某项任务时习惯于纵向摆放设备，这样感觉更为舒服，而有时用户又可能更倾向于横向摆放设备。不论旋转设备的原因为何，用户希望应用程序能够自我适配并可以专注于它的主要功能。

用户经常会通过Home屏幕来启动应用，所以他们期望应用启动后会保持同样的旋转方向。由于iPhone与iPad在Home屏幕上显示有所不同，故此用户的期望也会出现以下不同：

* 在iPhone与iPod touch上，Home屏幕只会纵向显示，Home键在屏幕底端。这一特点引导用户期望iPhone应用在默认情况下也以这个方向启动。
* 在iPad上，Home屏幕可以以任何旋转方向显示，因此用户倾向于期望iPad应用也可以以他们当前所使用的设备方向来启动。

###应用响应手势，而非点击
用户会用手指做出种种的动作，这些动作被称为手势，每一种手势操作iOS设备的唯一的多点触摸接口。比如，用户通过敲打动作来击活一个按钮，用划动或拖拽来使一个长列表滚动，或用双指的捏合来控制图片的放大与缩小。

多点触摸接口为用户和他们的设备之间建立了一种直观的感觉，提高了他们对于屏幕上元素的操作的实感。

标准的手势让用户感到舒适，因为内建的应用一直在使用这些手势。使用内建应用所获得经验，使用户总结出了一套他们期望能在大部分其它应用中同样可以使用的手势的集合。

**表格1-1** 用户用于与iOS设备交互的手势
<table id="tb11">
	<tr>
		<th>手势</th>
		<th>动作</th>
	</tr>
	<tr>
		<td class="gesture">点击(Tap)</td>
		<td class="action">点选屏幕上的元素（类似鼠标的单击）</td>
	</tr>
	<tr>
		<td>拖动(Drag)</td>
		<td>滚动或拖移（就是指从一边移动到另一边）<br/>
			拖动一个屏幕元素
		</td>
	</tr>
	<tr>
		<td>滑动(Flick)</td>
		<td>快速滚动或拖移</td>
	</tr>
	<tr>
		<td>横扫(Swipe)</td>
		<td>单指操作时，用于显示表视图中的删除按钮或iPad中的分隔视图的隐藏部分，或者通知中心(从屏幕顶端下拉显示)<br />
		四指操作时，用于在iPad中进行应用切换。
		</td>
	</tr>
	<tr>
		<td>双击(Double tap)</td>
		<td>放大显示，并令被点击的内容块或图片处于屏幕中心<br />
		当已经放大显示时，则为再次缩小视图。
		</td>
	</tr>
	<tr>
		<td>捏合(Pinch)</td>
		<td>两指向外捏为放大<br />向内捏为缩小</td>
	</tr>
	<tr>
		<td>触摸并按住(Touch and hold)</td>
		<td>操作可编辑或可选择的文本时，光标处会显示一个放大镜</td>
	</tr>
	<tr>
		<td>摇晃(Shake)</td>
		<td>触发回退或恢复操作</td>
	</tr>
</table>

除了这些手势之外，用户还可以通过移动设备本身来完成某些任务，例如在iPhone4S上激活Siri，或校对罗盘。用户期望不论他们在使用什么应用，这些手势都能够有相同的表现。

###用户某一时刻只会与一个应用产生交互
同一时刻只会有一个应用在前台可见。当用户从一个应用切换到另一个应用，前一个应用将进入后台并且它的界面会消失。这个特性，称为**多任务**，允许应用保留在后台直到用户再次启动它们或关闭它。

大部分应用在进入后台时会处于一个挂起状态。多任务UI会显示挂起的应用，并为用户切换到最近使用的应用提供一种便捷的方式。多任务UI会在屏幕底端、现在正在运行的应用或桌面屏幕下方显示。(如图中iPhone设置应用所示)

![multitasking_settings.png]({{ BASE_PATH }}/assets/images/multitasking_settings.png)

当用户恢复运一个挂起的应用，它会立即恢复到它进入后台时的那个时点的状态，而不需要重新载入它的UI。

而有些应用即使进入后台，也仍会在用户在前台运行其它应用的同时，保持运行状态。例如，用户可能希望他们正在使用的歌曲播放应用，在他们使用其它应用进行日程任务查询或收发邮件的同时，也能在后台继续播放歌曲。

对于如何正确地和优雅地处理多任务，请查看“[Multitasking](https://developer.apple.com/library/ios/#documentation/UserExperience/Conceptual/MobileHIG/TechnologyUsage/TechnologyUsage.html#//apple_ref/doc/uid/TP40006556-CH18-SW2)”。

***
备注：运行于iOS3.2及更早版本的应用不会进入后台，某些旧的设备即使运行了iOS4及更新的版本系统，也完全不支持多任务或后台执行。在这些情况下，应用在离开前台时会直接结束运行。
***

###在设置选项中可设定偏好
用户在内建的**设置**应用中为某个iOS应用进行偏好设置。当他们想要在**设置**中访问那些偏好选项，他们必须从当前的应用中切换出去。

**设置**应用中的偏好属于“一次设置，极少更改”的类型。虽然某些内建应用也提供了这类的设置选项，但大部分应用都不需要这些，因此它们并不在**设置**应用中设有偏好。

###屏幕上的用户帮助要最小化
移动用户在从一款应用中受益之前，既没有时间，也没有愿望去阅读大篇的帮助内容。而且，帮助内容会占去宝贵的存储和显示资源。

iOS设备和内建应用是直观易用的，所以用户不需要屏幕显示帮助内容来告诉他们如何使用设备或者应用。这条经验引导用户期望所有的iOS应用都能如此简单易用。

###绝大部分iOS应用具有单一窗口
一款iOS应用具有一个单一窗口，除非它支持多于一个的显示设备。一款应用的窗口填充了设备的主屏幕并提供了一个空的平面，这个平面承载了一个或多个用以呈现内容的视图。值得注意的是，iOS应用中的窗口的概念有别于电脑应用程序中的窗口。比如，一个iOS窗口不存在可见组件(可见组件指标题栏、关闭按钮等)，并且不能将其移动到设备显示设备上的另一个位置。

还有一点值得注意的重要事项是，大部分用户都没有意识到iOS应用中的窗口和视图的存在。大多情况下，iOS应用会被用户看作是一系列被导航的屏幕集合。从这一观点来着，一个*屏幕*一般对应了一款应用中唯一的视觉状态或模式。例如，在iPhone中的Contacts应用中，用户将他们的通讯录看作一个屏幕（不论它有多长），而将某一单独联系人的详细信息看作另一个屏幕。

***
**备注**：由于本文档集中于UI和用户体验，“屏幕”这一词会被经常提及以便于被绝大部分用户所理解。除非特别说明，否则本文档并不用“屏幕”这一词代替[UIScreen](https://developer.apple.com/library/ios/#documentation/UIKit/Reference/UIScreen_Class/Reference/UIScreen.html#//apple_ref/occ/cl/UIScreen)对象(UIScreen对象可以用于访问主屏幕以外的其它屏幕)。
***

###运行在iOS平台的两类软件
你可以为iOS设备开发两种软件：

*  iOS应用

*  Web内容

一款**iOS应用**是使用iOS SDK开发的，运行于iOS设备的本地应用程序。iOS应用与iOS设备的内建应用类似，建立在设备之上并能充分发挥iOS环境的特性和优势。用户在设备上安装iOS应用，像使用内建应用一样地使用它们，比如Photos, Calendar和Mail。

用户在使用他们的iOS设备访问网页时，**Web内容**就以网页为宿主，而Web内容又分为三类：

**Web应用**。为一项任务提供了一套集中的方案的一类网页，遵循了某些iOS应用显示指南的内容，从而拥有iOS本地应用类似的行为，这样的网页被称为Web应用。一款Web应用经常隐藏了iOS设备上的Safari浏览器的UI元素，使得它看上去像是一款本地应用。借助于网页剪辑(web clip)特性，一款Web应用也可以为用户在iOS系统桌面上提供一个图标。这样就使用户可以像打开一款iOS本地应用相同的方式来打开一款Web应用。

**优化网页**。设计上专门为iOS上的Safari浏览器特别优化以适应其显示和操作的网页(对于任何依赖于未支持的技术的元素——诸如插件、Flash和Java等——所引起的异常，也要在设计中有所考虑)。另外，设计一个优化网页，要令其以正确的尺寸在设备屏幕上呈现内容，并且经常还要使它能够检测当前iOS设备的显示状态，以适当地调整其显示的内容。

**兼容网页**。设计上能够兼容iOS上的Safari浏览器的显示和操作的网页(对于任何依赖于未支持的技术的元素——诸如插件、Flash和Java等——所引起的异常，也要在设计中有所考虑)。一个兼容网页不倾向于花费额外的步骤来优化它在iOS设备上的视图效果，但仍要保证设备可以成功呈现网页上的内容。

一款iOS应用还可能结合了本地UI元素以及用于显示web内容的web内容呈现区域(典型场景有[UIWebView](https://developer.apple.com/library/ios/#documentation/UIKit/Reference/UIWebView_Class/Reference/Reference.html#//apple_ref/occ/cl/UIWebView)的使用)。这样的一款应用应该在显示和行为上模仿本地应用，而非把用户的注意力吸引到那些依赖网络资源的元素上。

###iOS设备上的Safari浏览器提供了Web界面
iOS上的Safari提供了在iOS设备上浏览web内容的界面。虽然iOS上的Safari在很多方面和电脑上运行的Safari类似，但它们仍然存在不同之处。

最大的不同是，用户不能修改**视口**(显示区域)的大小。在电脑桌面中，用户只需修改浏览器窗口大小即可修改视口大小。但在iOS设备中，除非设备的横纵方向发生改变，否则视口大小不会改变。iOS用户可以通过放大和缩小来改变视口的内容显示尺寸，并对网页进行拖移。iPad用户放大缩小web内容的机会相对于iPhone(如下图所示)用户则更少。

![safari_not_same.png]({{ BASE_PATH }}/assets/images/safari_not_same.png)

**iOS上的Safari支持cookie**。使用cookie可以帮助用户简化与web内容进行的交互操作，比如用户上下文、偏好、自动完成曾经输入过的数据等。

**iOS上的Safari不支持Flash, Java(包括Java applet)，或者web内容中的第三方插件**。而支持HTML5的`<audio>`及`<video>`标签来提供视频音频流，还支持javascript和CSS3的变换、过渡、动画等前端效果。

**iOS上的Safari整合了绝大多数的手势，这些手势作用于显示内容的设备，而非内容本身**。点击——与鼠标单击类似的手势——可以让Safari触发web页面上的一个onclick事件。其余鼠标事件诸如悬停等则不支持。

**iOS上的Safari允许Web应用在全屏模式下运行**。iOS系统桌面上的Web应用的图标可以使Web应用以全屏模式启动，使得它们看上去更像是本地应用。

<h2 id="human_interface_principles">用户界面原则</h2>
[<<返回](#great_definition)

优秀的用户界面，会遵循一定的用户界面设计原则，这些原则是基于用户的思考和工作方式的，而非基于设备的职能。即使是一款优秀的应用，如果它的界面不吸引人，或者复杂难懂，抑或缺乏条理，那它同样会带来糟糕的使用体验。而一款设计精美、符合用户直觉且具吸引人的界面则会更好地发挥应用的功能，并为用户带来积极的情感体验。

###美学上的完整性
美学上的完整性并非衡量一款应用漂亮与否的标准，而是衡量一款应用对其外观和功能的整合程度的标准。比如，一款完成某项生产性任务的应用，一般都会在背景中放置有装饰性的界面元素，并且通过提供标准控件和行为让用户能够容易理解相应的任务。这样的应用为用户提供了一种简洁一致信号，方便用户识别并理解它的设计目的。相反地，如果应用所提供的界面显得古怪而琐碎，用户可能就难以理解这样自相矛盾的信号。

类似地，对于沉浸式的应用，比如游戏，用户期望看到一种漂亮的界面外观，并且能从中获得愉悦和探索的乐趣。虽然用户并不期望在游戏中完成什么严肃的或生产性的任务，但他们仍然希望游戏能提供给他们一种符合经验的行为和表现。

###一致性
界面的一致性可以让用户将使用一款应用所积累的知识和技能延用到对另一款应用的使用中。一款带有一致性的应用并非是对其它应用的盲目抄袭，而是充分地发挥了用户所习惯的标准和范例的优点。

判断一款应用是否遵循了一致性原则，要思考以下问题：

*   这款应用是否与iOS标准相一致。它是否正确使用了系统提供的控件、视图和图标？它是否以一种可靠的方式与设备的特性相结合？
*   这款应用是否与它自己相一致。在文字上是否使用了一致的措辞和风格？同一个图标是否始终只代表一个含义？用户在不同的位置进行相同操作时，他们可否预测操作的结果？自定义控件的外观和行为是否在应用中保持一致？
*   如果必要的话，这款应用是否与它的早期版本相一致？术语和含义是否保持不变？原理概念在本质上是否不变？

###直接操纵
当用户倾直接操纵屏幕上的元素，而非通过控制另一个独立的控件去间接操纵这些元素时，他们就能更加专注于应用完成的任务本身而更容易地理解他们的操作所获得的结果。因为有了多点触摸，iOS用户非常喜欢直接操纵所带来的增强体验。手势的使用使用户和屏幕上的元素之间的关系更加密切，操作的感觉更加舒适，因为用户是在直接操作它们，而非是借助类似鼠标这类作为中介的外部设备。

例如，用户可以用捏合手势代替点击放大按扭来实现对某一区域内容的缩放。在一款游戏中，用户通过手势直接移动并与屏幕上的实体进行交互，比如，游戏中有一连串的锁，用户可以通过旋转钥匙孔打开它们。

在一款iOS应用中，用户可以在以下一些场合中体验直接操纵：

*  旋转或者移动设备来影响屏幕上的元素。
*  使用手势来影响屏幕上的元素。
*  可以观察他们的操作所带来的即时的、可见的结果

###反馈
反馈是对用户行为的一种回应，让用户确认程序处理正在进行。当用户操作屏幕的控件时，他们期望可以立即得到反馈，并且在耗时任务进行时，乐于看到应用程序随时更新它的状态。

内建iOS应用会以某种可以察觉的行为变化来响应用户的每一种操作。例如，列表项会在用户点击它们时产生短暂的高亮。假如一个控件的相应操作的处理时间超过数秒，那当该操作进行的时候，这个控件会显示操作进度，并且在适当的情况下应用会显示相应的说明信息。

精细的动画可以给用户提供明确的反馈，帮助用户理解他们的操作。比如，列表会显示新行添加的动画来帮助用户直观地跟踪变化。

声音也会为用户提供有用的反馈。但声音不应被用作是根本的或是唯一的反馈机制，因为用户可能身处在他们听不到设备发声的环境中，或是他们必须将设备调成静音的环境中。

###隐喻
当一款应用中的虚拟物体和行为隐喻了现实世界的物体与行为时，用户可以很快领会应用的操作方法。软件隐喻中的一个经典例子就是文件夹：现实世界中人使用文件夹存放文件，因此用户可以立即理解在电脑的文件夹中存放文件的概念。

最恰当的隐喻建议一种使用方法或经验，但这种方法经验不会强行局限于它们所对应的现实世界的物体或行为。例如，用户可以同一个文件夹中存放远比现实世界中多得多的文件。

iOS因为支持了丰富的图形图象和手势，所以可以表达广泛的隐喻。用户可以实际地与屏幕上的元素进行交互，就好像在真实世界中操作它们一样。iOS中的隐喻包括：

*  点击音乐回放控件
*  在游戏中拖动、划动或横扫物体
*  打开或关闭开关
*  在相册中划动翻页
*  旋转选取器进行选择

一般而言，隐喻不宜过度延伸发散。比如，如果软件中的文件夹必须整理到一个虚拟的书架上，那么这种无用的设计将降低文件夹这个隐喻的可用性。

###用户控制
用户——并非应用——是自主进行操作的。虽然一款应用可以建议用户遵循某种操作过程或者在危险的操作结果发生之前提供警告，但越俎代庖替用户做决定终究是错误的。优秀的应用应该在将实用的功能提供给用户和帮助用户避免危险的结果之间寻求平衡。

当应用和控件的行为是熟悉和可控的时候，用户就可以感到对应用更多的掌控。并且，操作越简单直观，用户越能容易地理解并记住它们。

用户期望在一项操作开始之前可以有足够的机会来取消它，并且期望在一项存在潜在破坏性的操作进行之前有机会确认执行这项操作。最后，用户期望能够优雅地停止一项正在后台运行的操作。

<h2 id="app_design_strategies">应用设计策略</h2>
[<<返回](#great_design)

所有优秀的应用都始于一个优秀的创意，但这并不意味着将创意化为一款成功的iOS应用的道路是一帆风顺的。本章节描述了一些策略，你可以用它们来提取你的创意，复查你的设计要素，并将它们整合到一款用户喜闻乐见的应用中来。

###创建应用的定义描述

一款应用的定义描述简明而实质性地声明一款应用的主要设计目的和它的目标受众。

在开发早期先制定应用的定义描述，可以帮助你将你的产品切实地与用户所需要的产品特性紧密结合起来。在整个开发过程中，使用定义描述可以决定产品的某个特性或行为是否合理。下述步骤可以帮助你建立牢固可靠的应用定义描述。

####1.列出用户可能需要的所有的产品特性

随念所至，尽管开动你的脑筋吧。在这个步骤中，你要试着尽可能将所有和你的产品创意有关的点子都列出来。不要担心列表过长，你会在后续步骤中逐渐精减它们的。

例如，想像你要开发一款应用来帮助用户购买副食。当你考虑到这项活动时，你可能会列出诸如下表中所述的这些用户可能感兴趣的相关任务（潜在特性）：

*  列出清单
*  获得收据
*  比较价格
*  定位店铺
*  在收据上编辑注释
*  获得并使用优惠券
*  查看菜谱
*  检索菜谱
*  查找可替换的食材