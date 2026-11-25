# 贡献指南（通用规则）

KyokkouPT 由两个独立仓库组成，分别安装、构建与提交：

| 仓库 | 内容 | 技术栈 | 仓库内指南 |
| --- | --- | --- | --- |
| [backend](https://github.com/KyokkouPT/backend) | API、Tracker、经济系统、审核与站务 | Node.js 24 · TypeScript · Fastify 5 · Kysely | [backend/CONTRIBUTING.md](https://github.com/KyokkouPT/backend/blob/main/CONTRIBUTING.md) |
| [frontend](https://github.com/KyokkouPT/frontend) | 站点前台与站务后台 | Next.js 16 · React 19 · Tailwind CSS v4 | [frontend/CONTRIBUTING.md](https://github.com/KyokkouPT/frontend/blob/main/CONTRIBUTING.md) |

本文是通用规则。启动命令、目录结构、提交前检查见各仓库自己的贡献指南。

## 贡献者许可协议

CLA 位于 `.github` 仓库的 [`CLA/`](CLA/README.md) 目录：英文正式文本 [CLA.en.md](CLA/CLA.en.md)，中文译本 [CLA.zh-CN.md](CLA/CLA.zh-CN.md)。以英文版本为准。

提交贡献即视为同意 CLA（包括创建 Pull Request 或在 Issue 中发布代码）。PR 模板里保留了勾选行，用于记录你的同意，建议勾选。

> - [ ] 我已阅读并同意 [CLA](https://github.com/KyokkouPT/.github/blob/main/CLA/CLA.en.md)（以英文版本为准）

CLA 可能迁移到其他位置，迁移前会提前 7 天公告，以新位置发布的版本为准。

## 提交信息

提交信息必须符合 [Conventional Commits 1.0.0](https://www.conventionalcommits.org/zh-hans/v1.0.0/)：

```text
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

- `type`：`feat`、`fix`、`docs`、`refactor`、`perf`、`test`、`build`、`ci`、`chore`、`style`、`revert`
- `scope`：仓库或模块名；后端用 `api`，前端用 `web`；纯文档提交可省略 scope
- `description`：一句话说明改动，祈使句，句尾不加句号，标题不超过 72 字符
- 破坏性变更：`type(scope)!:`，或在 footer 写 `BREAKING CHANGE: 说明`
- 关联 Issue：在 footer 写 `Closes #12`
- 一个提交只做一件事，提交前能独立构建和测试
- 后端与前端分别提交；跨仓库功能开两个 PR，用相同标题关联，不要声称原子提交

示例：

```text
feat(api): add torrent field filtering
fix(web): avoid captcha hydration mismatch on login
docs: update CLA acceptance clause
```

## Pull Request

- 说明改了什么、为什么改、如何验证；
- 关联相关 Issue；
- 界面改动附截图，明暗主题各一张更好；
- 各仓库的 PR 模板已包含该仓库的检查项。

## 安全

- 不要在 Issue 或 PR 中贴出密钥、密码、passkey、2FA 恢复码或用户数据；
- 发现安全漏洞请私下联系维护者，不要公开细节。

## 不要提交的文件

`node_modules/`、`.env`、`data/`、`.next/`、`dist/`、运行时上传的文件。
