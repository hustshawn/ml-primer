# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 这是什么

AI / ML / LLM 基础概念的**单文件 HTML 图解**合集，用来沉淀学习 AI/ML 过程中的基础知识。没有构建系统、没有依赖、没有测试 —— 只有一堆能直接双击打开的 `.html`。

主分支 `main`。仓库里只有内容文件，所有路径引用都用相对路径。

## 命令

只有一个：

```bash
open <topic>.html        # macOS 直接用浏览器打开，无需 server
```

## 新增一页的流程

1. `/eli5 <topic>`（claude-community plugin）在**当前目录**生成 `index.html`
2. 重命名为 `<topic>.html`（主题 slug，扁平放在本目录根，**不要**建 `<topic>-eli5/` 子目录）
3. 更新 `README.md` 的页面表格：文件、标题、生成日期

`README.md` 的表格就是本仓库的索引；目前没有 `index.html` 导航页，页面之间也**没有交叉链接**。

## 页面架构（6 个页面共享，改动/新增时照抄）

### 硬约束：完全自包含

每个 `.html` 都是 `<style>` + markup + `<script>` 内联在一个文件里，**零外部请求** —— 没有 CDN、没有 KaTeX/MathJax、没有图表库、没有本地资源引用。公式用 HTML/CSS 排出来（`.mono` 类），图表用 div/grid/flex 手搓，箭头和流程图偶尔用内联 `<svg>`。新增页面必须保持这个性质：双击就能看。


## 内容约定

- **读者画像**：已经懂推理 / 会用 API 的工程师（见 `llm-training.html` 的 kicker「给已经懂推理的你」），不是完全的新手。所以可以直接用 logits、KV cache、量化这类词，但必须把训练侧、数学侧的概念拆到最小。
- 小节标题写成**主张或反问**（「为什么非得套个 e？」「A 不是参数」），不要写成「3. 温度参数」这种目录式标签。
- 大多数页面末尾有一张**名词对照表 / 翻译表**，把新概念映射到读者已知的东西。
- 数字、公式、显存/算力账都要给具体值，不要「很大」「更快」。已经写在页面里的实测数字（如各家 API 的 temperature 上限、论文 Table 3-E 的 BLEU）是有来源的，不要改成估算值。
