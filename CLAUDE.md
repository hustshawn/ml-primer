# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 这是什么

AI / ML / LLM 基础概念的**单文件 HTML 图解**合集，用来沉淀学习 AI/ML 过程中的基础知识。没有构建系统、没有依赖、没有测试 —— 只有一堆能直接双击打开的 `.html`。

主分支 `main`。仓库里只有内容文件，所有路径引用都用相对路径。

## 命令

只有一个：

```bash
open index.html          # 导航页
open <topic>.html        # 单页；macOS 直接用浏览器打开，无需 server
```

## 新增一页的流程

1. `/eli5 <topic>`（claude-community plugin）在**当前目录**生成 `index.html` —— ⚠️ `index.html` 在本目录是**导航页**，别让 `/eli5` 覆盖它。先确认它没被写坏，或者让它生成到别处再搬进来。
2. 重命名为 `<topic>.html`（主题 slug，扁平放在本目录根，**不要**建 `<topic>-eli5/` 子目录）
3. 在 `index.html` 里加一张卡片，放进对应的分组。只需要写 `href` 和 `data-sections="<该页小节数>"` —— 卡片脚注的文件名和组序号由页尾脚本从卡片算出，**不要手填任何数字**

`index.html` 是**唯一**的页面索引 —— `README.md` 故意不列页面清单，这样加页只需要动一处。内容页之间**没有交叉链接**，每页仍可单独打开。

## 唯一的硬约束：完全自包含

每个 `.html` 都是 `<style>` + markup + `<script>` 内联在一个文件里，**零外部请求** —— 没有 CDN、没有 KaTeX/MathJax、没有图表库、没有本地资源引用。双击就能看，断网也能看。

**除此之外没有任何规定。** 版式、配色、结构、图表画法、行文口吻，每页按主题自己发挥 —— 这份文件不提供风格指导，也不要往里加。

## 改现有页面时

已经写在页面里的具体数字（各家 API 的 temperature 上限、论文里的 BLEU 等）是有来源的，不要改成估算值或想当然的数。
