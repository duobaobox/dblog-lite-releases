轻量自托管博客，安装包免费公开下载，源码仓库保持私有。

支持 Linux systemd、amd64 和 arm64。安装前请确认服务器允许所需端口访问。

一键安装：

```sh
curl -fsSL https://github.com/duobaobox/dblog-lite-releases/releases/latest/download/install.sh -o /tmp/dblog-install.sh && sudo sh /tmp/dblog-install.sh
```

安装后终端显示后台地址、admin 账号及随机密码；初始化在开放访问前完成。

升级：`sudo dblog upgrade`。升级前自动备份，迁移、启动或健康检查失败时恢复原程序与数据。

可选 `--domain blog.example.com` 使用 Caddy 配置 HTTPS，DNS 须先指向服务器并放行 80/443。
可选 `--with-ai` 安装独立 Node.js 运行环境；模型服务在后台配置。

首次登录后请修改密码、填写正式站点地址，并配置主机备份。

下载入口：[最新稳定版](https://github.com/duobaobox/dblog-lite-releases/releases/latest)。离线环境下载对应 CPU 架构的部署 tar.gz，解包后执行 `sudo sh install.sh`。

维护命令：`sudo dblog status`、`sudo dblog logs`、`sudo dblog backup`、`sudo dblog version`。`sudo dblog uninstall` 移除服务但保留数据。

本仓库只提供客户说明与免费发行包，不包含博客项目源码或开发历史。公开安装包中的前端资源为浏览器运行所需文件。
