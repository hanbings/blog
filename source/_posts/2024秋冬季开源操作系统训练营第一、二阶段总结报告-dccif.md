---
title: 2024秋冬季开源操作系统训练营第一、二阶段总结报告-dccif
date: 2024-11-08 19:58:17
tags:
  - author:dccif
  - rust
---

# 第一阶段的Rustlings

关于第一阶段的Rustlings，还是花了很多时间去学习Rust。一开始是直接去看《Rust程序设计语言》，随后还看了《Rust圣经》，把一些较为简单的概念和程序过了一遍。可是发现做题时还是难以掌握，随后只能带着疑问和不懂的地方边做边查，做完一套后终于有点入门的感觉了，我感觉rust对我或者别的语言的用户来说，一大难点就是自造的概念太多了+ 第一次接触时的api暴露太多了，有一点不知如何下手。然后再结合上生命周期，就更难上手了。

# rcore实验

## Lab 1
这个实验主要是实现一个简单sys_task_info多任务系统. 通过这个实验, 了硬件是如何在不同的特权级之间切换的, 以及操作系统是如何管理这些特权级的，知道什么是系统调用和特权级的应用

## Lab 2
lab2是实现在启用虚拟地址的情况下重写sys_get_time和sys_task_info, 并实现sys_mmap和sys_munmpa系统调用, 因为启用了分页机制, 学习到了地址空间的概念, 应用程序只需要关心自己的地址空间, 而不需要关心其他应用程序的地址空间, 在实现过程中我对操作系统对代码中的地址空间, 页表的地址转换有了更深的理解  

## Lab 3
lab3是实现sys_spawn和stride调度算法, 学习到了进程是如何创建的, 以及进程是如何执行的

## Lab 4
lab4是实现硬链接和获取文件信息的系统调用,  需要对inode和disk_inode有较深的理解, 学习了文件系统是如何与物理存储设备交互的

## Lab 5
lab5是实现死锁检测, 需要理解死锁检测算法 need矩阵