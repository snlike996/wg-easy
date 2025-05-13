# WireGuard Easy

[![构建并发布最新镜像](https://github.com/wg-easy/wg-easy/actions/workflows/deploy.yml/badge.svg?branch=production)](https://github.com/wg-easy/wg-easy/actions/workflows/deploy.yml)
[![Lint](https://github.com/wg-easy/wg-easy/actions/workflows/lint.yml/badge.svg?branch=master)](https://github.com/wg-easy/wg-easy/actions/workflows/lint.yml)
[![GitHub星星](https://img.shields.io/github/stars/wg-easy/wg-easy)](https://github.com/wg-easy/wg-easy/stargazers)
[![许可证](https://img.shields.io/github/license/wg-easy/wg-easy)](许可证)
[![GitHub 发布](https://img.shields.io/github/v/release/wg-easy/wg-easy)](https://github.com/wg-easy/wg-easy/releases/latest)
[![图片拉取](https://img.shields.io/badge/image_pulls-12M+-blue)](https://github.com/wg-easy/wg-easy/pkgs/container/wg-easy)

<!-- TODO: 发布后移除 -->

> [!警告]
> 您正在查看v15 预发布版的 README 文件。
> 如果您想立即安装 wg-easy，请阅读此处生产分支的 README 文件：[README](https://github.com/wg-easy/wg-easy/tree/production) 或此处获取最新更新的 README 文件：[README](https://github.com/wg-easy/wg-easy/tree/c6dce0f6fb2e28e7e40ddac1498bd67e9bb17cba)

您已经找到了在任何 Linux 主机上安装和管理 WireGuard 的最简单方法！

<!-- 好：更新截图 -->

<p align="center">
<img src="./assets/screenshot.png" width="802" />
</p>

## 功能

- 一体化：WireGuard + Web UI。
- 安装简便，使用简单。
- 列出、创建、编辑、删除、启用和禁用客户端。
- 显示客户端二维码。
- 下载客户端配置文件。
- 统计已连接的客户端。
- 每个已连接客户端的 Tx/Rx 图表。
- 支持 Gravatar。
- 自动亮/暗模式
- 多语言支持
- 一次性链接
- 客户端过期
- Prometheus 指标支持
- IPv6 支持
- CIDR 支持
- 2FA 支持

> [!NOTE]
> 为了更好地管理此项目的文档，它拥有自己的网站：[https://wg-easy.github.io/wg-easy/latest](https://wg-easy.github.io/wg-easy/latest)

<!-- TODO: 发布后移除 -->

> [!WARNING]
> 由于文档仍处于预发布阶段，您可以在此处访问 [https://wg-easy.github.io/wg-easy/Pre-release](https://wg-easy.github.io/wg-easy/Pre-release)

- [入门指南](https://wg-easy.github.io/wg-easy/latest/getting-started/)
- [基础安装](https://wg-easy.github.io/wg-easy/latest/examples/tutorials/basic-installation/)
- [Caddy](https://wg-easy.github.io/wg-easy/latest/examples/tutorials/caddy/)
- [Traefik](https://wg-easy.github.io/wg-easy/latest/examples/tutorials/traefik/)
- [Podman](https://wg-easy.github.io/wg-easy/latest/examples/tutorials/podman-nft/)
- [AdGuard 首页](https://wg-easy.github.io/wg-easy/latest/examples/tutorials/adguard/)

> [!NOTE]
> 如果您想从旧版本迁移到新版本，您可以在此处找到迁移指南：[迁移指南](https://wg-easy.github.io/wg-easy/latest/advanced/migrate/)

## 安装

这是一个快速入门指南，可帮助您快速启动并运行 WireGuard Easy。

有关更详细的安装指南，请参阅[入门](https://wg-easy.github.io/wg-easy/latest/getting-started/)页面。

### 1. 安装 Docker

如果您尚未安装 Docker，请以 root 身份运行以下命令进行安装：

```shell
curl -sSL https://get.docker.com | sh
exit
```

然后重新登录。

### 2. 运行 WireGuard Easy

运行 WireGuard Easy 最简单的方法是使用 Docker Compose。

只需下载 [`docker-compose.yml`](docker-compose.yml) 并执行 `sudo docker compose up -d`。

现在设置一个反向代理，以便能够安全地从互联网访问 Web UI。

如果您想通过 HTTP 访问 Web UI，请将环境变量“INSECURE”更改为“true”。不建议这样做。仅用于测试。

## 捐赠

您喜欢这个项目吗？考虑捐赠。

创始人：[给 Emile 买杯啤酒！](https://github.com/sponsors/WeeJeWel) 🍻

维护者：[给 kaaax0815 买杯咖啡！](https://github.com/sponsors/kaaax0815) ☕

## 开发

### 先决条件

- Docker
- 已启用 Node LTS 和 corepack
- Visual Studio Code

### 开发服务器

这将使用 docker 启动开发服务器

```shell
pnpm dev
```

### 更新自动导入

如果您添加了一些应该自动导入的内容，但 VSCode 报错，请运行：

```shell
cd src
pnpm install
cd ..
```

### 测试命令行

这将使用 docker 启动命令行

```shell
pnpm cli:dev
```

## 许可证

本项目采用仅 AGPL-3.0 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件

本项目与 Jason A. Donenfeld、ZX2C4 或 Edge Security 没有任何关联、关联、授权、认可或官方联系。

“WireGuard”和“WireGuard”徽标是 Jason A. Donenfeld 的注册商标