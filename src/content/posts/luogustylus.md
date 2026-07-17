---
title: 分享一下我洛谷的stylus样式
published: 2026-07-17
description: 分享一下我洛谷的stylus样式
tags: [前端,stylus,css]
category: 前端开发
draft: false
---

``` css
body {
    background: url("https://img.cdn1.vip/i/6a10e0d61d1e4_1779491030.webp") fixed center / cover no-repeat !important;
}

/* 极浅的全屏遮罩（略微压暗背景） */
body::before {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0);
    pointer-events: none;
    z-index: 9997;
}

/* 主要内容区域透明背景 */
.lfe-body,
.lfe-main,
.lfe-app,
.main-container,
.content-container,
.lfe-content,
.card,
.panel,
.box,
.panel-body,
.panel-heading,
.container,
.row > div,
[class*="card"],
[class*="panel"] {
    background-color: rgba(0, 0, 0, 0) !important;
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.08);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

/* 题目内容区域稍微深一点，方便阅读 */
.problem-content,
.problem-card,
.lfe-problem,
.article-content,
.markdown-body {
    background-color: rgba(0, 0, 0, 0.25) !important;
    border-radius: 20px;
    padding: 1.2rem;
}

/* 代码块透明背景 */
pre,
code,
.hljs,
.lfe-code-block {
    background-color: rgba(0, 0, 0, 0.2) !important;
    border-radius: 12px;
}

/* 文字、图标、按钮：透明背景 + 白色文字 */
p, span, h1, h2, h3, h4, h5, h6, li, a, label, small, strong, b, em, i,
code, pre, button, .btn, input, select, textarea,
.icon, .fa, .fas, .far, .fab, svg {
    background: transparent !important;
    color: #ffffff !important;
    border-color: rgba(255, 255, 255, 0.3);
}

/* 链接颜色醒目 */
a {
    color: #FFDD88 !important;
    text-decoration: underline;
    text-underline-offset: 3px;
}
a:hover {
    color: #FFB347 !important;
}

/* 按钮样式 */
button, .btn, .lfe-button, [role="button"], input[type="submit"], input[type="reset"] {
    background: rgba(20, 30, 45, 0.6) !important;
    border: 1px solid rgba(255, 200, 100, 0.8) !important;
    color: #FFF3DF !important;
    border-radius: 40px !important;
    font-weight: 500;
    transition: 0.2s;
    padding: 6px 18px;
}
button:hover, .btn:hover {
    background: rgba(0, 0, 0, 0.7) !important;
    border-color: #FFB347 !important;
    transform: scale(1.02);
}

/* 输入框样式 */
input, select, textarea {
    background: rgba(0, 0, 0, 0.3) !important;
    border: 1px solid rgba(255, 215, 120, 0.7) !important;
    border-radius: 24px !important;
    padding: 8px 14px;
    color: #fff0 !important;
}
input:focus, textarea:focus, select:focus {
    background: rgba(0, 0, 0, 0.55) !important;
    border-color: #F4A261 !important;
    outline: none;
    box-shadow: 0 0 0 2px rgba(244, 162, 97, 0.3);
}

/* 表格样式 */
table, .table {
    background-color: transparent !important;
}
th, td {
    background: rgba(0, 0, 0, 0.2) !important;
    border: none;
    color: #F5F5F5;
    padding: 12px;
    border-radius: 14px;
}
th {
    background: rgba(0, 0, 0, 0.45) !important;
}

/* 导航栏透明 */
.navbar, .header, .lfe-header, .top-bar {
    background: rgba(0, 0, 0, 0.2) !important;
}

/* 滚动条样式 */
::-webkit-scrollbar {
    width: 6px;
    background: rgba(0, 0, 0, 0.2);
}
::-webkit-scrollbar-thumb {
    background: rgba(200, 180, 140, 0.6);
    border-radius: 12px;
}

/* 洛谷特定元素覆盖 */
.lfe-main-container,
.lfe-sidebar,
.lfe-problem-sidebar,
.lfe-ranking-table,
.lfe-discuss-list {
    background-color: rgba(0, 0, 0, 0) !important;
}

/* 竞赛/作业面板透明 */
.lfe-contest-card,
.lfe-homework-card {
    background-color: rgba(0, 0, 0, 0.15) !important;
}

/* 题解区域透明 */
.solution-content,
.comment-area {
    background-color: rgba(0, 0, 0, 0.2) !important;
}
body .header-layout.tiny[data-v-7ddab1d5]{
    background: rgba(0,0,0,0) !important;
}
body .lg-article, .lg-article-sub, .lg-article-nctrl{
    background: rgba(0,0,0,0.2) !important;
}
.am-comment-bd{
    background: rgba(0,0,0,0.2) !important;
}
.am-comment-hd{
    background: rgba(0,0,0,0.4) !important;
}
main[data-v-f265fec6]{
    background-color: rgba(0,0,0,0) !important;
}
nav[data-v-a119941e]{
    background: rgba(0,0,0,0) !important;
}
.bottom-wrap.float[data-v-1dd53196]{
    background: rgba(0,0,0,0.2) !important;
}
.combo-wrapper > .text[data-v-dbc33c63]{
    background: rgba(0,0,0,0) !important;
}
.category ul.luogu[data-v-c6a940aa]{
     background: rgba(0,0,0,0) !important;
}
.lcolor-bg-background{
    background: rgba(0,0,0,0) !important;
}
.user-header-bottom[data-v-0403faa2]{
    background-color: rgba(0,0,0,0) !important;
}
.swal2-popup{
    background-color: rgba(0,0,0,0) !important;
}
.user-nav[data-v-8a6f9694]{
    background: rgba(0,0,0,0.2) !important;
}
.center[data-v-1a591deb]{
    background: rgba(0,0,0,0.2) !important;
}
.casket.cs-main{
    background: rgba(0,0,0,0.2) !important;
}
.casket .cs-header{
    background: rgba(0,0,0,0.2) !important;
}
.ͼ2 .cm-gutters{
     background: rgba(0,0,0,0.2) !important;
}
.user-header-bottom[data-v-3c374c4c]{
    background: rgba(0,0,0,0.2) !important;
}

```

关于浏览器stylus拓展的安装，请自行查阅相关文章