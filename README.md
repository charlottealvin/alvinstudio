# Alvin's Studio — 设计师个人网站

> **本项目基于 [fanstudio](https://github.com/fan18660557495/fanstudio) 进行修改定制。**

一个面向设计师的开源个人网站，开箱即用，前台展示 + 后台管理一体。

所有文字、颜色、内容都能在后台图形界面里修改，**不需要写任何代码**。自适应手机 / 平板 / 电脑，内置亮色 / 暗色自动切换。

![前台首页](docs/screenshots/前台首页.png)

---

## 目录

- [项目介绍](#项目介绍)
- [前台功能](#前台功能)
- [后台功能](#后台功能)
- [技术栈](#技术栈)
- [从零开始本地运行](#从零开始本地运行)
- [Docker 部署](#docker-部署)
- [邮件通知配置（可选）](#邮件通知配置可选)
- [常见问题](#常见问题)
- [License](#license)

---

## 项目介绍

### 前台功能

**首页**
全屏 Hero 区域，带有问候语动画 + 品牌名文字动效 + 头像 + 社交链接入口。下方自动展示最新的知识库文章、设计作品、开发作品、文章和视频教程，每个区块可点击「查看全部」进入对应列表页。

**知识库**
瀑布流卡片展示知识文章，支持分类和标签筛选。详情页展示富文本正文、封面图、发布日期、作者信息。适合整理系统性的专业知识。

**设计作品集**
瀑布流卡片布局展示你的设计作品。支持分类筛选和标签。点击进入详情页可查看完整描述、多张展示图，如果关联了 Figma 链接还会自动嵌入 Figma 在线预览。

**开发作品集**
和设计作品集结构相同，独立页面，适合放 GitHub 项目、工具插件等技术类作品。

**个人博客**
瀑布流卡片展示所有文章，支持分类筛选。详情页展示富文本正文、封面图、发布日期、作者信息。

**视频教程**
瀑布流卡片展示，点击直接跳转到 B 站 / YouTube 等外链平台观看。

**工具导航**
分类展示常用工具链接，方便用户快速访问。

**关于页**
左侧个人信息卡片（头像、品牌名、姓名、职位标签），右侧展示个人介绍、工作经历、学习经历、技能标签。所有内容都在后台填写。

**作品赞助**
设计作品支持设置赞助金额。用户输入邮箱后扫码支付，赞助成功后自动发送下载 / Figma 链接到邮箱。也可以将作品设为免费或开源，用户直接获取。赞助后不支持自助返还，如需返还请在后台「赞助管理」中人工操作。

**访问密码**
支持设置网站访问密码，保护你的作品集不被公开访问。

**页脚**
显示品牌名、版权信息（年份自动更新）、版本号和社交链接。微信 / 公众号支持鼠标悬停弹出二维码。

**主题自定义**
9 种强调色 + 5 种灰度基调，在后台选好后自动全站生效。

| 作品展示 | 暗黑模式 |
|---|---|
| ![前台作品展示](docs/screenshots/前台作品展示.png) | ![前台暗黑模式](docs/screenshots/前台主页暗黑模式.png) |

### 后台功能

登录后台后，你可以管理网站的所有内容。

**仪表盘**
数据概览卡片：文章数、设计作品数、开发作品数、教程数、知识库文章数、赞助总数、本月收入（含环比变化）。页面下方有最近 5 笔赞助记录和近 30 天收入趋势折线图。

**知识库管理**
列表页支持搜索、分类筛选、排序。新建或编辑文章时使用富文本编辑器，支持图片上传、标题、列表、代码块等格式。每篇文章可设为草稿或发布状态。支持分类和标签管理。

**文章管理**
列表页支持搜索、分类筛选、排序。新建或编辑文章时使用富文本编辑器，支持图片上传、标题、列表、代码块等格式。每篇文章可设为草稿或发布状态。

**设计作品管理**
列表管理所有设计作品。每件作品可上传封面和多张展示图、设置价格（也可设为免费或开源）、关联 Figma 链接（前台自动嵌入在线预览）、填写下载交付链接。支持分类和标签。支持版本管理。

**开发作品管理**
结构同设计作品，独立管理。

**视频教程管理**
列表管理，填入视频链接（B 站 / YouTube 等），上传或填写缩略图，设置排序顺序。

**工具管理**
管理工具导航页面展示的工具链接，支持分类管理。

**分类与标签**
统一管理所有内容（文章、作品、教程、知识库、工具）的分类和标签。

**赞助管理**
查看所有作品赞助记录。支持按状态筛选（待支付 / 已支付 / 已取消 / 已返还）和批量操作。返还操作由管理员在后台手动执行，款项将原路退回。

**网站设置**
四个 Tab 面板，涵盖网站的所有可自定义内容：

| Tab | 包含内容 |
|---|---|
| 基本设置 | 网站名称、网站描述（SEO）、页脚版权信息、社交链接（9 个平台）、访问密码 |
| 导航与页面 | 各页导航名称、首页 Hero 文案、各页页头介绍、模块固定封面比例、关于页区块标题 |
| 关于我 / 头像 | 头像上传、品牌名、姓名、职位、个人介绍、工作经历、学习经历、技能 |
| 外观主题 | 基底灰度（5 选 1）、强调色（9 选 1），实时预览 |

| 后台首页 | 后台暗黑模式 | 作品编辑 |
|---|---|---|
| ![后台首页](docs/screenshots/后台首页.png) | ![后台暗黑模式](docs/screenshots/后台主页暗黑模式.png) | ![后台作品编辑](docs/screenshots/后台作品编辑.png) |

---

## 技术栈

| 技术 | 版本 | 说明 |
|------|------|------|
| **Next.js** | 16.1.6 | 全栈框架，App Router |
| **React** | 19.2.3 | UI 渲染 |
| **TypeScript** | 5.x | 类型安全 |
| **Tailwind CSS** | 4.x | 原子化样式 |
| **MySQL** | 8.0+ | 数据库 |
| **Prisma** | 6.19.2 | ORM |
| **NextAuth.js** | 5.0.0-beta.30 | 认证 |
| **BlockNote** | 0.46.2 | 富文本编辑器 |
| **Framer Motion** | 12.31.0 | 动画库 |
| **shadcn/ui** | - | UI 组件库 |
| **Recharts** | 3.7.0 | 图表库 |
| **微信支付** | - | 赞助支付 |

---

## 从零开始本地运行

> **适合谁**：从来没有写过代码的设计师，电脑上什么开发工具都没装过。

### Step 1: 安装 Node.js

访问 https://nodejs.org，下载 **LTS** 版本并安装。

### Step 2: 安装 MySQL

访问 https://dev.mysql.com/downloads/installer/，下载并安装 MySQL 8.0。安装过程中设置 root 密码并记住。

### Step 3: 下载项目代码

```bash
git clone https://github.com/你的用户名/alvinstudio.git
cd alvinstudio
```

### Step 4: 配置环境变量

```bash
cp .env.example .env
```

编辑 `.env` 文件，修改数据库连接：

```env
DATABASE_URL="mysql://root:你的密码@localhost:3306/alvinstudio"
AUTH_SECRET="随机生成的密钥"
AUTH_URL="http://localhost:3000"
```

### Step 5: 初始化数据库

```bash
# 创建数据库
mysql -u root -p -e "CREATE DATABASE alvinstudio CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"

# 执行迁移
npx prisma migrate deploy

# 写入初始数据
npm run db:seed
```

### Step 6: 启动开发服务器

```bash
npm install
npm run dev
```

### Step 7: 访问网站

- **前台首页**：http://localhost:3000
- **后台管理**：http://localhost:3000/admin
- **默认管理员**：`admin@example.com` / `admin123`

> 请登录后台后立即修改密码。

---

## Docker 部署

项目支持 Docker 一键部署，详见 [Docker 部署指南](docs/DOCKER_DEPLOY.md)。

```bash
# 克隆项目
git clone https://github.com/你的用户名/alvinstudio.git
cd alvinstudio

# 配置环境变量
cp .env.example .env
# 编辑 .env，设置 NEXTAUTH_SECRET

# 启动服务
docker-compose up -d
```

访问 http://localhost:3333 即可看到网站。

---

## 邮件通知配置（可选）

配置后，用户赞助成功会自动收到邮件（含下载链接），返还时也会收到通知邮件。

在 `.env` 文件中添加：

```env
SMTP_HOST="smtp.163.com"
SMTP_PORT="465"
SMTP_USER="your-email@163.com"
SMTP_PASS="授权码"
EMAIL_FROM="your-email@163.com"
```

---

## 常见问题

| 问题 | 解决方案 |
|------|----------|
| `npm install` 很慢 | 切换镜像源：`npm config set registry https://registry.npmmirror.com` |
| MySQL 连接失败 | 检查 MySQL 服务是否运行，`.env` 中密码是否正确 |
| 端口 3000 被占用 | 修改端口：`PORT=3001 npm run dev` |
| 后台登录失败 | 确认 `db:seed` 执行成功，或重新执行 `npm run db:seed` |

---

## 项目结构

```
alvinstudio/
├── src/
│   ├── app/
│   │   ├── (frontend)/          # 前台页面
│   │   │   ├── about/           # 关于页
│   │   │   ├── blog/            # 个人博客
│   │   │   ├── knowledge-base/  # 知识库
│   │   │   ├── tools/           # 工具导航
│   │   │   ├── tutorials/       # 视频教程
│   │   │   ├── works/           # 作品集
│   │   │   └── password/        # 访问密码验证
│   │   ├── admin/               # 后台管理页面
│   │   └── api/                 # API 接口
│   ├── components/
│   │   ├── ui/                  # 基础 UI 组件
│   │   ├── frontend/            # 前台专用组件
│   │   ├── admin/               # 后台专用组件
│   │   └── react-bits/          # 动效组件
│   ├── hooks/                   # 自定义 Hooks
│   ├── lib/                     # 工具函数和配置
│   └── contexts/                # React Context
├── prisma/
│   ├── schema.prisma            # 数据库模型
│   ├── migrations/              # 迁移文件
│   └── seed.ts                  # 初始数据
├── public/                      # 静态资源
├── docs/                        # 文档
├── scripts/                     # 脚本
├── docker-compose.yml           # Docker 编排
├── Dockerfile                   # Docker 镜像
└── package.json                 # 项目配置
```

---

## 功能模块

| 模块 | 数据模型 | 说明 |
|------|----------|------|
| 知识库 | `knowledgebasearticle` | 系统性知识文章，支持分类和标签 |
| 个人博客 | `post` | 博客文章，支持分类和标签 |
| 设计作品 | `work` (DESIGN) | 设计作品集，支持版本管理 |
| 开发作品 | `work` (DEVELOPMENT) | 开发作品集，支持版本管理 |
| 视频教程 | `videotutorial` | 外链视频教程 |
| 工具导航 | `tool` | 工具链接导航 |
| 订单 | `order` | 作品赞助订单 |
| 用户 | `user` | 管理员和体验账户 |
| 设置 | `settings` | 网站全局设置 |

---

## License

MIT，详见 [LICENSE](LICENSE)。

你可以自由使用、修改、二次开发。欢迎 Fork 和 Star。
