# 紫尘阁 · 三衡生活 · 文献库

> 大医派紫尘阁 · 项目战略文献库

公开网址：https://wjpvip-cloud.github.io/sanheng/

## 文件结构

```
sanheng-site/
├── index.html                          首页（9 个文档入口 + 归档链接）
│
├── docs/                               主文档区
│   ├── strategy-v3.html       ★ 当前主干 · 战略主干 v3.0
│   ├── community.html         01 共同体战略
│   ├── structure.html         02 双主体整合
│   ├── roadmap.html           03 完整落地计划
│   ├── handbook.html          04 品牌手册 2.0
│   ├── scenes.html            05 书院内容场景地图
│   ├── tools.html             06 三工具分工方案
│   ├── prompts.html           07 AI 9 个岗位提示词
│   └── volunteers.html        08 义工战略仪表盘
│
├── archive/                            历史归档（不在主页突出展示）
│   ├── v1_master_strategy.html         早期英文版
│   ├── v1_strategic_plan_zh.html       中文化版
│   ├── v2_upgraded_strategy.html       已验证阶段诊断版
│   ├── v2_brand_ai_team.html           里斯品类+AI团队
│   └── v2_brand_draft_2_0.html         品牌战略底稿
│
└── README.md
```

## 文档关系

**战略层 vs 执行层**

- `strategy-v3.html` 是战略主干当前版本，整合自 archive/ 下 5 份原始迭代版本
- `community / structure / roadmap` 三份是更早的战略文档，与 v3 互为参照
- `handbook / scenes / tools / prompts / volunteers` 五份是执行手册，每天打开就能用

**何时看哪份？**

| 场景 | 看这份 |
|------|--------|
| 第一次了解项目 | strategy-v3 |
| 想做内容选题 | handbook + prompts |
| 想拍书院短视频 | scenes |
| 想搭 AI 工作流 | tools + prompts |
| 想激活义工 | volunteers |
| 想理解共同体的本质 | community |
| 处理法律/合规问题 | structure |
| 团队搭建/里程碑 | roadmap |

**品牌名规范**

- 母品牌（运营方、法律主体、师承）：**紫尘阁**
- 对外接触点（用户接触、课程名、生活方式倡导）：**三衡生活**
- 双层一起出现：**紫尘阁 · 三衡生活** 或 **大医派紫尘阁 · 三衡生活**

## 后续怎么继续加文档？

### 加新的主文档

1. 把新 HTML 放进 `docs/` 文件夹（文件名用英文）
2. 在 `index.html` 的「Part I 战略」或「Part II 执行」区域里加一个 `<a class="doc">` 入口（参考现有写法）

### 加新的归档版本

1. 把旧版本放进 `archive/`，文件名建议用 `v{版本号}_{描述}.html` 格式
2. 在 `index.html` 页脚的 footer-archive 部分加上链接
3. 在归档文件顶部记得加一条「此文档已归档」的提示栏

## 部署/更新方式

### 方法 A · 网页直接传

1. 进入仓库 → **Add file** → **Upload files**
2. 拖新文件进去 → Commit
3. 1-2 分钟后网址自动更新

### 方法 B · GitHub Desktop（推荐长期用）

下载 https://desktop.github.com，clone 仓库到本地。以后改文件就在本地改，改完 Commit + Push 即可。

## 后续方向

**想换自己的域名**：买完域名（如 `sanheng.life`），在域名服务商加 CNAME 指向 `wjpvip-cloud.github.io`，仓库 Settings → Pages → Custom domain 填上即可。GitHub Pages 免费提供 HTTPS。

**想加访问统计**：推荐 [Umami](https://umami.is/)（隐私友好，免费）。

**对外开放时**：去掉子页面顶部"内部"字样、改首页 hero 文案、加"如何加入"入口。这是品牌从内部期进入对外期的标志。
