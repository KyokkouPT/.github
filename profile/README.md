<div align="center">

<img src="./assets/logo.png" width="148" alt="KyokkouPT 极光">

# KyokkouPT

**通用、可配置、可自部署的私有 PT 站引擎**

从注册、发布、审核、做种，到魔力值、考核与站务管理，一套代码跑起完整的私有 Tracker 站点。

![status](https://img.shields.io/badge/status-early%20development-orange?style=flat-square)
![version](https://img.shields.io/badge/version-0.1.0-blue?style=flat-square)
![node](https://img.shields.io/badge/Node.js-24-339933?style=flat-square&logo=node.js&logoColor=white)
![fastify](https://img.shields.io/badge/Fastify-5-000000?style=flat-square&logo=fastify&logoColor=white)
![next](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)

</div>

KyokkouPT 不预设站点形态：站点名、导航、分区与分类、分区字段、用户等级、注册策略、H&R 规则、魔力值产出与兑换、审核策略，全部由后台配置决定。同一份代码可以部署成不同形态的站点。

## 仓库

| 仓库 | 内容 | 技术栈 |
| --- | --- | --- |
| [backend](https://github.com/KyokkouPT/backend) | API、Tracker、经济系统、审核与站务 | Node.js 24 · TypeScript · Fastify 5 · Kysely |
| [frontend](https://github.com/KyokkouPT/frontend) | 站点前台与站务后台 | Next.js 16 · React 19 · Tailwind CSS v4 |

前后端是两个独立仓库，分别安装、构建与部署，只通过 HTTP API 通信。

## 能力

<table>
<tr>
<td width="50%" valign="top">

**目录与发布**

- 分区、分类与分区级自定义字段
- `.torrent` 解析、查重、文件列表
- 审核队列：通过、驳回、退回修改
- 促销：免费、2× 上传、折扣
- 多条件筛选、排序与 RSS 订阅

</td>
<td width="50%" valign="top">

**Tracker 与 H&R**

- announce / scrape，passkey 鉴权
- IPv4 / IPv6 peer 列表
- 下载时只替换 announce，info_hash 不变
- 下载量达标自动生成 H&R 义务
- 做种时长累计，到期结算

</td>
</tr>
<tr>
<td width="50%" valign="top">

**魔力值与经济**

- 产出公式可配置（表达式）
- 商店：库存、限购、等级门槛
- 完整账本与兑换记录
- 求种悬赏：冻结、退回、结算
- 邀请额度与一次性邀请码

</td>
<td width="50%" valign="top">

**账号与安全**

- 开放注册或邀请注册
- 邮箱验证三档：自动、邮件、人工审核
- 密码找回：邮件令牌，限频保护
- TOTP 两步验证与恢复码
- passkey 轮换，旧链接立即失效

</td>
</tr>
<tr>
<td width="50%" valign="top">

**社区与考核**

- 站内通知与 SMTP 邮件，按类型订阅
- 举报、申诉，含免登录封禁申诉
- 排行榜与公开用户主页
- 考核 / 任务按指标结算
- 17 个固定用户组，按条件自动升降

</td>
<td width="50%" valign="top">

**站务管理**

- 审核台、举报工单、反作弊
- 用户处置：警告、停用、封禁、恢复
- 审计日志与 CSV 导出
- 站点设置与分区编辑
- 按条件筛选群发站内信

</td>
</tr>
</table>

界面提供明暗两套主题，桌面与移动端都可完整操作。

## 维护者

[ImJingLan](https://github.com/ImJingLan) - **蜂巢 @xihu** — KyokkouPT 的发起人与维护者，负责整体设计、后端与前端实现、版本发布。

## 许可证

- 后端 [GPL-3.0-or-later](https://github.com/KyokkouPT/backend/blob/main/LICENSE)：可商用、可修改；分发修改版时需按 GPL 提供源码。
- 前端 [Apache-2.0](https://github.com/KyokkouPT/frontend/blob/main/LICENSE)：可商用、可修改、可闭源分发，需保留版权与归属声明。
