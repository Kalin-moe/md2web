# md2web

> AI生成。本项目用于帮助我学习html。和部署个人网站。已经弃用。


## 工作方式

- `index.html` 通过 Fetch API 读取 `doc.md`
- [Showdown.js](https://github.com/showdownjs/showdown) 将 Markdown 转为 HTML
- 附带 CSS

## 使用

将`doc.md`和`index.html`放在同一目录

`index.html` 在启动时会fetch `doc.md` 然后转换为html

本地环境可能会收到浏览器安全功能影响

## Showdown.js

默认从 CDN 加载：

```html
<script src="https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js"></script>
```

离线使用：从 https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js 下载 `showdown.min.js` 到 `index.html` 同目录，并将 script 的 `src` 改为 `showdown.min.js`。

## 致谢

本项目使用 [Showdown.js](https://github.com/showdownjs/showdown)，基于 MIT License：

> MIT License  
> Copyright (c) 2018,2021 ShowdownJS  
> https://github.com/showdownjs/showdown

## 许可证

本项目自有代码采用 [Unlicense](https://unlicense.org/)，可自由使用、复制、修改、分发和销售。

Showdown.js 遵循其原始 MIT License。
