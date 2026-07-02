# HTML Design Package Design System

本文件适配当前目录 `StartUpCampSaaS_Project_src/design-assets/html-design-package/`，用于说明这套 HTML 原型包的设计系统、资产路径和组件使用方式。

## 1. 目录结构

- `html-pages/`：可直接打开的 HTML 页面。
- `html-pages/assets/`：HTML 页面运行所需的本地素材和共享脚本/样式。
- `confirmed-designs/`：已确认的页面设计稿。
- `current-design-screens/`：当前页面与组件状态截图。
- `component-states/`：弹窗、任务状态、组件状态等局部设计稿。
- `reusable-assets/`：可复用 UI 素材、卡片截图、背景、Logo、弹窗参考图。
- `reference-screens/`：早期或补充参考页面。
- `raw-generated-by-thread/`：按 Codex 对话线程归档的生成稿来源。

HTML 页面引用素材时优先使用 `html-pages/assets/`，设计系统文档和人工查阅时优先使用 `reusable-assets/`、`confirmed-designs/`、`component-states/`。

## 2. 品牌与顶栏

可用资产：

- `reusable-assets/top-blue-header.png`
- `reusable-assets/brand-logo-header-white.png`
- `reusable-assets/brand-logo-login-blue.png`
- `html-pages/assets/brand-logo-header-white.png`

设计规则：

- 老师端、学员端、家长端工作台使用高饱和品牌蓝顶栏。
- 深色顶栏使用白色 Logo；登录/注册浅色场景使用蓝色 Logo。
- 顶栏高度保持 64-70px，左侧品牌，右侧消息、设置、用户信息。
- 图标按钮必须水平垂直居中，统一由 `html-pages/assets/icon-centering.css` 兜底。

## 3. 背景系统

可用资产：

- `reusable-assets/app-soft-gradient-background.png`
- `reusable-assets/login-left-hero-panel.png`
- `reusable-assets/login-hero-children-future-city.png`
- `html-pages/assets/login-hero-children-future-city.png`

设计规则：

- 工作台背景使用浅蓝灰底，叠加柔和蓝、紫、粉光感。
- 登录/注册页使用左侧品牌插画面板，右侧承载表单卡片。
- 页面不使用纯灰硬背景，整体保持轻盈、可信、教育科技感。

## 4. 页面设计稿对应

已确认页面设计稿位于 `confirmed-designs/`：

- `01-login-role-entry-登录与角色进入.png`
- `02-register-identity-select-选择注册身份.png`
- `03-teacher-register-step1-老师注册基础档案.png`
- `04-teacher-register-step2-老师注册营地报名V1.png`
- `04-teacher-register-step2-老师注册营地报名V2.png`
- `04-teacher-register-step2-老师注册营地报名V3.png`
- `05-teacher-register-step3-老师注册确认审核png.png`
- `06-teacher-workstation-老我的队伍.png`
- `07-teacher-workstation-学生点评.png`
- `08-teacher-workstation-老每日任务.png`
- `09-teacher-workstation-老报告推送.png`
- `20-student-register-identity-学员注册身份确认.png`
- `21-student-register-profile-学员基础档案.png`
- `22-student-register-camp-info-报名营地信息提交.png`
- `23-student-register-precamp-questionnaire-营前问卷.png`
- `24-student-register-confirm-account-确认提交与账号确认.png`
- `25-parent-register-student-questionnaire-了解学员问卷.png`
- `26-parent-register-safety-check-入营安全自查.png`
- `27-parent-register-account-profile-注册家长账号.png`
- `28-parent-register-bind-student-绑定学生账号.png`
- `29-parent-register-confirm-report-注册确认报告.png`

对应 HTML 位于 `html-pages/`，文件名保持英文页面编号，便于跳转与维护。

## 5. 角色身份卡片

可用资产：

- `reusable-assets/profile-card-student-leader.png`
- `reusable-assets/profile-card-parent.png`
- `reusable-assets/profile-card-teacher.png`

设计规则：

- 卡片使用浅蓝底、白色描边头像、轻阴影。
- 角色徽章用于区分学员、家长、老师、队长、队员。
- 头像、徽章、状态图标均需居中，避免文字图标偏移。

## 6. 侧栏信息卡片

可用资产：

- `reusable-assets/sidebar-my-courses-card.png`
- `reusable-assets/sidebar-material-card.png`

适用场景：

- 我的课程
- 相关资料
- 今日资料
- 待处理事项

设计规则：

- 白色卡片，圆角 12-14px。
- 标题左侧使用蓝色线性图标，可带小面积黄色点缀。
- 列表 bullet 使用小蓝点或菱形。
- 右侧操作按钮使用蓝色描边小按钮。

## 7. 功能入口卡片

可用资产：

- `reusable-assets/feature-card-submit-idea-banner.png`
- `reusable-assets/feature-card-camp-album.png`
- `reusable-assets/feature-card-feedback.png`

适用页面：

- `html-pages/22-student-dashboard-day-flow.html`
- `html-pages/23-parent-dashboard-day-flow.html`

设计规则：

- 主入口卡使用浅蓝底、大号品牌蓝标题、轻拟物图标。
- 学员端入口包含课程、资料、相册、创业想法。
- 家长端入口包含课程、资料、相册、反馈。
- hover 可轻微上浮，阴影增强，但不要破坏工作台的信息密度。

## 8. 中央业务面板

可用资产：

- `reusable-assets/center-workshop-task-panel.png`
- `reusable-assets/parent-review-main-panel.png`
- `reusable-assets/teacher-student-table-panel.png`
- `reusable-assets/teacher-team-management-panel.png`
- `reusable-assets/generated-teacher-record-dashboard.png`
- `reusable-assets/generated-parent-report-cards.png`

设计规则：

- 主内容区使用大白色面板，圆角 12-14px。
- 老师端允许更高密度表格，但仍需保留清晰分区。
- 表格使用浅灰表头、状态标签、蓝色操作按钮。
- 筛选条由搜索框、下拉框、筛选按钮组成。

## 9. 团队展示与管理

可用资产：

- `reusable-assets/team-card-student-leader.png`
- `reusable-assets/modal-edit-team.png`
- `component-states/06-老师工作台-我的队伍-队伍复盘弹窗.png`
- `component-states/06-老师工作台-我的队伍-项目复盘弹窗.png`

适用页面：

- `html-pages/06-teacher-dashboard-teams.html`

设计规则：

- 团队卡片可使用独立白卡。
- 队长头像比普通队员更突出。
- 队员头像圆形排列，角色标签使用胶囊样式。
- 协助组队弹窗使用多步骤结构：队伍设置、添加队员、确认组队。

## 10. 弹窗体系

可用资产：

- `reusable-assets/modal-submit-idea-form.png`
- `reusable-assets/modal-feedback-form.png`
- `reusable-assets/modal-edit-team.png`
- `reusable-assets/modal-task-submit.png`
- `reusable-assets/modal-album-grid.png`
- `component-states/08-老师工作台-记录任务-个人记录弹窗.png`
- `component-states/08-老师工作台-记录任务-队伍记录弹窗.png`
- `component-states/08-老师工作台-记录任务-项目记录弹窗.png`
- `component-states/08-老师工作台-记录任务-每日汇总弹窗.png`
- `component-states/08-老师工作台-记录任务-路演里程碑弹窗.png`
- `component-states/08-老师工作台-记录任务-路演材料上传弹窗.png`
- `component-states/08-老师工作台-记录任务-特殊情况记录弹窗.png`

设计规则：

- 遮罩层使用半透明灰蓝，可带轻微 blur。
- 弹窗白底，圆角 12-18px。
- 标题区包含图标、标题、说明文字和右上关闭按钮。
- 普通详情弹窗宽度约 560px；复杂表单弹窗宽度约 900-960px。
- 大表单内容可滚动，底部操作区保持清晰。
- 报告回执弹窗需要展示已读状态、家长留言正文和时间。

## 11. 表单与上传

可用资产：

- `reusable-assets/register-step-form-card.png`
- `reusable-assets/register-camp-selector-card.png`
- `reusable-assets/camp-uniform-size-chart.png`
- `html-pages/assets/camp-uniform-size-chart.png`

设计规则：

- 输入框高度 44-48px。
- 文本域高度 120-160px。
- 表单 label 在输入框上方。
- 上传区使用浅灰底、虚线边框或大加号图标。
- 注册流程统一支持保存草稿、获取验证码、提交成功反馈。

## 12. 登录与注册流程

适用页面：

- `html-pages/01-login-role-entry.html`
- `html-pages/02-register-identity-select.html`
- `html-pages/03-teacher-register-step1.html`
- `html-pages/04-teacher-register-step2.html`
- `html-pages/05-teacher-register-step3.html`
- `html-pages/20-student-register-identity.html`
- `html-pages/21-student-register-profile.html`
- `html-pages/22-student-register-camp-info.html`
- `html-pages/23-student-register-precamp-questionnaire.html`
- `html-pages/24-student-register-confirm-account.html`
- `html-pages/25-parent-register-student-questionnaire.html`
- `html-pages/26-parent-register-safety-check.html`
- `html-pages/27-parent-register-account-profile.html`
- `html-pages/28-parent-register-bind-student.html`
- `html-pages/29-parent-register-confirm-report.html`

设计规则：

- 桌面端保留左右分屏，左侧品牌插画，右侧表单。
- 移动端隐藏或弱化左侧插画，保留 Logo、标题、步骤、表单。
- 步骤条使用数字圆点和完成态对勾。
- 当前步骤使用品牌蓝，已完成步骤使用绿色。

## 13. 入营流程与创业想法

可用资产：

- `reusable-assets/onboarding-flow-three-step.png`
- `reusable-assets/onboarding-flow-active-card.png`
- `reusable-assets/idea-card-grid-compact.png`
- `reusable-assets/idea-card-grid-detail.png`

设计规则：

- 入营流程适合使用横向三阶段卡片，移动端改为纵向。
- 当前步骤使用蓝色渐变卡，未激活步骤使用白色弱化卡。
- 创业想法卡片使用浅蓝白背景，可带青色与黄色边框点缀。
- 创业想法提交入口在学员工作台中需要作为显著主行动。

## 14. 状态标签与评分

推荐状态色：

- 已完成 / 活跃：绿色。
- 进行中 / 当前：品牌蓝。
- 待修改 / 请假中 / 待确认：黄色或橙色。
- 风险 / 未报到 / 移除：红色。
- 已锁定 / 弱提示：灰色。
- 队伍和项目标签：蓝、紫、绿、青等低饱和背景。

设计规则：

- 标签使用胶囊或小圆角矩形。
- 状态文字保持短句，避免撑开表格列宽。
- 星级评分使用黄色星星 + 灰色未选中星星。

## 15. 图标系统

本包使用本地线性图标方案，避免离线打开时丢失 iconfont 外链。

相关文件：

- `html-pages/assets/icon-centering.css`
- `html-pages/assets/icon-replacements.js`

设计规则：

- 图标优先使用线性 SVG，风格接近 iconfont 线性图标。
- 图标容器统一水平垂直居中。
- `+`、`✓`、下拉箭头等文字图标由 `icon-replacements.js` 替换为 SVG。
- 按钮图标、步骤图标、标题图标不要出现偏上或偏左。

## 16. 推荐沉淀组件

- `BrandHeader`
- `LoginHeroPanel`
- `RegisterStepper`
- `RoleProfileCard`
- `SideListCard`
- `FeatureEntryCard`
- `MainPanel`
- `FilterBar`
- `DataTable`
- `StatusTag`
- `RoleBadge`
- `AppModal`
- `ModalTitle`
- `ReceiptDialog`
- `TeamMemberGrid`
- `UploadGrid`
- `RatingStars`
- `DayFlowTabs`
- `IdeaCard`
- `ReportMetricCard`

## 17. 维护规则

- 新增 HTML 页面时，页面文件放入 `html-pages/`。
- 页面运行必需素材放入 `html-pages/assets/`。
- 可复用视觉参考放入 `reusable-assets/`。
- 已确认整页设计稿放入 `confirmed-designs/`。
- 弹窗和局部状态设计稿放入 `component-states/`。
- 命名建议使用 `页面编号-页面名称-组件名称.png`，例如 `08-老师工作台-记录任务-个人记录弹窗.png`。
- 更新页面后，同步检查 `StartUpCampSaaS_Project_src/docs/设计稿-HTML-需求总索引.md`。
