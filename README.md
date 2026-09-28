# 每日古典名句

一个安静、适合手机阅读的静态小站：每天展示一则**中国古典小说**公有领域原文短章。

线上地址：[https://jujujuliazz.github.io/daily-literary-quote/](https://jujujuliazz.github.io/daily-literary-quote/)

## 简介

- 纯静态：`index.html`、`style.css`、`quotes.json`，无需构建。
- 名句保存在 [`quotes.json`](quotes.json)。
- 按 **亚洲/上海（UTC+8）** 日历日取「年内第几天」，再以 `(day-of-year − 1) mod N` 选择篇章，同一天所有访客看到同一则。
- 每则约 **80–160 字**，相当于一小段可读的小说原文，而非单句摘抄。

## 版权说明

仅收录中国古典白话/文言小说中已进入公有领域的原文，例如：

- 《红楼梦》《西游记》《水浒传》《三国演义》
- 《儒林外史》《聊斋志异》
- 《镜花缘》《老残游记》《官场现形记》

不含外国著作现代译文，也不含仍在版权保护期内的现当代作品。页脚声明仅供参考，**不构成法律意见**。

每条包含：原文、书名与回目、作者、来源说明（公有领域）。

## 如何添加篇章

1. 打开 `quotes.json`。
2. 追加如下对象（建议 80–160 字）：

```json
{
  "text": "小说原文短段……",
  "book": "书名·第×回",
  "author": "作者",
  "note": "公有领域 · 古典小说原文"
}
```

3. 请确认确属公有领域后再添加。
4. 提交并推送到 `main` 后，GitHub Pages 会自动更新轮换池。

## 本地预览

```bash
python3 -m http.server 8080
```

浏览器打开 `http://localhost:8080`。

## 部署

GitHub Pages 从 `main` 分支根目录发布。
