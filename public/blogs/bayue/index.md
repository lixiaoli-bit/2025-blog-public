# 🌱 阿少的八月学习手记

> ✍️ 写给自己看的成长记录  
> 📆 2026.08.14 → 2026.08.31  
> 🧩 Python · Flask · 数据库 · 图表 · 云服务


## 🛠️ 2026-08-31 · 类与图表
- 把类重新写了一遍，这回真的懂了
- ECharts 单独拎出来做了一个模块
- Flask 从数据库取数，画成动态图表 📈
```bash
#echo半月整理一次
# 💻查看所有内容（日期 + 内容） 
sqlite3 /opt/ech0/data/ech0.db "SELECT datetime(created_at, 'unixepoch', 'localtime'), content FROM echos;"

# 📊查看最近10条 
sqlite3 /opt/ech0/data/ech0.db "SELECT datetime(created_at, 'unixepoch', 'localtime'), content FROM echos ORDER BY created_at DESC LIMIT 10;"

# 💾导出到文件 
sqlite3 /opt/ech0/data/ech0.db "SELECT datetime(created_at, 'unixepoch', 'localtime'), content FROM echos;" > /tmp/内容.txt

```


## 🛠️ 2026-08-30 · MySQL 折腾记
- 装上了 MySQL Server
- VSCode 配上数据库插件，舒服了
- Flask 连 MySQL 跑通，函数重新写，思路清晰多了


## 🎨 2026-08-29 · Flask 开张
- Flask 项目根目录搭好了
- 工具目录搞了个淡绿色，看着顺眼


## 📦 2026-08-28 · 类和文件
- 类和对象过了一遍 ✅
- 文件读取笔记整理完 ✅
- 「吾日三省」打卡 APP 做出来了，成就感 🎉


## 🐍 2026-08-27 · 函数
- Python 函数笔记整理
- 学习笔记打包成 APP


## 💸 2026-08-26 · 记账小工具
- 记账 APP 做完啦
- 研究网页打包 APP：
  - [web-to-app](https://github.com/shiahonb777/web-to-app)
  - [Pakr 体验版](https://github.com/ZhangShengFan/Pakr)


## ⚡ 2026-08-25 · 前端小项目
- 用 DeepSeek 写了 TODO 清单 + 番茄时钟
- 技术栈：React + Vite


## 🎬 2026-08-24 · 视频转文字
- 试了下 Python 搞视频转文字，没跑通，先放着


## 📖 2026-08-23 · 数据库
- 数据库正传笔记过了一遍


## 💡 2026-08-20 · 币圈灵感
- 建了个灵感仓库：[crypto_info](https://github.com/lixiaoli-bit/crypto_info)
- 100 天 Python 项目加了图标
- 研究 PyPI，让网页能读懂文字


## 🔧 2026-08-16 · Git 和备份
```bash
# 查提交记录
git log --format='%h %an <%ae> %s'

# 每天看一眼备份（阿里云 OSS）
echo "📂 最新备份文件：" && /opt/ossutil64 ls oss://my-ech0-backup-2026/ech0-backup/ | grep "ech0-data-" | tail -1
echo "📊 备份文件总数：" && /opt/ossutil64 ls oss://my-ech0-backup-2026/ech0-backup/ | grep "ech0-data-" | wc -l
echo "💾 总占用空间：" && /opt/ossutil64 ls oss://my-ech0-backup-2026/ech0-backup/ | grep "ech0-data-" | awk '{sum += $5} END {printf "%.2f KB\n", sum/1024}'

# ✈️ 离开西安 · Termux 小玩具

- 💻 `cmatrix` —— 数字雨特效，装酷用
- 🎨 `figlet "Cool" | lolcat` —— 彩色大字
- 🛠️ `proot` · `openssh` · `sl` 小火车 · `nyancat` 彩虹猫 · `hollywood` 黑客特效
```

## 💳 2026-08-15 · PayPal 和邮件

- 🌍 开通 PayPal：[https://www.paypal.cn/](https://www.paypal.cn/)
- ✉️ 研究邮件定时发送
- 💾 echo 存储方案
- 📁 单独开了个 GitHub 笔记仓库


## 🌐 2026-08-14 · 域名和云

- 🔗 搞了个免费域名：`www.ashao.dpdns.org`
- 🔒 DNS 解析 + SSL 证书配好
- ☁️ 阿里云 OSS + Docker 搭了个「朋友圈」