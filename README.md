# ml-primer — AI/ML 基础概念图解

AI / ML / LLM 基础概念的单文件 HTML 图解合集。目前的页面都由 `/eli5`(claude-community plugin)生成,但本目录按**内容**组织而非按工具 —— 任何形式的 AI/ML 基础材料都可以放进来。

每个 `.html` 都是自包含的(内联 CSS/JS,无本地资源依赖),直接双击即可打开。

## 页面

导航页:[index.html](index.html) —— 按「零件 → 架构 → 训练」分组,含推荐阅读顺序。

| 文件 | 标题 | 生成日期 |
|---|---|---|
| [attention-head.html](attention-head.html) | Attention 和 Head · 图解 | 2026-08-23 |
| [attention-paper.html](attention-paper.html) | Attention Is All You Need · 图解 | 2026-08-22 |
| [llm-training.html](llm-training.html) | LLM 训练 · 给懂推理的人 | 2026-08-22 |
| [residual-connections.html](residual-connections.html) | 残差连接 · 一个加号救了深度学习 | 2026-08-23 |
| [softmax.html](softmax.html) | Softmax · 一堆乱数 → 一组概率 | 2026-08-23 |
| [training-methods.html](training-methods.html) | LLM 训练方式全景 · 四段人生 | 2026-08-22 |

## 约定

- 新页面直接放这里,文件名用主题 slug(`<topic>.html`),不要建 `<topic>-eli5/` 子目录。
- `/eli5` 默认会往当前目录生成 `index.html`,**别让它覆盖导航页** —— 先让它写到别处或立刻重命名成 `<topic>.html`,然后更新上表和 `index.html` 的卡片。
- 内容页之间没有交叉链接,只由 `index.html` 汇总;各页仍可独立打开。

## 来源

2026-08-23 合并自 workdir 根下的 `attention-head-eli5/`、`attention-paper-eli5/`、`llm-training-eli5/`(原目录已删除)。
