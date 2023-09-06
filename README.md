# Tasks



> **我们要写一个驱动,并改装(Hook)CE,使CE和驱动通信,能够读、写受反作弊保护的游戏。**
>
> 并且这个驱动可以**兼容任何Windows 64位操作系统**,**不会轻易蓝屏**,不会**触发PatchGuard**

---

# How and what we should do



为了完成上述任务

我们应该有

- 一个稳定驱动

- 一个CE
- 一个Dll或者是其他,用于注入CE,hook R3层函数,通过**DeviceIoControl**或者说其他通信方式,与驱动通信,完成读写操作。

---

# This video

我这个视频将代领大家从0[^1]开始,写一个驱动,这个驱动不依赖任何OS版本,不依靠任何特征码搜索等不稳定的因素查找函数。**均使用ntosknrl.exe已导出的函数进行**。



# will learn

- [x] 什么是句柄以及Windows句柄校验机制
- [x] 驱动层是如何进行句柄回调保护的
- [x] Windows内核导出函数的使用

- [x] Detours库的使用 R3 Hook
- [x] 简单驱动与简单
- [x] 劫持dll补丁的编写 AheadList

version


预计3-5课左右。

---

[^1]: 非0基础,要有简单的反汇编,基础的C++/C语言知识,对于驱动编写,我会简单地点几下,但是会写驱动更好
