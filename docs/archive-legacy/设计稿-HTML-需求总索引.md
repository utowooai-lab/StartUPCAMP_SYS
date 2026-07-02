# 设计稿 / HTML / 功能需求总索引

更新时间：2026-07-02

本文件用于把 `codex://threads/019f0cf6-0470-7c20-8c04-dd7be69f01b3`、`codex://threads/019f1d22-e1e2-7ab0-8937-99095ef972cc`、`codex://threads/019f1d70-6d95-7ac1-b663-d81a1a7b5070` 三个对话中的「功能需求描述」「确认的设计稿」「基于设计稿实现的 HTML」统一整理起来，并定义当前 HTML 原型使用的设计系统与素材归档规则。

## 1. 固定目录

### HTML 原型目录

`/Volumes/AppleEx/VideCoding WorkSpace/StartupCampSaaS_Design/exports/design-pages/individual`

### 固定设计素材包

`/Volumes/AppleEx/VideCoding WorkSpace/StartupCampSaaS_Design/StartUpCampSaaS_Project_src/design-assets/html-design-package`

目录结构：

| 目录 | 用途 |
| --- | --- |
| `confirmed-designs/` | 已确认的整页设计稿，命名与 HTML 文件前缀和功能名保持一致 |
| `component-states/` | 已确认的弹窗、任务页改版、记录类型等局部状态设计稿 |
| `html-pages/` | 当前三个对话产出的全部 HTML 页面副本，作为可打开的原型快照 |
| `current-design-screens/` | 当前 `exports/design-pages/individual` 下全部 PNG 设计稿/页面截图副本 |
| `raw-generated-by-thread/` | 三个 Codex 对话原始生成图，按 thread id 分目录完整保存 |
| `reusable-assets/` | HTML 可复用切图：Logo、登录插画、卡片、弹窗、侧栏、流程卡等 |
| `reference-screens/` | 用于延续视觉风格的完整页面参考图 |

> 说明：原始生成图仍保留在 `/Users/woo/.codex/generated_images/`，本目录已复制三条指定对话的生成图，方便后续不依赖 Codex 缓存也能追溯。

## 2. 页面总表

| 模块 | 功能需求描述 | 确认设计稿 / 设计依据 | HTML |
| --- | --- | --- | --- |
| 登录 | 用户用手机号/账号进入系统，登录后按角色进入学员端、家长端、老师端；提供注册入口。 | `confirmed-designs/01-login-role-entry-登录与角色进入.png` | `01-login-role-entry.html` |
| 注册身份选择 | 新用户选择学员、家长、老师身份，进入不同信息填写流程。 | `confirmed-designs/02-register-identity-select-选择注册身份.png` | `02-register-identity-select.html` |
| 老师注册 - 基础档案 | 老师填写姓名、手机号、身份类型、基础资料；邀请链接场景可带入教师类型与营地。 | `confirmed-designs/03-teacher-register-step1-老师注册基础档案.png` | `03-teacher-register-step1.html` |
| 老师注册 - 营地信息 | 老师提交参与营地、交通、住宿、职责相关信息。 | 延续 `03-teacher-register-step1` 的注册分屏和步骤条；整页确认稿待补充归档。 | `04-teacher-register-step2.html` |
| 老师注册 - 账号审核 | 老师设置登录账号，确认资料并提交后台审核。 | 延续老师注册设计系统；整页确认稿待补充归档。 | `05-teacher-register-step3.html` |
| 老师工作台 - 我的队伍 | 带队老师查看负责队伍、队员、项目，支持团队/项目记录查看和管理。 | `component-states/06-老师工作台-我的队伍-队伍复盘弹窗.png`、`component-states/06-老师工作台-我的队伍-项目复盘弹窗.png`、`reusable-assets/teacher-team-management-panel.png` | `06-teacher-dashboard-teams.html` |
| 老师工作台 - 学生点评 | 带队老师查看学生列表，按学生填写点评、评分、可见性说明。 | `reusable-assets/teacher-student-table-panel.png`，并沿用老师端顶栏、侧栏、表格系统。 | `07-teacher-dashboard-students.html` |
| 老师工作台 - 每日任务 | 老师按营地日程查看任务，进入个人、团队、项目记录弹窗，完成记录和点评。 | `component-states/08-teacher-dashboard-tasks-clean-task-list.png`、`component-states/08-老师工作台-记录任务-个人记录弹窗-v2.png`、`component-states/08-老师工作台-记录任务-队伍记录弹窗-v2.png`、`component-states/08-老师工作台-记录任务-项目记录弹窗-v2.png` | `08-teacher-dashboard-tasks.html` |
| 老师任务弹窗 - 个人记录 | 老师填写/查看单个学员每日表现、能力观察、状态与建议。 | `component-states/08-老师工作台-记录任务-个人记录弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师任务弹窗 - 队伍记录 | 老师填写/查看队伍概况、协作观察、冲突卡点与建议。 | `component-states/08-老师工作台-记录任务-队伍记录弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师任务弹窗 - 项目记录 | 老师填写/查看项目概况、Milestone、关键结果、产物、目标达成与下一步。 | `component-states/08-老师工作台-记录任务-项目记录弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师任务弹窗 - 每日汇总 | 老师汇总当日记录，查看发布前摘要。 | `component-states/08-老师工作台-记录任务-每日汇总弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师任务弹窗 - 路演里程碑 | 老师记录路演排练、里程碑和项目进度。 | `component-states/08-老师工作台-记录任务-路演里程碑弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师任务弹窗 - 路演材料上传 | 老师记录/查看项目路演材料提交状态。 | `component-states/08-老师工作台-记录任务-路演材料上传弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师任务弹窗 - 特殊情况 | 老师记录特殊情况，作为报告和运营跟进依据。 | `component-states/08-老师工作台-记录任务-特殊情况记录弹窗.png` | `08-teacher-dashboard-tasks.html` 内弹窗状态 |
| 老师工作台 - 报告推送 | 老师查看报告草稿、家长/学员已读状态，并处理报告发布前后的推送状态。 | `reusable-assets/generated-teacher-record-dashboard.png`，沿用老师端工作台系统。 | `09-teacher-dashboard-reports.html` |
| 学员注册 - 身份确认 | 判断由学员自己填写还是家长代填，决定后续验证和绑定逻辑。 | `confirmed-designs/20-student-register-identity-学员注册身份确认.png` | `20-student-register-identity.html` |
| 学员注册 - 基础档案 | 收集学员基础资料、证件、学校、家长联系人验证信息。 | `confirmed-designs/21-student-register-profile-学员基础档案.png` | `21-student-register-profile.html` |
| 学员注册 - 营地信息 | 学员选择报名营地，提交住宿、交通、服装尺码等营地服务信息。 | `confirmed-designs/22-student-register-camp-info-报名营地信息提交.png` | `22-student-register-camp-info.html` |
| 学员注册 - 营前问卷 | 学员填写兴趣、期待、创业想法、个人偏好等营前问卷。 | `confirmed-designs/23-student-register-precamp-questionnaire-营前问卷.png` | `23-student-register-precamp-questionnaire.html` |
| 学员注册 - 账号确认 | 学员设置登录账号，核对报名信息，确认营地公约并最终提交。 | `confirmed-designs/24-student-register-confirm-account-确认提交与账号确认.png` | `24-student-register-confirm-account.html` |
| 家长注册 - 了解学员问卷 | 家长补充孩子兴趣、表达方式、学习期待等信息。 | `confirmed-designs/25-parent-register-student-questionnaire-了解学员问卷.png` | `25-parent-register-student-questionnaire.html` |
| 家长注册 - 入营安全自查 | 家长填写健康、安全、过敏、接送等风险信息。 | `confirmed-designs/26-parent-register-safety-check-入营安全自查.png` | `26-parent-register-safety-check.html` |
| 家长注册 - 家长账号 | 家长填写本人资料、联系方式，并创建家长账号。 | `confirmed-designs/27-parent-register-account-profile-注册家长账号.png` | `27-parent-register-account-profile.html` |
| 家长注册 - 绑定学生 | 家长绑定学生账号，建立监护关系。 | `confirmed-designs/28-parent-register-bind-student-绑定学生账号.png` | `28-parent-register-bind-student.html` |
| 家长注册 - 确认报告 | 家长核对注册信息与提交结果，查看后续说明。 | `confirmed-designs/29-parent-register-confirm-report-注册确认报告.png` | `29-parent-register-confirm-report.html` |
| 学员工作台 | 学员查看每日记录推送、工作坊资料、团队、结营报告入口；每日记录支持详情弹窗，按老师端记录字段映射展示。 | `current-design-screens/03-学员首页.png`、`reference-screens/student-home.png`、`raw-generated-by-thread/019f1d70-6d95-7ac1-b663-d81a1a7b5070/` | `22-student-dashboard-day-flow.html` |
| 家长工作台 | 家长切换绑定孩子，查看孩子每日记录、课程、报告、相册和反馈入口；每日记录支持详情弹窗与家长回执。 | `current-design-screens/12-家长首页.png`、`reference-screens/parent-home.png`、`raw-generated-by-thread/019f1d70-6d95-7ac1-b663-d81a1a7b5070/` | `23-parent-dashboard-day-flow.html` |

## 3. 三个对话的归档范围

| 对话 | 主要产出 | 已归档位置 |
| --- | --- | --- |
| `019f0cf6-0470-7c20-8c04-dd7be69f01b3` | 登录页、注册身份选择、老师注册三步、老师工作台、老师任务弹窗/记录表单相关设计图 | `raw-generated-by-thread/019f0cf6-0470-7c20-8c04-dd7be69f01b3/` |
| `019f1d22-e1e2-7ab0-8937-99095ef972cc` | 学员注册 20-24、家长注册 25-29 的整页设计稿与 HTML | `raw-generated-by-thread/019f1d22-e1e2-7ab0-8937-99095ef972cc/` |
| `019f1d70-6d95-7ac1-b663-d81a1a7b5070` | 学员/家长工作台、每日记录详情弹窗、家长回执、移动端顺序调整相关设计图 | `raw-generated-by-thread/019f1d70-6d95-7ac1-b663-d81a1a7b5070/` |

## 4. 当前 HTML 快照

`html-pages/` 中已复制当前可打开的 21 个 HTML 页面：

| 文件 | 页面 |
| --- | --- |
| `01-login-role-entry.html` | 登录与角色进入 |
| `02-register-identity-select.html` | 选择注册身份 |
| `03-teacher-register-step1.html` | 老师注册基础档案 |
| `04-teacher-register-step2.html` | 老师报名营地信息提交 |
| `05-teacher-register-step3.html` | 老师创建账号并提交审核 |
| `06-teacher-dashboard-teams.html` | 老师工作台：我的队伍 |
| `07-teacher-dashboard-students.html` | 老师工作台：学生管理 |
| `08-teacher-dashboard-tasks.html` | 老师工作台：每日任务 |
| `09-teacher-dashboard-reports.html` | 老师工作台：报告推送 |
| `20-student-register-identity.html` | 学员注册身份确认 |
| `21-student-register-profile.html` | 学员基础档案 |
| `22-student-register-camp-info.html` | 学员报名营地信息 |
| `23-student-register-precamp-questionnaire.html` | 学员营前问卷 |
| `24-student-register-confirm-account.html` | 学员账号确认与最终提交 |
| `25-parent-register-student-questionnaire.html` | 家长了解学员问卷 |
| `26-parent-register-safety-check.html` | 家长入营安全自查 |
| `27-parent-register-account-profile.html` | 家长账号注册 |
| `28-parent-register-bind-student.html` | 家长绑定学生账号 |
| `29-parent-register-confirm-report.html` | 家长注册确认报告 |
| `22-student-dashboard-day-flow.html` | 学员工作台 / 每日记录 |
| `23-parent-dashboard-day-flow.html` | 家长工作台 / 每日记录 |

## 5. 旧设计稿与待补 HTML

导出目录里还存在一批 01-19 的早期/移动端设计稿 PNG，其中部分暂未找到一一对应的当前 HTML。已统一复制到 `current-design-screens/`，建议作为需求池和视觉参考保留，不直接作为「已确认 HTML 对应稿」使用。

| 设计稿 | 对应功能 |
| --- | --- |
| `01-登录页.png` | 旧登录页参考 |
| `02-信息收集页.png` | 旧信息收集流程参考 |
| `03-学员首页.png` | 旧学员首页参考 |
| `04-学员任务提交.png` | 学员任务提交弹窗/页面 |
| `05-学员创业想法提交.png` | 学员创业想法提交 |
| `06-学员团队管理.png` | 学员团队管理 |
| `07-学员成长报告.png` | 学员成长报告 |
| `08-学员营地相册.png` | 学员营地相册 |
| `09-老师工作台.png` | 老师工作台旧整页参考 |
| `10-老师营地记录.png` | 老师营地记录 |
| `11-老师AI报告生成.png` | 老师 AI 报告生成 |
| `12-家长首页.png` | 家长首页旧整页参考 |
| `13-家长营地点评.png` | 家长查看营地点评 |
| `14-家长问题反馈.png` | 家长问题反馈 |
| `15-后台首页.png` | 后台首页 |
| `16-后台营地基础配置.png` | 后台营地基础配置 |
| `17-后台课程资料任务管理.png` | 后台课程、资料、任务管理 |
| `18-后台记录报告管理.png` | 后台记录、报告管理 |
| `19-后台相册反馈管理.png` | 后台相册、反馈管理 |

## 6. 设计系统定义

### 6.1 产品气质

系统面向营地运营、老师、学员和家长，视觉应同时满足：

- 学员/家长端：亲和、明亮、轻量，有成长感和科技感。
- 老师端：信息密度更高，但仍保持清晰、轻盈、可快速扫描。
- 后台端：以运营效率为主，使用更克制的表格、筛选、状态和批量操作。

### 6.2 色彩

| Token | 用途 | 建议值 |
| --- | --- | --- |
| `--color-primary` | 主按钮、重点文字、选中态 | `#246BFE` |
| `--color-primary-dark` | 顶栏、强品牌区 | `#0B56D8` |
| `--color-primary-soft` | 浅蓝底、标签、弱强调 | `#EAF2FF` |
| `--color-bg` | 主应用背景 | `#F4F8FF` |
| `--color-surface` | 卡片、弹窗、主内容容器 | `#FFFFFF` |
| `--color-border` | 分割线、输入框描边 | `#DDE7F5` |
| `--color-text` | 主文本 | `#1F2A44` |
| `--color-muted` | 次级说明 | `#66748A` |
| `--color-warning` | 队长、待处理、提醒 | `#FFB84D` |
| `--color-success` | 已完成、已发布 | `#20B486` |
| `--color-danger` | 删除、退回、异常 | `#F05252` |

背景允许使用浅蓝、浅粉、浅紫的柔和径向渐变，但页面主体不能被单一颜色铺满。

### 6.3 字体与排版

- 字体：优先使用系统中文字体，CSS 建议 `-apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC", "Microsoft YaHei", sans-serif`。
- 页面 H1：28-36px，700-800。
- 区块标题：20-24px，700。
- 卡片标题：16-18px，700。
- 正文：14-16px，400-500。
- 辅助说明：12-14px，颜色使用 `--color-muted`。
- 字间距保持默认，不使用负字距。

### 6.4 布局

- 登录/注册页：桌面端左右分屏，左侧品牌插画/价值主张，右侧表单卡片；移动端保留表单为主。
- 工作台页：顶部品牌栏 + 左侧身份/资料侧栏 + 右侧主工作区。
- 主内容最大宽度根据页面复杂度控制在 1180-1320px；表格和任务页允许更宽。
- 页面区块使用完整内容带，不把大页面区块都做成浮动卡片。
- 卡片只用于独立信息单元、列表项、弹窗和表单容器。

### 6.5 组件

| 组件 | 规范 |
| --- | --- |
| 顶栏 | 品牌蓝底，左侧 Logo，右侧角色/设置；高度 64-70px |
| 侧栏身份卡 | 浅蓝卡片，大头像，角色标签，基础信息 |
| 主按钮 | 品牌蓝实心，圆角 10-12px，高度 44-48px |
| 次按钮 | 白底蓝字或浅蓝底，边框使用 `--color-border` |
| 输入框 | 浅灰蓝填充或白底细边框，高度 44-48px |
| 步骤条 | 圆点/短线组合，当前步骤品牌蓝，高亮当前流程 |
| Tab | 蓝色文字 + 2px 下划线选中态 |
| 表格 | 浅灰表头、状态标签、右侧操作按钮；老师端可提高密度 |
| 弹窗 | 半透明灰蓝遮罩，白底 12-16px 圆角，标题居中或左对齐，底部主操作清晰 |
| 上传区 | 浅底、虚线或图标提示，缩略图圆角 8-10px |
| 状态标签 | 使用蓝/绿/黄/红区分草稿、已提交、待处理、异常 |

### 6.6 角色差异

| 角色 | 信息架构重点 |
| --- | --- |
| 学员 | 今日任务、资料、团队、提交、报告入口 |
| 家长 | 孩子切换、已发布记录/报告、课程、相册、反馈 |
| 老师 | 班级/队伍筛选、学生列表、每日记录、任务点评、报告推送 |
| 后台 | 营地配置、人员关系、内容任务、记录报告、相册反馈、导入导出 |

## 7. 功能需求来源摘要

当前页面整理依据项目文档中的产品边界和页面需求，核心规则如下：

- 系统覆盖营前报名建档、营中课程任务与老师点评、营后报告导出与复盘。
- 用户端包含老师、学员、家长三类用户；后台用于营地运营和管理员配置。
- 学员是主账号，可本人创建，也可由家长代为创建。
- 家长以独立账号存在，可绑定多个学员。
- 老师与管理员由后台创建和授权，不开放普通自注册；当前老师注册 HTML 可作为邀请/审核型原型。
- 家长可见内容必须是已审核并发布的记录、点评、报告或相册。
- AI 报告只能生成草稿，不能替代老师判断，也不能未经审核直接对家长发布。

## 8. 后续整理建议

1. 为 `04-teacher-register-step2.html`、`05-teacher-register-step3.html` 补齐最终整页确认稿，并放入 `confirmed-designs/`。
2. 为 `22-student-dashboard-day-flow.html`、`23-parent-dashboard-day-flow.html` 输出最终整页确认稿，当前已保留旧参考图和线程原始生成图。
3. 如果继续实现 01-19 旧 PNG 中的学员任务、Idea、相册、家长反馈、后台页面，应新建对应 HTML，并按 `编号-html-name-功能名` 重新归档确认稿。
4. 后续新增页面统一遵循：先归档确认稿到 `confirmed-designs/`，再导出 HTML 到 `exports/design-pages/individual/`，同步复制到 `html-pages/`，最后更新本索引表。
