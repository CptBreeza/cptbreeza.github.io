---
title: CSS 学习
---

# 1. 选择器

## 1.1 attribute 选择器

1. 具有 `a[href]`
2. 相等 `a[href="/posts"]`
3. 包含 `a[href*="posts"]`
4. 开头 `a[href^="https"]`
5. 结尾 `a[href$=".org"]`
6. 多个 `a[href^="https"][href$=".org"]`

## 1.2 类选择器

1. 直接使用 `.class-name`
2. 限定标签 `a.class-name`
3. 多个 `a.class-a.class-b`

## 1.3 id 选择器

1. 直接使用 `#id-a`

## 1.4 & 选择器

1. 没有 & 时，嵌套解释为父子 `nav { a { color: red; }}`
2. 有 & 时，& 被解释为 parent（这句和上面等效） `nav { & a { color: red; }}`
3. 没有 & 时，嵌套解释为父子 `a { :hover { color: white; }}` 会被解释为
   `a *:hover { color: white; }`
4. 有 & 时，& 被解释为 parent `a { &:hover { color: white }}`

## 1.5 关系选择器

1. 接邻兄弟选择器 `p + a { color: red; }`
2. 子选择器 `p > a { color: red; }`
3. 后代选择器 `p a { color: red; }`
4. 兄弟选择器（只选它后面的） `p ~ a { color: red; }`

## 1.6 选择器列表

1. 多个选择器共用一套样式 `a,p,h1 { color: red; }`

## 1.7 状态类伪类

1. 常用于按钮按下时 `:active`
2. 选项被选择时 `:checked`
3. 有效/无效 `:enabled`/`:disabled`
4. 获得焦点时 `:focus`
5. 鼠标悬浮时 `:hover`
6. 有效/无效时（input、form 等）`:valid`/`:invalid`
7. 必填的 `:required`
8. 目标（URL 中的 fragmnent 指向的元素） `:target`
9. 链接被访问过 `:visited`

## 1.8 关系型伪类

1. `:first-child`/`:last-child`
2. `:first-of-type`/`:last-of-type`
3. `:nth-child(n)`
4. `:nth-of-type(n)`
5. `:nth-last-child(n)`
6. `:nth-last-of-type(n)`
7. `:only-child`
8. `:only-of-type`

## 1.9 功能型伪类

1. `:has(+ p)`

## 1.10 伪类元素

1. `::before`/`::after`
2. `::first-letter`/`::first-line`
3. `::placeholder`
4. `::selection`
