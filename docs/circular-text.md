---
id: circular-text
title: 环形文字
---

<AUTOGENERATED_TABLE_OF_CONTENTS>

```playground
<style>
  @keyframes circular-text-rotate {
    to { transform: rotate(1turn); }
  }
  body { margin: 0; display: flex; justify-content: center; flex-wrap: wrap; }
  .text {
    width: 160px; height: 160px; margin: 40px 30px;
  }
  .text svg {
    overflow: visible;
    animation: circular-text-rotate 5s linear paused infinite;
  }
  .text svg:hover {
    animation-play-state: running;
  }
  .text path {
    fill: none;
  }
  .text text {
    fill: #75836e;
  }
</style>
<body>
  <div class="text">
    <svg viewBox="0 0 100 100">
      <path d="M 0,50 a 50,50 0 1,1 0,1 z" id="circle" />
        <text>
          <textPath xlink:href="#circle">
            circular reasoning works because because becau
          </textPath>
        </text>
    </svg>
  </div>
</body>
```

> + [svg path](https://developer.mozilla.org/zh-CN/docs/Web/SVG/Tutorial/Paths)