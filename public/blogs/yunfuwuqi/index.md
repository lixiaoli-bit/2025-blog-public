# 🚀 1Panel 面板部署全记录

> 本文档记录了在AWS EC2服务器上完整安装1Panel面板的操作流程，包含系统更新、面板安装、端口放行及访问配置。

---

## 🔐 步骤一：连接服务器，切换到 root 账户

```bash
🔐 步骤一：连接服务器，切换到 root 账户
sudo -i
📦 步骤二：更新系统

```bash
 apt-get update && apt-get upgrade 
⏳ 看到 # 表示更新完成

 🛠️ 步骤三：安装 1Panel
bash -c "$(curl -sSL https://resource.fit2cloud.com/1panel/package/v2/quick_start.sh)"
💡 安装过程中一直按回车，使用默认配置即可

📋 步骤四：查看面板访问信息
安装完成后会显示以下内容：

log
[1Panel 2026-08-01 05:15:15 install Log]: 外部地址： http://16.171.181.217:19384/e97bac1c6d
[1Panel 2026-08-01 05:15:15 install Log]: 内部地址： http://172.31.34.219:19384/e97bac1c6d
[1Panel 2026-08-01 05:15:15 install Log]: 面板用户： 82317eccb6
[1Panel 2026-08-01 05:15:15 install Log]: 面板密码： fcee8c3a1d
🔓 步骤五：开放端口（AWS 安全组配置）
⚠️ 此时外部无法访问，是因为入站规则未开放端口

操作路径：

text
AWS 控制台 → EC2 → 实例 → 选择服务器 → 安全 → 安全组 → 编辑入站规则 → 添加规则 → 端口 19384
🌐 步骤六：访问面板
浏览器打开外部地址：

text
http://16.171.181.217:19384/e97bac1c6d
输入账号密码即可登录 ✅

🎉 部署完成！