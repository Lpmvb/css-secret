---
id: irregular-drop-shadows
title: 不规则投影
---

<AUTOGENERATED_TABLE_OF_CONTENTS>

```playground
<style>
  body { margin: 0; display: flex; justify-content: center; flex-wrap: wrap; }
  .shadow {
    width: 120px; height: 120px; margin: 40px 30px; background: #fb3;
    position: relative;
    filter: drop-shadow(2px 2px 10px rgba(0,0,0,.5));
  }
  .shadow::before {
    content: '';
    position: absolute;
    width: 0; height: 0;
    top: 50%; right: -20px;
    transform: translateY(-50%);
    border: 22px solid transparent;
    border-left-color: #fb3;
    border-right-width: 0;
  }
</style>
<body>
  <div class="shadow"></div>
</body>
```