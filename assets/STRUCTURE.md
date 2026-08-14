# 诗往哥导航 — 项目结构文档（STRUCTURE.md）

> **维护说明**：本文档旨在帮助后续维护者快速理解导航站的分类逻辑、文件架构和更新规范。请在进行任何结构调整前先阅读本文档。


## 一、项目概述

### 1.1 这是什么？

诗往哥导航是一个基于 **Homer** 搭建的轻量级网址收藏夹，主要面向**学生、教师、职场新人**三大群体，聚合了教育学习、职业发展、工具资源、软件下载等优质链接。

### 1.2 核心架构原则

本项目采用 **“用户成长路径 + 功能工具分离 + 专业场景独立”** 的三层架构，具体为：

| 原则 | 说明 |
|------|------|
| **主线：用户成长阶段** | 按 `K12 → 大学 → 职场` 构建三个核心页面，用户根据自身阶段“对号入座” |
| **副线：工具与资源分离** | Web端在线服务（数字工具）与本地/客户端资源（资源软件）严格分离，避免认知混淆 |
| **支线：专业场景独立** | 教师群体的继续教育与备课需求高度特定，独立成页，不与普通用户混用 |


## 二、文件结构一览

```
/
├── config.yml                 # 主页（基础教育）—— K12 同步学习
├── higher-education.yml       # 高等教育 —— 大学/考研/留学/科普
├── career-development.yml     # 职业发展 —— 认证/技能/简历/面试
├── digital-tools.yml          # 数字工具 —— AI/开发/在线工具（Web服务）
├── resources-software.yml     # 资源软件 —— 系统/激活/APP（本地资源）
├── teacher-education.yml      # 教师教育 —— 继续教育/备课资源
└── STRUCTURE.md               # 本文档
```


## 三、各页面详细分类说明

### 3.1 `config.yml` — 主页（基础教育）

| 属性 | 值 |
|------|-----|
| **锚点** | `#` |
| **定位** | K12 学生同步学习与高考备考 |
| **目标用户** | 初中生、高中生、家长 |

**分类结构：**

| 分组名称 | 图标 | 内容说明 |
|----------|------|----------|
| 基础教育资源 | `fa-solid fa-school` | 课程标准（2022版/2017版）、电子教材平台、题库组卷网 |
| 高中语文 | `fa-solid fa-book` | B站语文名师（作文/阅读/素材） |
| 高中数学 | `fa-solid fa-calculator` | B站数学名师（基础/压轴/真题） |
| 高中英语 | `fa-solid fa-language` | B站英语名师（语法/续写/词汇） |
| 高中物理 | `fa-solid fa-atom` | B站物理名师（基础/专题突破） |
| 高中化学 | `fa-solid fa-flask` | B站化学名师（同步/一轮复习） |
| 高中生物 | `fa-solid fa-dna` | B站生物名师（零基础/技巧） |

**维护提醒**：新增学科资源请放入对应分组；若新增学科，请按现有命名规范（`"高中XX | XXXX"`）创建新组。


### 3.2 `higher-education.yml` — 高等教育

| 属性 | 值 |
|------|-----|
| **锚点** | `#higher-education` |
| **定位** | 大学生课程学习、考研升学、留学语言、学术科研、通识科普 |
| **目标用户** | 大学生、考研党、留学生、学术研究者 |

**分类结构：**

| 分组名称 | 图标 | 内容说明 |
|----------|------|----------|
| 大学升学规划 | `fa-solid fa-bullseye` | 志愿填报、院校信息、大学生活质量 |
| 考研备考资源 | `fa-solid fa-graduation-cap` | 考研规划、政治/英语/数学经验 |
| 大学课程学习 | `fa-solid fa-chalkboard-user` | 高数/线代/大物等大学基础课 |
| 学术科研技能 | `fa-solid fa-flask` | 论文检索、文献阅读、科研方法 |
| 学习方法与思维 | `fa-solid fa-brain` | 记忆法、学习状态、系统学习方法 |
| 大学生活指南 | `fa-solid fa-lightbulb` | 新生入学、避坑、人际关系 |
| 在线教育平台 | `fa-solid fa-laptop` | 慕课平台（中国大学MOOC/学堂在线等） |
| 留学与语言考试 | `fa-solid fa-language` | 四六级、雅思、托福备考 |
| 自然科学与通识 | `fa-solid fa-clapperboard` | 纯粹的自然科普（物理/生物/天文/植物） |


### 3.3 `career-development.yml` — 职业发展

| 属性 | 值 |
|------|-----|
| **锚点** | `#career-development` |
| **定位** | 职场技能认证、求职实战、职业规划 |
| **目标用户** | 应届毕业生、求职者、职场新人 |

**分类结构：**

| 分组名称 | 图标 | 内容说明 |
|----------|------|----------|
| 职业认证 | `fa-solid fa-certificate` | 教师资格证、公考（行测/申论/面试） |
| 实用技能 | `fa-solid fa-screwdriver-wrench` | PPT/Excel/PS/剪辑/EduEditer 等职场硬技能 |
| 人际交往 | `fa-solid fa-people-arrows` | 沟通技巧、关系处理、社会适应 |
| 职业规划 | `fa-solid fa-bullseye` | 目标设定、人生规划、职业方向 |
| 简历与面试 | `fa-solid fa-file-lines` | 简历撰写、自我介绍、面试问答 |

**维护提醒**：
- “实用技能”组已聚合了**所有软件教学视频**（含从资源软件移入的 Oeasy、doyoudo、菜鸟主老王）。新增软件教程请放此组。
- **语言考试类资源**（四六级/雅思/托福）请放入高等教育的“留学与语言考试”组，**勿放入此页**。


### 3.4 `digital-tools.yml` — 数字工具

| 属性 | 值 |
|------|-----|
| **锚点** | `#digital-tools` |
| **定位** | Web 端在线服务 — “打开即用，无需下载安装” |
| **目标用户** | 所有用户 |

**分类结构：**

| 分组名称 | 图标 | 内容说明 |
|----------|------|----------|
| 人工智能工具 | `fa-solid fa-robot` | AI 大模型（ChatGPT/DeepSeek/Kimi 等） |
| 开发与部署 | `fa-solid fa-code` | 代码托管（GitHub/Gitee）、云部署（Vercel/Cloudflare） |
| 编程开发学习 | `fa-solid fa-book` | 编程文档、在线教程、学习路线 |
| 在线实用工具 | `fa-solid fa-toolbox` | 翻译、图片压缩、图标库、正则测试等 |

**维护提醒**：
- **此页面仅放 Web 端在线服务**，需要下载安装的本地软件请放入 `resources-software.yml`。
- 区分标准：用户点击链接后是在浏览器中直接使用（Web），还是需要下载文件安装（本地）。


### 3.5 `resources-software.yml` — 资源软件

| 属性 | 值 |
|------|-----|
| **锚点** | `#resources-software` |
| **定位** | 本地客户端、系统镜像、激活工具、移动应用 — “需要下载安装或部署” |
| **目标用户** | 所有用户 |

**分类结构：**

| 分组名称 | 图标 | 内容说明 |
|----------|------|----------|
| 数字图书馆与电子书 | `fa-solid fa-book-open-reader` | 电子书资源库（Anna's Archive/Z-Library） |
| 影视与媒体资源 | `fa-solid fa-film` | TVBox、影视仓、音乐播放器、FTP |
| 系统与办公软件 | `fa-solid fa-download` | Windows/Office 原版镜像下载 |
| 软件激活 | `fa-solid fa-key` | KMS 激活、MAS 脚本、密钥分享论坛 |
| 综合软件与移动应用 | `fa-solid fa-box-open` | PC/Mac 软件下载站、移动端 APP 资源、论坛 |
| 生活服务 | `fa-solid fa-house-chimney` | 电商推广联盟（淘宝/京东/拼多多等） |


### 3.6 `teacher-education.yml` — 教师教育

| 属性 | 值 |
|------|-----|
| **锚点** | `#teacher-education` |
| **定位** | 教师专业发展 — 继续教育、研修培训、备课资源 |
| **目标用户** | 中小学教师、教育工作者 |

**分类结构：**

| 分组名称 | 图标 | 内容说明 |
|----------|------|----------|
| 教师继续教育 | `fa-solid fa-chalkboard` | 官方学分平台（国家平台/各省平台） |
| 教学资源 | `fa-solid fa-book-open` | 备课课件、教辅资料、学科网盘资源 |


## 四、导航栏统一规范

所有页面的顶部导航栏**必须保持一致**，包含以下 7 个链接：

```yaml
links:
  - name: "主页"          url: "#"
  - name: "高等教育"       url: "#higher-education"
  - name: "职业发展"       url: "#career-development"
  - name: "数字工具"       url: "#digital-tools"
  - name: "资源软件"       url: "#resources-software"
  - name: "教师资源"       url: "#teacher-education"
  - name: "网站源码"       url: "https://github.com/lss53/NavGuide"  target: "_blank"
```

**维护提醒**：如果新增页面，请在所有文件的 `links` 中同步添加对应条目。


## 五、更新操作指南

### 5.1 新增一个链接

1. **确定归属**：根据上述分类结构，确定新链接应放入哪个页面、哪个分组。
2. **编辑对应 YAML 文件**：在目标分组的 `items` 列表末尾添加新条目。
3. **格式规范**：

```yaml
- name: "显示名称"
  icon: "fab fa-bilibili"          # 或 fa-solid fa-xxx
  subtitle: "简短描述（不超过10字）"
  tag: "可选标签"                  # 如"大学数学""PC""Mobile"
  url: "https://完整链接"
  target: "_blank"                 # 外部链接必须加
  # quick:                         # 如有快捷入口，可添加
  #   - name: "名称"
  #     url: "链接"
  #     icon: "fa-solid fa-arrow-up-right-from-square"
  #     target: "_blank"
```

### 5.2 删除一个链接

1. 确认该链接无其他页面引用。
2. 从对应 YAML 文件中移除条目。
3. **请勿在 `quick` 中残留失效链接**。

### 5.3 移动链接到其他页面

1. 从原页面 YAML 中**完整复制**条目。
2. 粘贴到目标页面对应分组。
3. **删除原位置条目**（避免重复）。
4. 更新两个页面的注释说明。

### 5.4 新增一个分组

```yaml
- name: "分组名称 | English Name"
  icon: "fa-solid fa-xxx"          # 从 https://fontawesome.com/search 选取
  items:
    # 在此填入链接条目
```

**注意**：新增分组前请确认现有分类无法容纳，避免分类过细。

### 5.5 更换图标

1. 访问 [Font Awesome 图标库](https://fontawesome.com/search?ic=free)
2. 搜索所需图标，复制图标类名（如 `fa-solid fa-robot`）
3. 替换 YAML 中对应 `icon` 字段值


## 六、常用图标速查

| 场景 | 推荐图标 |
|------|----------|
| B站链接 | `fab fa-bilibili` |
| 外部链接/跳转 | `fa-solid fa-arrow-up-right-from-square` |
| 首页 | `fa-solid fa-home` |
| 教育/学校 | `fa-solid fa-school` / `fa-solid fa-graduation-cap` |
| 书/阅读 | `fa-solid fa-book` / `fa-solid fa-book-open` |
| 工具 | `fa-solid fa-tools` / `fa-solid fa-screwdriver-wrench` |
| 下载 | `fa-solid fa-download` |
| AI/机器人 | `fa-solid fa-robot` / `fa-solid fa-brain` |
| 代码/开发 | `fa-solid fa-code` / `fa-brands fa-github` |
| 语言 | `fa-solid fa-language` |
| 数学 | `fa-solid fa-calculator` |
| 物理 | `fa-solid fa-atom` |
| 化学 | `fa-solid fa-flask` |
| 生物 | `fa-solid fa-dna` |
| 电影/视频 | `fa-solid fa-film` / `fa-solid fa-clapperboard` |
| 音乐 | `fa-solid fa-music` |
| 密钥/激活 | `fa-solid fa-key` / `fa-solid fa-unlock` |
| 生活/购物 | `fa-solid fa-house-chimney` / `fa-solid fa-shopping-cart` |


## 七、版本历史

| 日期 | 版本 | 修改内容 |
|------|------|----------|--------|
| 2026-08-14 | v2.0 | 架构重构：语言考试移入高等教育；软件教程移入职业发展；科普视频独立更名；电商服务更名生活服务；全文件补充注释 |
| 2026-08-13 | v1.0 | 初始版本，六页面架构确立 |


## 八、相关资源

- **Homer 官方文档**：https://github.com/bastienwirtz/homer
- **Font Awesome 图标库**：https://fontawesome.com/search?ic=free
- **Bulma CSS 框架**：https://bulma.io/documentation/
- **本导航源码**：https://github.com/lss53/NavGuide

---

> **最后提醒**：在修改任何 YAML 文件前，请先用 `yamllint` 或编辑器插件检查语法格式（缩进、引号、冒号）。YAML 对缩进敏感，**请使用 2 个空格缩进**，不要混用 Tab。