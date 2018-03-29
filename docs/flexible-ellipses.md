---
id: flexible-ellipses
title: 自适应的椭圆
---

<AUTOGENERATED_TABLE_OF_CONTENTS>

```playground
<style>
  body { margin: 0; display: flex; justify-content: center; flex-wrap: wrap; }
  .ellipses {
    background: #fb3; width: 160px; height: 120px; margin: 20px 10px;
  }
  .ellipses:nth-of-type(1) { border-radius: 50%; }
  .ellipses:nth-of-type(2) { border-radius: 100px / 100px; }
  .ellipses:nth-of-type(3) { border-radius: 25px / 50px; }
  .ellipses:nth-of-type(3) { border-radius: 20px / 40px; }
  .ellipses:nth-of-type(4) { border-radius: 50% / 100% 100% 0 0; }
  .ellipses:nth-of-type(5) { border-radius: 50% / 100% 0; }
  .ellipses:nth-of-type(6) { border-radius: 100% 0 0 0; }
</style>
<body>
  <div class="ellipses"></div>
  <div class="ellipses"></div>
  <div class="ellipses"></div>
  <div class="ellipses"></div>
  <div class="ellipses"></div>
  <div class="ellipses"></div>
</body>
```

Tips:

> + 当任意两个相邻圆角的半径之和超过 border box 的尺寸时,用户代理必须按比例减小各个边框半径所使用的值,直到它们不会相互重叠为止。（因此 2 的半径最终缩减到 50px）
> + `50% / 50%` 分别指定圆角的水平和垂直半径， 每个值又可以写成四个值分别指定四个角， 从左上角开始按顺时针排列。

知识点：

> + [`border-radius`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-radius)