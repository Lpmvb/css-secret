---
id: simple-pie-charts
title: 简单的饼图
---

<AUTOGENERATED_TABLE_OF_CONTENTS>

```playground
<style>
  body { margin: 0; display: flex; justify-content: center; flex-wrap: wrap; }
  @keyframes spin {
    to { transform: rotate(.5turn); }
  }
  @keyframes bg {
    50% { background: #655; }
  }
  .pie {
    width: 120px; height: 120px; margin: 40px 30px;
    position: relative;
    border-radius: 50%;
    background: yellowgreen;
    background-image: linear-gradient(to right, transparent 50%, #655 0);
    text-align: center;
  }
  .pie:nth-of-type(1)::before {
    content: '';
    display: block;
    margin-left: 50%;
    height: 100%;
    border-radius: 0 100% 100% 0 / 50%; /* 右半圆 */
    background-color: inherit;
    transform-origin: left; /* 0 50% */
    transform: rotate(.1turn);
  }
  .pie:nth-of-type(2)::before {
    content: '';
    display: block;
    margin-left: 50%;
    height: 100%;
    border-radius: 0 100% 100% 0 / 50%; /* 右半圆 */
    background-color: inherit;
    transform-origin: left; /* 0 50% */
    transform: rotate(.1turn);
    animation: spin 3s linear infinite, bg 6s step-end infinite;
  }
  .pie:nth-of-type(3)::before {
    content: '';
    position: absolute;
    top: 0; left: 50%;
    width: 50%; height: 100%;
    border-radius: 0 100% 100% 0 / 50%;
    background-color: inherit;
    transform-origin: left;
    animation: spin 50s linear infinite, bg 100s step-end infinite;
    animation-play-state: paused;
    animation-delay: inherit;
  }
  .pie:nth-of-type(4) > svg {
  }
</style>
<body>
  <div class="pie"></div>
  <div class="pie"></div>
  <div class="pie" style="animation-delay: -60s">60%</div>
</body>
```