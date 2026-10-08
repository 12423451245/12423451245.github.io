---
title: 你好，世界：博客使用指南
date: 2026-10-08 12:00:00
tags:
  - 博客
  - 教程
categories:
  - 随笔
description: 博客搭好了！这篇文章演示了常用的写作功能，也是以后写文章的速查表。
mathjax: true
---

博客搭好了！这篇文章演示常用功能，写文章时可以回来对照。

## 发一篇新文章

在博客目录下运行：

```bash
npx hexo new "文章标题"
```

会在 `source/_posts/` 里生成 `文章标题.md`，编辑后提交并推送到 GitHub，一两分钟后网站就会自动更新。

本地预览：

```bash
npx hexo server
```

然后打开 http://localhost:4000 。

## 文章开头的设置

每篇文章最上面 `---` 之间的部分叫 front-matter：

```yaml
title: 标题
date: 2026-10-08 12:00:00
tags: [标签1, 标签2]
categories: [分类]
cover: https://图片地址.jpg   # 首页封面图
description: 首页显示的摘要
```

## 文字样式

**粗体**、*斜体*、~~删除线~~、`行内代码`、[链接](https://butterfly.js.org/)。

> 这是一段引用。

- 无序列表
- 第二项

1. 有序列表
2. 第二项

| 功能 | 状态 |
| --- | --- |
| 搜索 | ✅ |
| 深色模式 | ✅ |
| 目录 | ✅ |

## 提示块

{% note info flat %}
这是一个信息提示块。
{% endnote %}

{% note warning flat %}
这是一个警告提示块。
{% endnote %}

## 折叠内容

{% hideToggle 点我展开 %}
藏起来的内容在这里。
{% endhideToggle %}

## 代码

```python
def hello(name):
    print(f"你好，{name}！")

hello("世界")
```

## 数学公式

文章开头加上 `mathjax: true` 就能写公式。行内公式 $E = mc^2$，独立公式：

$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$

## 流程图

```mermaid
graph LR
  A[写 Markdown] --> B[git push]
  B --> C[GitHub Actions 构建]
  C --> D[网站更新]
```

## 标签页

{% tabs 示例 %}
<!-- tab 第一页 -->
第一页的内容
<!-- endtab -->
<!-- tab 第二页 -->
第二页的内容
<!-- endtab -->
{% endtabs %}

更多玩法见 [Butterfly 官方文档](https://butterfly.js.org/)。
