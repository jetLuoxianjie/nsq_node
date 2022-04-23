---
title: nsq从入门到精通（🐕狗头保命）
renderNumberedHeading: true
grammar_cjkRuby: true
---


> 为什么写这个资料？
> 目前在国内有关nsq的资料还是比较少，目前在学习并使用，并写下对nsq的理解和介绍。
> nsq的源码写法和一些设计思想对我们开发写代码会有一定的提升。 

<!-- TOC -->


- [nsq基础](#nsq基础)
  - [nsq是什么](#nsq是什么)
  - [nsq应用场景](#nsq应用场景)




<!-- /TOC -->

# nsq基础

## nsq是什么

**nsq**是**Go**语言编写的一个开源的**实时分布式内存消息队列**，其性能十分优异。

**nsq** 是实时的分布式消息处理平台，其设计的目的是用来大规模地处理每天数以**十亿**计级别的消息。它具有分布式和去中心化拓扑结构，该结构具有无单点故障、故障容错、高可用性以及能够保证消息的可靠传递的特征

## nsq应用场景

> 通常来说，消息队列都适用以下场景。

### 异步处理

> 参照下图利用消息队列把业务流程中的非关键流程异步化，从而显著降低业务请求的响应时间。

![](https://github.com/Jet-luoxianjie/nsq_node/blob/main/image/nsq1.png?raw=true)

###  应用解耦

> 通过使用消息队列将不同的业务逻辑解耦，降低系统间的耦合，提高系统的健壮性。后续有其他业务要使用订单数据可直接订阅消息队列，提高系统的灵活性。

![](https://github.com/Jet-luoxianjie/nsq_node/blob/main/image/nsq2.png?raw=true)

### 流量削峰

> 类似秒杀（大秒）等场景下，某一时间可能会产生大量的请求，使用消息队列能够为后端处理请求提供一定的缓冲区，保证后端服务的稳定性。

![enter description here](https://github.com/Jet-luoxianjie/nsq_node/blob/main/image/nsq3.png?raw=true)








