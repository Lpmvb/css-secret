---
id: blinking
title: 闪烁效果
---

<AUTOGENERATED_TABLE_OF_CONTENTS>

```playground
<style>
  @keyframes blink-smooth {
    50% { color: transparent }
  }
  body { margin: 0; display: flex; justify-content: center; flex-wrap: wrap; }
  .blinking {
    margin: 40px 30px;
    font-family: Consolas, Monaco, monospace; /* 等宽字体 */
  }
  .blinking:nth-of-type(1) {
    animation: 2s blink-smooth infinite;
  }
  .blinking:nth-of-type(2) {
    animation: 1s blink-smooth infinite steps(1);
  }
</style>
<body>
  <h1 class="blinking">CSS is awesome!</h1>
  <h1 class="blinking">CSS is awesome!</h1>
</body>
```
