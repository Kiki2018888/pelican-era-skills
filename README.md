# 鹈鹕时代技能

给 Codex 一段动作，再选一种画风，就能得到一段可以离线播放的动画。比如让一只螃蟹横穿石头、举起左钳，可以用爪哇皮影画出转动的关节，也可以用浮世绘画出它的轮廓。把两种画风放在同一个播放器里，暂停后切换，螃蟹会停在同一个姿势。[先看机器人羽毛球的 20 种画风](https://kiki2018888.github.io/pelican-era-skills/)

## 安装

在终端运行下面的命令，将技能添加到 Codex。制作动画需要 Node.js 22 或更高版本。

```sh
git clone https://github.com/Kiki2018888/pelican-era-skills.git "$HOME/.agents/skills/pelican-era-film"
```

也可以下载 ZIP，或只为一个项目安装。[其他安装方式](references/codex-install.md)

## 做第一段动画

在 Codex 中输入这句话，动作、画风和画幅都可以换。

> 用 $pelican-era-film 做一段横屏动画。一只松鼠推开窗，把松果放上窗台。用唐代白描画一版，再加一版浮世绘，让我暂停在松鼠松手的那一帧切换画风。

写 HTML 前，可以沿用角色设定图，也可以用生图工具画出「前爪托着松果」和「松手后松果留在窗台上」两个姿势。动画写好后，拖过松手的时刻，对照爪尖在哪里离开松果、前臂转动时有没有被拉长，再调整场景代码。[用关键姿势对照图检查造型](references/scene-authoring.md#可选的造型与姿势对照图)

打开生成的 HTML 即可播放。把这个文件发给别人，对方用浏览器就能看。想继续改动作，可以编辑随动画交付的场景代码。[使用说明与导出方法](使用说明.md)

## 试跑纸船示例

从技能目录执行下面的命令，再用浏览器打开 `out/boat.html`。

```sh
cd "$HOME/.agents/skills/pelican-era-film"
node scripts/style-scene.mjs build --scene examples/paper-boat.js --style 浮世绘 --style 唐代白描 --out out/boat.html
```

[查看两段示例的源码](examples) · [查看 20 种画风](assets/medium/styles.json) · [编写自己的场景](references/scene-authoring.md)

## 原作与许可

20 种时代画风的顺序和部分画笔算法来自 Elbert 的《鹈鹕测试》（Pelican Test，MIT）。原片描绘一只骑自行车的鹈鹕。鹈鹕时代技能把这些画法用到新的角色和动作上，并提供场景接口、播放器和导出工具。[原作仓库](https://github.com/orbitoo/pelican-test) · [采用的原作版本](https://github.com/orbitoo/pelican-test/tree/59c8ca2657ce5b2cf067969b5bda19d6609af8ac) · [上游 MIT 许可](references/upstream/LICENSE) · [第三方声明](THIRD_PARTY_NOTICES.md) · [技能包 MIT 许可](LICENSE)
