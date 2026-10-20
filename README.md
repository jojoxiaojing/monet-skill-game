# 莫奈花园散步 · Promenade chez Monet

一个在浏览器里玩的横版小游戏：穿紫色裙子的小女孩走进莫奈的三幅画，沿路收集发光的罂粟、紫藤和夕光，走到画架前，这次散步就成了一幅画。

> **本作由 [huashu-art-motion](https://github.com/alchaincyf/huashu-art-motion) skill 生成。**
> 这个 skill 由花叔（[@alchaincyf](https://github.com/alchaincyf)）开发，用代码画出各种艺术风格的动画。游戏的莫奈画法和「主角从左走到右、穿过一幅幅画」的结构都来自它。

![罂粟田](screenshot-poppy.png)

## 三幅画

| 画 | 年份 | 收集 |
|---|---|---|
| 罂粟田（Les Coquelicots） | 1873 | 五朵发光的罂粟，走过去她会弯腰摘下 |
| 睡莲池上的日本桥（Le Pont japonais） | 1899 | 五串低垂的紫藤，要跳起来才够得着 |
| 干草堆，日落（Meules, soleil couchant） | 1891 | 五束夕光，有的要先跳上草堆 |

![日本桥](screenshot-bridge.png)
![干草堆](screenshot-stacks.png)

## 怎么玩

- 键盘：`←` `→` 或 `A` `D` 走，`空格` / `↑` 跳
- 手机：按住屏幕下方的箭头走，点「跳」；横屏更好看

直接用浏览器打开 `index.html` 就能玩，不需要安装任何东西。整个游戏是一个 HTML 文件，没有图片素材，画面全部由代码画出。

## 从 skill 里用到了什么

- **莫奈画法**（`references/风格配方/28_monet.md`）：先平涂底稿，再按区域色板用短笔触重画。水面横笔，草地竖笔，远景房子单独用细笔再画一遍。
- **每格独立种子的笔触重画**（`demos/long_scroll/lib/crossing.js` 的 `XING.strokes`）：笔触位置固定，不会每帧乱闪。
- **长卷穿越结构**（`references/11-长卷穿越片.md`）：每幅画是一段横向长卷，跨边界时下一幅画用笔触一笔一笔盖过来。
- **画要一直是活的**：水面光斑在闪，睡莲随涟漪起伏，柳条和紫藤在摆，罂粟会被她走过时推开。
- **角色和画风同一套**（`references/角色精细度.md`）：小女孩也用同一套莫奈笔触画，帽檐下有一层冷紫色的彩色阴影，进入日落那幅画会被染成暖色。

## 署名

- 画法与结构：[huashu-art-motion](https://github.com/alchaincyf/huashu-art-motion)，作者花叔
- 灵感来源：克洛德·莫奈（Claude Monet）的《罂粟田》《睡莲池上的日本桥》和干草堆系列
- 游戏由 Claude 用上述 skill 制作
