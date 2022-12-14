# 阶段二 周报
经过一个月的第一阶段学习，进一步学习了Rust语言，深入学习了计算机操作系统。因为本身在这两方面基础就很薄弱，加上不是学生，没有足够多的精力投入，整个过程比较艰难，很多知识点并没有完全掌握，欠下的技术债较多。但无论如何，收获是巨大的，还是很满意的，欠下的东西通过后面的学习要一一补上。

## Weekly 1 (8.1 ~ 8.7)
### 内容
#### 1. 熟悉阶段二
进入第二阶段，我的选题是关于rFreeRTOS的，可以说和第一阶段的rCore关联不大，这一点比较可惜，但和个人的工作息息相关，第一次看到这个项目就萌生了极大兴趣。经过取舍、考虑，最终选定这个课题，目标是将该项目移植到手头的 赤菟 CH32V307 开发板。

从上周六到这周五，每天都天课题报告，主要是关于 zCore 的，认真听了，收获没那么大。

#### 2. 跑通最简工程
参照 STM32 的工程，完成了 CH32V307 的最简 Rust 工程，包括工程编译、固件下载、调试。详细内容在[工具链及基础工程](rust-based-os-comp2022-Phase2-toolchain.md)中。

### 计划
下周尽快实现：
1. 点灯
2. 尽快实现栈的切换

## Weekly 2 (8.8 ~ 8.14)
### 内容
#### 1. 完成点灯实验
在上周的基础上，成功完成了点灯实验。

#### 2. 嵌入式编程交流
因缺少 Rust 嵌入式开发经验，在串口驱动上遇到了问题。根据 Rust 嵌入式团队的约定，不管是PAC库还是HAL库，都只会也只能有一个完整外设的实例，如果严格遵循约定，需要在软件整个周期内小心维护这个实例，这给编成带来了较大困难，就此问题在本周交流会上进行了讨论，得到米明恒同学、杨德睿工程师的经验分享和向老师建议。

几个相关链接：
* [Tracking Issue for RFC 3128: I/O Safety](https://github.com/rust-lang/rust/issues/87074)
* [RFC 导读 | 构建安全的 I/O](https://cloud.tencent.com/developer/article/1899748)
* [3128-io-safety.md](https://github.com/rust-lang/rfcs/blob/master/text/3128-io-safety.md)

需要在以后认真学习。

#### 3. 更换开发板
这款芯片是国产芯片，南京沁恒在MCU领域也不是主流厂家，所以不管是官方还是社区，资料相对较少，在开发是遇到问题个人无法解决。

板载仿真器是原厂方案，不通用，编译器和仿真器驱动OpenOCD，也是在开源方案上的魔改版本，且为闭源，二进制文件是从官方IDE里的提取版本，独立使用问题不稳定，影响开发。为了能够集中精力于Rust和操作系统的学习，在老师的建议下更换开发板，先复现原作者的工作内容，提升自己能力后在回过头在研究这块板子。

### 计划
下周尽快实现：
1. 熟悉开发板
2. 尽快跟上原作者进度

## Weekly 3 (8.15 ~ 8.22)
### 内容
#### 1. 熟悉 Nezha 开发板
成功编译工程，能够完成 Qemu 的启动、运行、调试。

[基于 Qemu 环境搭建](rust-based-os-comp2022-Phase2-qemu-env.md)

#### 2. 硬件开发环境搭建
成功编译对应开发板的工程，完成固件的下载，但在调试上遇到一些问题。在交流会上进行讨论后，得到杨德睿工程师的建议。跟原作者沟通后，得知当时他们没有并没有使用仿真器进行调试，使用的是串口输出的方式。

[Nezha 开发板环境搭建](rust-based-os-comp2022-Phase2-nezha-env.md)

### 计划
下周尽快实现：
1. 跑通测例
2. 并能完成测例



## Weekly 4 (8.23 ~ 8.28)
### 内容
#### 1. 编译测例
在编译测例时遇到问题，尝试修改

### 计划
下周尽快实现：
1. 跑通测例
2. 并能完成测例

## Weekly 5 (8.29 ~ 9.04)
#### 1. 编译测例
仍然卡在编译测例这一步，整理了未完成的测例函数。个人觉得应该是有哪里操作错误了，尝试与原作者沟通。

### 计划
下周第二阶段就要结束了，这个月完成的内容太少了，完全没有达到预期，但仍要有个总结，有始有终。

下一周不会赶进度，停下脚步，回过头来整理已经学到的。




