# <p align="center"> PokemonGo </p>

<p align="center"> Jetpack 实战项目 PokemonGo（神奇宝贝）基于 MVVM 架构和 Repository 设计模式 </p>

<p align="center">
这是一个小型的 App 项目，涉及到技术：Paging3（network + db），Dagger-Hilt，App Startup，DataBinding，Room，Motionlayout，Kotlin Flow，Coil，JProgressView 等等。
</p>

<p align="center">
<a href="https://github.com/hi-dhl"><img src="https://img.shields.io/badge/GitHub-HiDhl-4BC51D.svg?style=flat"></a> <a href="https://opensource.org/licenses/Apache-2.0"><img src="https://img.shields.io/badge/license-Apache2.0-blue.svg?style=flat"></a> <img src="https://img.shields.io/badge/language-kotlin-orange.svg"/> <img src="https://img.shields.io/badge/platform-android-lightgrey.svg"/>
</p>

<p align="center">
<img src="http://cdn.51git.cn/2020-07-14-Pokemon.png"/> 
</p>

<p align="center"> PokemonGo 动态效果图如下所示，如果动图无法查看，请点击这里查看 <a href="http://cdn.51git.cn/2020-07-14-15946978385391.gif"> 动态效果图</a> | <a href="http://cdn.51git.cn/2020-07-14-Pokemon.png"> 静态图</a></p>

<p align="center">
<img src="http://cdn.51git.cn/2020-07-12-15945313937044.gif" height = 500/> 
</p>

关于 PokemonGo 项目分析的文章请查看 [神奇宝贝 眼前一亮的 Jetpack + MVVM 极简实战](https://juejin.im/post/5f0d303e6fb9a07e76550d4c)

### 项目 PokemonGo 涉及到的技术

* [Gradle Versions Plugin](https://github.com/ben-manes/gradle-versions-plugin)：检查依赖库是否存在最新版本
* Minimum SDK >= 26
* [Kotlin](https://kotlinlang.org/) + [Coroutines](https://github.com/Kotlin/kotlinx.coroutines) + [Flow](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/)：flow 是对 Kotlin 协程的扩展，让我们可以像运行同步代码一样运行异步代码
* JetPack
    * Paging3（network + db）：用到了 Paging3 中的  `MediatorResult` 用来实现 network + db
    * Dagger-Hilt (2.28-alpha)：依赖注入框架
    * App Startup：设置组件初始化顺序
    * DataBinding：以声明方式将可观察数据绑定到界面上
    * Room：在 SQLite 上提供了一个抽象层，流畅地访问 SQLite 数据库
    * LiveData：在底层数据库更改时通知视图
    * ViewModel：以注重生命周期的方式管理界面相关的数据
    * Andriod KTX：编写更简洁、惯用的 Kotlin 代码
* 项目架构
    * MVVM 架构（View - DataBinding - ViewModel - Model）
    * Repository 设计模式
    * Data Mapper 数据映射
* [Material-Components](https://github.com/material-components/material-components-android)
* [Motionlayout](https://developer.android.com/training/constraint-layout/motionlayout) ：MotionLayout 是一种布局类型，可帮助您管理应用中的动画
* [Retrofit2 & OkHttp3](https://github.com/square/retrofit)：用于请求网路数据
* [Coil](https://github.com/coil-kt/coil/)：基于 Kotlin 开发的首个图片加载库
* [Timber](https://github.com/JakeWharton/timber): 日志打印
* [JDataBinding](https://github.com/hi-dhl/JDataBinding)：基于 DataBinding 封装的基础组件库
* [JProgressView](https://github.com/hi-dhl/JProgressView) ：一个小巧灵活可定制的进度条，支持图形：圆形、圆角矩形、矩形等等

**以上技术栈对应之前写的技术文章：**

* [Jetpack 最新成员 AndroidX App Startup 实践以及原理分析](https://juejin.im/post/5ee4bbe4f265da76b559bdfe)
* [Jetpack 成员 Paging3 实践以及源码分析（一）](https://juejin.im/post/5ee998e8e51d4573d65df02b)
* [Jetpack 新成员 Paging3 网络实践及原理分析（二）](https://juejin.im/post/5eeefbf4e51d45742c53ddce)
* [Jetpack 新成员 Hilt 实践（一）启程过坑记](https://juejin.im/post/5ef2f31951882565a94e06a5?utm_source=gold_browser_extension) 
* [Jetpack 新成员 Hilt 实践之 App Startup（二）进阶篇](https://juejin.im/post/5ef7638c5188252e6a532db3)
* [Jetpack 新成员 Hilt 与 Dagger 大不同（三）落地篇](https://juejin.im/post/5efca0c1e51d4534a40d972f)
* [全方面分析 Hilt 和 Koin 性能](https://juejin.im/post/5f02114d5188252e8a081afb)
* [[译][2.4K Star] 放弃 Dagger 拥抱 Koin](https://juejin.im/post/5ebc1eb8e51d454dcf45744e)
* [项目中封装 Kotlin + Android Databinding](https://juejin.im/post/5e9c434a51882573663f6cc6)
* [为数不多的人知道的 Kotlin 技巧以及 原理解析(一)](https://juejin.im/post/5edfd7c9e51d45789a7f206d)
* [为数不多的人知道的 Kotlin 技巧以及 原理解析(二)](https://juejin.im/post/5f0747486fb9a07ea86dc881)


## 如何检查依赖库的版本更新

在项目的根目录下执行以下命令。

```
./gradlew dependencyUpdates
```
    
会在当前目录下生成 build/dependencyUpdates/report.txt 文件，内容如下所示：

```
The following dependencies have later release versions:
 - androidx.swiperefreshlayout:swiperefreshlayout [1.0.0 -> 1.1.0]
     https://developer.android.com/jetpack/androidx
 - com.squareup.okhttp3:logging-interceptor [3.9.0 -> 4.7.2]
     https://square.github.io/okhttp/
 - junit:junit [4.12 -> 4.13]
     http://junit.org
 - org.koin:koin-android [2.1.5 -> 2.1.6]
 - org.koin:koin-androidx-viewmodel [2.1.5 -> 2.1.6]
 - org.koin:koin-core [2.1.5 -> 2.1.6]

Gradle release-candidate updates:
 - Gradle: [6.1.1 -> 6.5.1]
```

会列出所有需要更新的依赖库的最新版本，并且 Gradle Versions Plugin 比 AndroidStudio 所支持的更加全面：

* 支持手动方式管理依赖库最新版本检查
* 支持 ext 的方式管理依赖库最新版本检查
* 支持 buildSrc 方式管理依赖库最新版本检查
* 支持 gradle-wrapper 最新版本检查
* 支持多模块的依赖库最新版本检查
    
## MVVM 架构

PokemonGo 基于  MVVM 架构和 Repository 设计模式，如今几乎所有的 Android 开发者至少都听过 MVVM 架构，在谷歌 Android 团队宣布了 Jetpack 的视图模型之后，它已经成为了现代 Android 开发模式最流行的架构之一。

<p align="center">
<img src="http://cdn.51git.cn/2020-07-12-159453363449491.jpg"/> 
</p>

Jetpack 的视图模型的 MVVM 架构由 View + DataBinding + ViewModel + Model 组成。**如果这个仓库对你有帮助，请仓库右上角帮我 star 一下，非常感谢。**

## 结语


致力于分享一系列 Android 系统源码、逆向分析、算法、翻译、Jetpack 源码相关的文章，关注我来一起学习，在技术的道路上一起前进，另外我还在维护其他项目 [Android10-Source-Analysis](https://github.com/hi-dhl/Android10-Source-Analysis)、[Leetcode-Solutions-with-Java-And-Kotlin](https://github.com/hi-dhl/Leetcode-Solutions-with-Java-And-Kotlin) 、[Technical-Article-Translation](https://github.com/hi-dhl/Technical-Article-Translation) 、 [AndroidX-Jetpack-Practice](https://github.com/hi-dhl/AndroidX-Jetpack-Practice) 可以前去查看。

### AndroidX-Jetpack-Practice

正在建立一个最全、最新的 AndroidX Jetpack 相关组件的实战项目 以及 相关组件原理分析文章，目前已经包含了 App Startup、Paging3、Hilt 等等，正在逐渐增加其他 Jetpack 新成员，仓库持续更新，可以前去查看：[AndroidX-Jetpack-Practice](https://github.com/hi-dhl/AndroidX-Jetpack-Practice)。

### Android10-Source-Analysis

正在写一系列的 Android 10 源码分析的文章，了解系统源码，不仅有助于分析问题，在面试过程中，对我们也是非常有帮助的，如果你同我一样喜欢研究 Android 源码，可以关注我 GitHub 上的 [Android10-Source-Analysis](https://github.com/hi-dhl/Android10-Source-Analysis)。

### Leetcode-Solutions-with-Java-And-Kotlin

由于 LeetCode 的题库庞大，每个分类都能筛选出数百道题，由于每个人的精力有限，不可能刷完所有题目，因此我按照经典类型题目去分类、和题目的难易程度去排序。

* 数据结构： 数组、栈、队列、字符串、链表、树……
* 算法： 查找算法、搜索算法、位运算、排序、数学、……

每道题目都会用 Java 和 kotlin 去实现，并且每道题目都有解题思路，如果你同我一样喜欢算法、LeetCode，可以关注我 GitHub 上的 LeetCode 题解：[Leetcode-Solutions-with-Java-And-Kotlin](https://github.com/hi-dhl/Leetcode-Solutions-with-Java-And-Kotlin)。

### Technical-Article-Translation

目前正在整理和翻译一系列精选国外的技术文章，不仅仅是翻译，很多优秀的英文技术文章提供了很好思路和方法，每篇文章都会有**译者思考**部分，对原文的更加深入的解读，可以关注我 GitHub 上的 [Technical-Article-Translation](https://github.com/hi-dhl/Technical-Article-Translation)。

## License

```
Copyright 2020 hi-dhl (Jack Deng)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```


