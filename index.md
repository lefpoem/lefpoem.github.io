# DPDK简介

DPDK（Data Plane Development Kit）数据平面开发工具包，是一个开源软件项目。DPDK通过维护一系列能够加速多核CPU数据包处理的库，提供数据处理框架。DPDK通过绕过内核进行数据处理，表现出了比内核中断处理更高的效率。

## DPDK项目架构

- EAL

  EAL（Environment Abstraction Layer），EAL层负责访问低级资源包括硬件和内存空间。EAL屏蔽了内核具体细节，提供一个通用的接口访问库和操作系统。

- Memory Management

  内存管理包括巨页支持、内存池、缓冲区管理。

- Poll Mode Drivers

  MEMPOOL作为内存池存放MBUFF包。

- RING

  RING库管理线程、核心以及其它并行实体之间传送的无日队列/消息。

- TIMER

  TIMER提供异步回调函数包括添加、删除或重启定时器。
