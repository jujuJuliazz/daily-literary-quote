# 每日古典名句

一个安静、适合手机阅读的静态小站：每天展示一则**中国古典公有领域**名句。

线上地址：[https://jujujuliazz.github.io/daily-literary-quote/](https://jujujuliazz.github.io/daily-literary-quote/)

## 简介

- 纯静态：`index.html`、`style.css`、`quotes.json`，无需构建。
- 名句保存在 [`quotes.json`](quotes.json)。
- 按 **亚洲/上海（UTC+8）** 日历日取「年内第几天」，再以 `(day-of-year − 1) mod N` 选择名句，同一天所有访客看到同一则。

## 版权说明

仅收录中国古典文献中已进入公有领域的原文短章，例如：

- 《论语》《孟子》《庄子》《道德经》
- 《诗经》《楚辞》
- 《古文观止》所选古文
- 《世说新语》《菜根谭》
- 唐诗、宋词等名篇（作者去世已久，文本本身公版）

不含外国著作的现代受版权译文，也不含仍在版权保护期内的现当代作品。页脚声明仅供参考，**不构成法律意见**。

每条包含：原文、篇名/书名、作者（或佚名）、来源说明（如「公有领域」）。

## 如何添加名句

1. 打开 `quotes.json`。
2. 追加如下对象：

```json
{
  "text": "短句原文。",
  "book": "篇名或书名",
  "author": "作者或佚名",
  "note": "公有领域"
}
```

3. 请确认确属公有领域后再添加；保持一两句至四句为佳。
4. 提交并推送到 `main` 后，GitHub Pages 会自动更新轮换池（`N` 为数组长度）。

## 本地预览

```bash
python3 -m http.server 8080
```

浏览器打开 `http://localhost:8080`。

## 部署

GitHub Pages 从 `main` 分支根目录发布。
