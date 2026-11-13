# 2026-11-v2 · 旧版主页存档

这一页留着，是因为主页上说「我会改、会撤回」。撤回的东西也在。

- **存档对象**：tag [`profile-v2`](../../../../peishenglai3-hash/tree/profile-v2)
- **对应的提交**：`8baf46d`（2026-11-06T05:21:21Z，`profile: v2 cover and editorial layout (赖选 · 主页号)`）
- **存档内容**：那一版的 `README.md` 原文，逐字未改（BOM 除外），与同目录的旧封面 `cover-2026-11.png`

## 这一版当时的样子

一页静态图文：一张封面、五件正在做的事、一张 mermaid 方法图、一段边界。没有动效，也没有能动手的东西。

## 旧资源去哪了

| 路径 | blob | 现状 |
|---|---|---|
| `assets/cover-2026-11.png` | `653c9d4` | 移进本目录，改名 `cover-2026-11.png` |
| `assets/field.png` | `ab79528` | 从 `main` 删除（全仓无人引用，是孤儿） |
| `assets/field.svg` | `2dff672` | 从 `main` 删除（同上） |

删除只是从 `main` 上消失，历史里都在。取回任意一个：

```bash
git show profile-v2:assets/field.svg > field.svg
```

本目录里的 `README.md` 仍指向旧的绝对地址
`.../main/assets/cover-2026-11.png`，那个地址现在 404——
封面就在本目录里，要看直接打开 `cover-2026-11.png`。

## 怎么整个退回去

```bash
git checkout profile-v2 -- README.md assets/cover-2026-11.png
# 或者整个工作树回到那一版（会丢弃当前改动，先 stash）
git switch --detach profile-v2
```
