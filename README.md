<p align="center">
  <img src="./docs/assets/contextgo-readme-header.png" alt="ContextGo Releases" width="100%">
</p>

<p align="center">
  <img src="./docs/assets/contextgo-logo.png" alt="ContextGo Logo" width="108">
</p>

<p align="center">
  <strong>ContextGo Releases</strong><br>
  ContextGo 的公共发行与分发出口。
</p>

<p align="center">
  <a href="./README_EN.md">English</a> ·
  <a href="https://github.com/contextgo/contextgo">ContextGo 主仓</a> ·
  <a href="https://github.com/contextgo/contextgo-releases">GitHub</a>
</p>

---

## 这是什么

`contextgo-releases` 是 ContextGo 产品矩阵中的公共发布仓库。

它的职责很简单，但很关键：

- 对外提供安装包和 GitHub Releases
- 对外提供版本元数据、清单和更新器可消费内容
- 对外提供网站可读取的公开发布内容

它不是主产品源码仓，也不承载内部研发文档。

---

## 为什么要单独存在

ContextGo 的产品源码、网站源码、内部计划和自动化流程可以继续在主仓演进，但公共发行面需要一个更稳定、更干净的出口。

把发布仓单独拆出来，可以同时做到：

- 安装包和公开发布历史可见
- 桌面更新器和下载中心有稳定 source of truth
- 官网可以消费公开结构化内容
- 不暴露私有源码、未完成实现和内部文档

---

## 这里包含什么

这个仓库应该承载：

- GitHub Releases 及其安装包附件
- release metadata
- checksums 与可分发清单
- `site/` 下导出的公开网站内容

对于网站侧：

- `site/docs/` 存储版本化文档 payload
- `site/blog/` 存储公开博客 payload
- 每篇内容目录同时包含：
  - `article.json`
  - `source.mdx`

---

## 这里不包含什么

这个仓库不应该承载：

- 主产品源码
- 内部工程计划或设计文档
- 手工维护的网站构建产物来源真相

它是一个**公开分发出口**，不是研发主仓的替代品。

---

## 它如何被消费

`contextgo-releases` 服务的对象主要有三类：

- 最终用户
  - 通过 Releases 下载安装包
- 桌面更新器 / 下载中心
  - 读取版本与分发元数据
- 官网
  - 消费 `site/` 下导出的公开内容

这个仓库的存在，是为了让“发布”成为一个公开、稳定、可消费的事实层。

---

## 和主仓的关系

两者职责拆分如下：

- [`contextgo`](https://github.com/contextgo/contextgo)
  - 产品代码
  - WebUI / mobile shell
  - Agent Package
  - Context Engine
  - 网站源码与发布自动化
- [`contextgo-releases`](https://github.com/contextgo/contextgo-releases)
  - 公共 artifacts
  - 公共 manifests
  - 公共 release history
  - 导出的公共 docs / blog 内容

主仓负责“生产”，发布仓负责“公开分发”。

---

## 面向用户的入口

如果你只是想获取 ContextGo：

- 直接查看本仓的 GitHub Releases

如果你想了解完整产品：

- 查看 [ContextGo 主仓](https://github.com/contextgo/contextgo)

如果你想了解相关子项目：

- [Connector](https://github.com/contextgo/connector)
- [SkillMarket](https://github.com/contextgo/skillmarket)

---

## 公开分发原则

这个仓库默认遵循这些长期原则：

- Git tag + GitHub Release 是公共发布真相源
- 官网消费 release metadata，而不是重新发明一套版本真相
- 公共发布仓可以和主源码仓分离，但品牌和产品身份保持一致

这保证了 ContextGo 在产品快速演进的同时，仍有一个稳定的公开出口。
