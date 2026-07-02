# StartUPCAMP SYS

少年马斯克创业营系统的在线项目资料站，也是 `StartUpCampSaaS_Project_src` 主工程的产品资料入口。

## 正式文档体系

当前资料站首页展示 6 份正式 Markdown 文档、1 个需求池管理页和 1 个 UI/UX 设计图库：

| 文档 | 作用 |
| --- | --- |
| `00-总产品文档.md` | 唯一正式产品主线，融合旧终极文档、四视角梳理和关键规则确认。 |
| `10-用户端V1.0基础方案产品需求说明.md` | 学员、家长、老师用户端基础业务闭环。 |
| `11-用户端V1.1运营优化产品说明.md` | 结合现有 HTML 原型与代码反推的用户端运营优化需求。 |
| `20-后台V1.0基础方案产品需求说明.md` | 后台基础管理需求。 |
| `21-后台V1.1基础方案产品需求说明.md` | 后台营地上下文、招生、日程、记录、AI、看板等优化需求。 |
| `requirements.html` | 需求池管理与版本排期，可增删改查，并支持 Markdown 导入、复制和下载。 |
| `40-工程文档.md` | 源码结构、UUID 规则、API 模块、权限原则。 |
| `design-system.html` | 可直接查看设计稿、组件状态、截图和可复用视觉资产。 |

旧的重复文档已移动到 `docs/archive-legacy/`，只作为历史追溯，不作为正式需求入口。

## 目录关系

```text
StartupCampSaaS_Design/
├── StartUPCAMP_SYS/                 # 在线项目资料站
│   ├── index.html                   # 项目中枢：首页、开发计划、需求池入口
│   ├── requirements.html            # 需求池管理与版本排期
│   ├── requirements-data.js         # 需求池基线数据
│   ├── doc.html                     # Markdown 文档阅读页
│   ├── design-system.html           # UI/UX 设计图库
│   └── docs/                        # 正式文档 + archive-legacy 历史归档
└── StartUpCampSaaS_Project_src/     # SaaS 主工程源码
```

## 本地预览

直接在浏览器中打开 `index.html` 即可。`doc.html` 已内置 `docs-data.js`，支持 `file://` 本地打开 Markdown 文档。需求池请使用 `requirements.html`，页面修改会保存在当前浏览器，并可导出为 Markdown。
