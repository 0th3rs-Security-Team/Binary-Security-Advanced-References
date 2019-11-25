# Binary-Security-Advanced-References

本仓库内容旨在收集二进制安全相关的精品阅读材料，供学习者深入参考学习所用

## 资源介绍

### ctf-all-in-one
`《CTF All in One》`是一本媲美CTF-Wiki的，对CTF所有领域有着百科全书一样介绍的开源书籍，除此之外，本书还介绍了大量领域内的优秀学术论文，对寻找研究方向、拓宽研究思路也大有益处。只是内容还不完整，有些主题还留有空白，作者会不定期更新。原出处及最新更新请参考[Github仓库](https://github.com/firmianay/CTF-All-In-One)

### SymbolicExecution
符号执行是一项重要的软件分析与测试技术，在软件测试领域有非常重要的用途。而在CTF中，符号执行技术又是一个解题利器。这份PPT是一份符号执行快速入门教程，内容比较基础，但是也非常容易懂

### SAT_SMT_by_example
符号执行背后的理论支撑是`SAT/SMT`数学理论，若要彻底理解符号执行，就需要对该数学理论有一个全面的认识。`《SAT/SMT by Example》
`这本网络书籍由`Dennis Yurichev`编写，作者在其主页会不定期更新，原出处及最新更新请参考[这里](https://yurichev.com/writings/SAT_SMT_by_example.pdf)

### pin官方教程
代码插桩是符号执行以外另一个软件分析与测试技术，常用来确定程序执行状态，以及进行一些统计分析，Intel开发的Pin Tool是一个重要的代码插桩工具，而这份资料是它的官方教程

### OLLVM快速学习
[Obfuscator-LLVM](https://github.com/obfuscator-llvm/obfuscator)是一个在LLVM编译器上二次开发的代码混淆器，OLLVM提供了三种代码混淆：控制流平坦化、指令替换、虚假控制流，这篇文章是对OLLVM的简单介绍。关于OLLVM网上资料也很多，以后有机会我还会补充一些相关文章

### domas_2015_the_movfuscator
除OLLVM以外，另一种有名的代码混淆工具叫[movfuscator](https://github.com/Battelle/movfuscator)，作者为domas。`movfuscator`可以将所有的汇编指令都用`mov`指令等效替换。作者在Derbycon 2015上对它的设计思想做了全面的介绍，演讲视频请见[此处](https://www.youtube.com/watch?v=R7EEoWg6Ekk)（要翻墙）。这份资料就是它演讲的幻灯片

### mov_is_Turing-complete
`movfuscator`的理论支撑在于，`mov`指令是图灵完备的，而这篇论文是对这个结论的证明

### Machine_Code_Obfuscation_via_Instruction_Set_Reduction_and_Control_Flow_Graph_Linearization_Analysis_and_Countermeasures
这份资料是德国慕尼黑工业大学一名本科生于2016年完成的本科毕业论文，这篇论文提出了一个反制movfuscator混淆的方法，可以去除movfuscator混淆。作者依据其方法，还真正实现了该反混淆工具，具体可以查看他的[Github仓库](https://github.com/kirschju/demovfuscator)

### glibc内存管理ptmalloc源代码分析
学习glibc堆漏洞利用的前提是熟练掌握glibc堆管理机制，这本书以glibc 2.23版本为例，分析了glibc堆管理机制`ptmalloc2`的内存管理思想和策略，还详解了内存管理策略对应的开源代码，是学习堆管理机制和堆漏洞利用的必读书籍，其中3.2节又是重中之重

### Understand the heap by breaking it
另一篇glibc堆管理机制介绍资料，但这本资料是从堆漏洞利用的角度去学堆管理机制的

### 堆漏洞的利用技巧
这是北京大学Atum同学讲座的幻灯片，这份资料是站在CTF竞赛的角度对CTF中的堆漏洞利用进行的总结，内容较全面但不详细，特点是每个堆漏洞技巧的后面附上了练习题，可以在阅读的同时边学边练。另外，Atum同学的[Github仓库](https://github.com/A7um/slides)上有很多高质量的资源，大家也可以多多参考

### Linux Heap Internals
上海交通大学0ops战队的内部训练资料，这份资料与Atum的`堆漏洞的利用技巧`相比少了很多CTF的应试成分，更多的是从一个研究者的角度来介绍各种常见的和不常见的堆漏洞利用

### 堆管理机制
一张描述堆管理机制的高清大图，有利于理清逻辑

### 逆向工程核心知识体系
我个人编写的逆向工程核心知识体系，并对不同知识的难度进行了评级。这份知识体系有利于新手把握学习方向，知道要去学什么。当然，这份知识体系只是根据我个人的理解编写的，可能存在谬误和不完整的地方，欢迎大家提交Pull Request进行补充