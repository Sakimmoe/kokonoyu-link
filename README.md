# 九重紫 · 链接页

- 在线：https://sakimmoe.github.io/kokonoyu-link/
- 仓库：https://github.com/Sakimmoe/kokonoyu-link

`index.html` 是主页面：顶部直接用 `home.jpg` 原图（不裁剪），名字和一行小字在图下方，下面是白色胶囊按钮。
`preview.html` 是预览页，可以看另外五个备选版本（01–05）。

---
# 九重紫 · 链接页（说明）

粉色调、亮色系。整页背景用桌面上的 `home.jpg`：完整铺满屏宽（`background-size:100% auto`），不做任何裁剪；原图四周的白底已刷成同色粉，所以图片和页面背景无缝衔接。宽屏下最大铺到 1400px 宽、居中。链接资料取自 [kokonoyu.com](https://www.kokonoyu.com/)。

| 文件 | 方案 | 一句话 |
| --- | --- | --- |
| `01-cover.html` | 封面卡 | 白卡浮在粉底上，头图当封面，头像压在卡片边缘 |
| `02-hero.html` | 满幅 | 头图铺满整幅，粉色面板从下面接上来 |
| `03-postcard.html` | 明信片 | 头图拍成明信片，纸胶带 + 落款印 + 手写体 |
| `04-split.html` | 分屏 | 桌面左边粉色人物区、右边白底链接；手机自动上下排 |
| `05-tiles.html` | 贴纸墙 | 彩色磁贴按钮，B 站蓝、直播粉、YouTube 橘、X 炭黑 |

`index.html` 是五个方案的预览页（手机框并排），点框或「打开」进单页。

## 本地预览

```powershell
# 在 kokonoyu-linktree 目录下
D:\node.exe serve.js
# 打开 http://127.0.0.1:19388/
```

纯静态，也可以直接双击 `index.html`。手机宽度 390px 左右最舒服。

## 说明

- 单文件 HTML，样式全部内联；引用 `assets/images/` 下的 `bg-full.jpg`（`home.jpg` 去掉白边，画面未裁切）、`home.jpg`、`avatar.webp`、`favicon.png`。
- 字体统一用 **Resource Han Rounded CN**（资源圆体，OFL 授权），放在 `assets/fonts/RHR-CN.woff2`：
  只子集了页面用到的 406 个字符，保留 200–900 可变字重，一个文件 235KB，不依赖任何 CDN。
  字体来源和重新子集的方法写在 `assets/fonts/README.txt`。
- 每页 15 个链接：哔哩哔哩、直播间 9162799、YouTube、X、爱发电、FANBOX、BOOTH，加站内八个（主页、紫记、同传、作品、音乐、画廊、历程、留言板）。
- 头像、插画版权归九重紫及合作画师所有，这里只是非官方整理。

## 改字

链接都在 `<a href="...">` 里，文案直接改文本。主色在每页开头的 `:root` 里：`--rose`（强调色）、`--ink`（正文色），浅色变量看名字就能分辨。头图尺寸 1620×580，换图时保持这个比例最稳。
