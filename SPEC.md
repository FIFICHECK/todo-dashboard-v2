# Fiona Team To-Do Dashboard v2

**Project:** https://fificheck.github.io/todo-dashboard-v2/
**Repo:** FIFICHECK/todo-dashboard-v2
**Created:** 2026-06-11

## Overview

互動式 To-Do List Dashboard，採用交叉視圖 (Cross-view) 布局。

## Layout

- **橫向 (Columns):** 7 位 RM — Cat, Gary, Fi Fi, Jerry, Moses, Alvis, Knald
- **縱向 (Rows):** 3 個星期 — 上一週、呢一週、下一週
- **每格 (Cell):** 可加入多個工作項目，每項包含：
  - 工作描述文字
  - 可點擊之 URL Link
  - 剔選擇 ✅/☐（可點擊切換）

## Features

1. **動態加入工作** — 點擊「+ 加入工作」按鈕，彈出輸入框
2. **編輯/刪除工作** — 每項工作右側有編輯同刪除按鈕
3. **剔選擇** — ✅ 完成 / ☐ 未完成，狀態保存在 localStorage
4. **URL Link** — 可輸入網址，自動轉為可點擊連結
5. **週數導航** — 可切換睇唔同嘅三週組合
6. **本地存儲** — 所有數據保存在瀏覽器 localStorage，無需後端

## Data Structure

```javascript
{
  "tasks": {
    "2026-W24": {  // ISO week key
      "cat": [
        { "id": "uuid", "text": "工作描述", "url": "https://...", "done": false }
      ],
      "gary": [...],
      ...
    }
  }
}
```

## Tech Stack

- Pure HTML/CSS/JavaScript（無框架）
- localStorage 持久化
- GitHub Pages 托管
- Responsive design

## Team Members

1. Cat
2. Gary
3. Fi Fi
4. Jerry
5. Moses
6. Alvis
7. Knald

## Week Display Logic

- 自動計算今日所在週
- 顯示：上一週（W-1）、呢一週（W0）、下一週（W+1）
- 每週顯示為一列橫跨所有 RM
