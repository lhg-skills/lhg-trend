# lhg-trend · 近 30 天热点扫描

训练数据和通用搜索引擎对"正在发生的事"天然滞后。这个 skill 用多源并行搜索 + 真实互动热度排序 + 健康检查诚实降级，回答"这个话题近 30 天到底火不火、为什么火、还能不能追"。

**双模式**：主题模式（给定主题深挖近 30 天讨论）/ 发现模式（扫榜单提名 5–10 个按热度排序的候选话题，可直接投喂 lhg-benchmark-topic-factory 做选题库）。

**触发**：用户说"最近有什么热点""这话题最近火吗""帮我看看近一个月的讨论""选题灵感""热点扫描"，或任何"某主题 + 最近/近30天/这阵子"类请求时自动触发。

**方法借鉴**：`mvanhorn/last30days-skill`（MIT License）。本 skill 为独立重写（中文优先、平台中立、增加中文信源与选题模式），非原项目翻译或分支。

## 安装

- 一键安装：`npx skills add lhg-skills/lhg-trend`
- 通用：将本仓库放到各平台的 skill 目录（如 `~/.agents/skills/lhg-trend/`，注意 SKILL.md 须在目录根）。
- Coze：扣子编程 → 导入项目 → 本地上传本仓库 zip（SKILL.md 须在 zip 根目录；`.skill` 后缀由导入后生成，不要只改扩展名）。
- Trae：设置 → 技能 → 上传技能（zip 根目录含 SKILL.md；国区版路径 `~/.trae-cn/skills/`）。
- 平台无关：本 skill 写法平台中立（联网搜索/抓取全文/只读子 agent/任务清单），不依赖任何单一生态的专有工具名。

## 自检与反馈

本 skill 每次执行后自动做一次轻量自检；只有发现疑似自身缺陷时，才运行 `references/smoke-test.md` 标准用例并输出质检报告。报告经你确认后，可一键向 GitHub 提交 `[QC]` issue（模板见 `.github/ISSUE_TEMPLATE/qc-report.md`）。

## 版本

- 1.0.0（2026-09-29）：首版。双模式（主题/发现）+ 三层信源 + 30 天硬窗口 + 诚实降级纪律 + 冒烟脚本；方法借鉴 mvanhorn/last30days-skill（MIT）。

## 出品：刘洪光

本 skill 由真人出镜 IP「刘洪光」（安徽合肥）出品，归属 [lhg-skills](https://github.com/lhg-skills)。

- GitHub 主页：https://github.com/lhg-skills —— 全部 skill 开源在此，欢迎 star
- 视频号：搜「刘洪光实名上网」
- 微信：lhgsmsw
