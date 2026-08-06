# Docker 入门到实战：从零搭建容器化应用

> **原文地址**：[https://zero-to-tech.pages.dev/dockerdemo.html](https://zero-to-tech.pages.dev/dockerdemohtml)

---

## 📖 简介

🐳 **Docker** 是当今云计算与微服务时代不可或缺的容器化技术，它通过操作系统级虚拟化，将应用及其依赖环境打包为标准镜像，实现了 **"一次构建，到处运行"** 的核心理念，彻底解决了传统开发中"环境不一致"的痛点。

本指南专为具备 Linux 基础的开发者设计，从 Docker 的历史背景、容器与虚拟机的对比等基础知识讲起，逐步深入到安装配置、镜像加速、容器生命周期管理等实操环节。内容涵盖网络模型（bridge/host/none）、自定义网络创建、数据卷挂载与持久化等进阶主题，最后通过部署 PrestaShop 电子商城系统的完整实战，将理论知识与实际应用场景紧密结合，帮助读者在动手实践中真正掌握 Docker 的核心技能，具备独立完成容器化应用部署的能力。

---

*📅 适用版本：Docker CE · 环境要求：Linux 内核 ≥ 3.10*

---

## 📚 目录

- [第一章 · Docker 简介](#第一章--docker-简介)
- [第二章 · 镜像与容器常用配置](#第二章--镜像与容器常用配置)
- [第三章 · Docker 网络与通讯原理](#第三章--docker-网络与通讯原理)
- [第四章 · Docker 数据卷](#第四章--docker-数据卷)
- [第五章 · Docker 部署电子商城](#第五章--docker-部署电子商城-prestashop)
- [常用命令速查表](#常用命令速查表)

---

## 第一章 · Docker 简介

### 🏛️ 1. Docker 历史

Docker 通过 Linux Container 技术将应用变为标准化、可移植、自管理的组件，实现 **"一次构建，到处运行"**。

**✨ 核心特点：**
- 🚀 快速发布
- 📦 部署简单
- 🛠️ 管理方便
- ⚡ 应用密度更高

**📋 版本说明：**

| 版本 | 全称 | 支持周期 |
|:----:|------|:--------:|
| **CE** | 社区版（Community Edition） | 4 个月 |
| **EE** | 企业版（Enterprise Edition） | 12 个月 |

> 💡 Docker 引擎每季度发布稳定版。

---

### ⚖️ 2. 容器 vs 虚拟机

| 对比项 | 🟢 容器 | 🔵 虚拟机 (VM) |
|--------|:-------:|:--------------:|
| **抽象层** | 应用层抽象 | 硬件抽象 |
| **操作系统** | 共享宿主机内核 | 包含完整 OS |
| **体积** | 轻量（数十 MB） | 庞大（数十 GB） |
| **启动速度** | 快（秒级） | 慢（分钟级） |
| **资源开销** | 小 | 高 |
| **隔离方式** | 进程级隔离 | Hypervisor 管理 |

---

### 📥 3. Docker 安装

#### 🐧 Linux 安装（内核 ≥ 3.10）

```bash
# 下载 repo 文件（注意 -O 大写字母O）
wget -O /etc/yum.repos.d/docker.repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo

# 修改系统版本
sed -i 's/$releasever/7/g' /etc/yum.repos.d/docker.repo

# 安装 docker-ce
yum -y install docker-ce

# 查看可用版本并安装指定版本
dnf list docker-ce --showduplicates | sort -r
dnf install docker-ce-<VERSION> docker-ce-cli-<VERSION> containerd.io
📦 离线安装
从 https://download.docker.com/linux/static/stable/x86_64/ 下载 tgz 包，解压并复制到 /usr/bin/，后台运行：

bash
nohup dockerd &
```
📎 参考资料
原文 HTML 页面：Docker 入门到实战 · 清新版

Docker 官方文档：https://docs.docker.com

Docker Hub：https://hub.docker.com

📅 文档整理于 2026 · 基于 Docker CE 版本，适用于 Linux 环境（内核 ≥ 3.10）

⭐ 如果这份指南对你有帮助，欢迎 Star 或分享给更多需要的开发者！

text
