# [Chat Chat](https://chat.okisdev.com)

> Chat Chat，解锁你的下一级 AI 对话体验。你可以使用 OpenAI、微软 Azure、Claude、Cohere、Hugging Face 等多个 API，让你的 AI 对话体验更加丰富。

[![LICENSE](https://img.shields.io/github/license/okisdev/ChatChat?style=flat-square)](https://github.com/okisdev/ChatChat/blob/master/LICENSE) [![Twitter](https://img.shields.io/twitter/follow/okisdev)](https://twitter.com/okisdev) [![Telegram](https://img.shields.io/badge/Telegram-Chat%20Chat-blue?style=flat-square&logo=telegram)](https://t.me/+uWx9qtafv-BiNGVk)

<p align='center'>
    <a href='README.md'>English</a> | <a href='README.zh_HK.md'>繁体中文</a> | <a>简体中文</a> | <a href='README.JA.md'>日本語</a>
</p>

<p align='center'>
    <a href='https://docs.okis.dev/zh-CN/chat' target='_blank'>
        文档
    </a>
    | <a href='https://github.com/okisdev/ChatChat/issues/3'>常见问题</a>
</p>

## 重要提示

-   本项目仅供学习交流使用，请确保使用前已经阅读了 LICENSE。
-   部分 API 为付费 API，使用前请确保你已经阅读并同意了相关服务条款。
-   本项目会在一定范围内获取到用户部分数据，请确保你已经阅读并同意了隐私政策。
-   部分功能还在开发中，如果遇到任何问题，欢迎提交 PR 或者 Issue。
-   部分模型并不完善，可能出现样式不一致，上下文不连贯，或者生成了不适当内容等问题。

## 预览

### 界面

![UI](https://cdn.harrly.com/project/GitHub/Chat-Chat/img/UI-1.png)

![Dashboard](https://cdn.harrly.com/project/GitHub/Chat-Chat/img/Dashboard-1.png)

### 功能演示

https://user-images.githubusercontent.com/66008528/235539101-562afbc8-cb62-41cc-84d9-1ea8ed83d435.mp4

https://user-images.githubusercontent.com/66008528/235539163-35f7ee91-e357-453a-ae8b-998018e003a7.mp4

## 功能

-   [x] TTS
-   [x] 黑暗模式
-   [x] 与文件聊天
-   [x] 支持多种语言
-   [x] 支持分享对话
-   [x] 支持流信息（SSE）
-   [x] Markdown 格式化
-   [x] 支持消息代码语法高亮
-   [x] 支持 System Prompt
-   [x] 快捷菜单（command + k）
-   [x] 聊天记录（本地和云端同步）
-   [x] 封装的 API（不再需要代理）
-   [x] 支持插件功能（`/search`, `/fetch`）
-   [x] 支持 OpenAI, Microsoft Azure, Claude, Cohere, Hugging Face

## Roadmap

请参考 https://github.com/users/okisdev/projects/7

## 使用

### 前提条件

-   来自 OpenAI、Microsoft Azure、Claude、Cohere、Hugging Face 的任何 API 密钥

### 环境变量

| 变量名称          | 描述                  | 默认 | 是否强制需要 | 提示                                                                                                |
| ----------------- | --------------------- | ---- | ------------ | --------------------------------------------------------------------------------------------------- |
| `DATABASE_URL`    | Postgresql 数据库地址 |      | **Yes**      | 以 `postgresql://` 开头 （如果不需要，请填写 `postgresql://user:password@example.com:port/dbname`） |
| `NEXTAUTH_URL`    | 您的网站 URL          |      | **Yes**      | （带前缀）                                                                                          |
| `NEXTAUTH_SECRET` | NextAuth Secret       |      | **Yes**      | 随机哈希数值（16 位最佳）                                                                           |
| `EMAIL_HOST`      | SMTP Host             |      | No           |                                                                                                     |
| `EMAIL_PORT`      | SMTP Port             | 587  | No           |                                                                                                     |
| `EMAIL_USERNAME`  | SMTP username         |      | No           |                                                                                                     |
| `EMAIL_PASSWORD`  | SMTP password         |      | No           |                                                                                                     |
| `EMAIL_FROM`      | SMTP 发送地址         |      | No           |                                                                                                     |

### 部署

> 请在部署前修改环境变量，更详细的部署流程请看 https://docs.okis.dev/zh-CN/chat/deployment/

#### 本地部署

```bash
git clone https://github.com/okisdev/ChatChat.git
cd ChatChat
cp .env.example .env
pnpm i
pnpm dev
```

#### Vercel

[![部署在 Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/okisdev/ChatChat)

#### Zeabur

访问 [Zeabur](https://zeabur.com) 来部署

#### Railway

[![部署在 Railway](https://railway.app/button.svg)](https://railway.app/template/-WWW5r)

#### Docker

```bash
docker build -t chatchat .
docker run -p 3000:3000 chatchat -e DATABASE_URL="" -e NEXTAUTH_URL="" -e NEXTAUTH_SECRET="" -e EMAIL_HOST="" -e EMAIL_PORT="" -e EMAIL_USERNAME="" -e EMAIL_PASSWORD="" -e EMAIL_FROM=""
```

或者

```bash
docker run -p 3000:3000 -e DATABASE_URL="" -e NEXTAUTH_URL="" -e NEXTAUTH_SECRET="" -e EMAIL_HOST="" -e EMAIL_PORT="" -e EMAIL_USERNAME="" -e EMAIL_PASSWORD="" -e EMAIL_FROM="" ghcr.io/okisdev/chatchat:latest
```

## LICENSE

[AGPL-3.0](./LICENSE)

## 支持我

[![Buy Me A Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/okisdev)

## 技术栈

nextjs / tailwindcss / shadcn UI
