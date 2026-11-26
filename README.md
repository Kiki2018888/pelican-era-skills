# 鹈鹕时代技能

鹈鹕时代技能可以在 Codex 中独立安装，用 20 种时代画风制作动画。给 Agent 一段动作和一个画风名，它会编写角色、道具和时间轴，再按选定的画法绘制。用同一段动作比较多种画风时，可以暂停在同一帧切换。[在线大画面演示 · 机器人打羽毛球](https://kiki2018888.github.io/pelican-era-skills/)

## 安装和使用

把 `pelican-era-skills` 克隆到个人技能目录下的 `pelican-era-film` 文件夹，即可用 `$pelican-era-film` 调用。

```sh
git clone https://github.com/Kiki2018888/pelican-era-skills.git "$HOME/.agents/skills/pelican-era-film"
```

更新已有安装时，先确认安装目录名为 `pelican-era-film`，目录内直接包含 `SKILL.md`。在 Codex 中可以这样调用。

> 用 $pelican-era-film 做一段纸船松绳过桥的动画。先用浮世绘，再用唐代白描，让我停在同一帧切换两种画风。

也可以在仓库根目录用 Node.js 22 或更高版本直接生成离线 HTML。

```sh
node scripts/style-scene.mjs list
node scripts/style-scene.mjs build --scene examples/paper-boat.js --style 浮世绘 --style 唐代白描 --out out/boat.html
```

双击 `out/boat.html` 可播放。导出 PNG 需要 Chrome 或 Chromium，导出静音 MP4 还需要 FFmpeg。[场景编写、按画风导出和关键帧验收](references/scene-authoring.md) · [可修改的动作样例](examples) · [20 套画风规则](assets/medium/styles.json)

## 原作与许可

画风顺序和部分画材算法取自 Elbert 的《鹈鹕测试》（Pelican Test，MIT）。原片的主体是骑自行车的鹈鹕。这个改编提取了各分场的画法，为新题材增加了通用规则、场景接口、离线播放器和导出工具。每种画风都注明了上游源文件和函数。[原作仓库](https://github.com/orbitoo/pelican-test) · [采用的固定提交](https://github.com/orbitoo/pelican-test/tree/59c8ca2657ce5b2cf067969b5bda19d6609af8ac) · [上游 MIT 许可](references/upstream/LICENSE) · [第三方声明](THIRD_PARTY_NOTICES.md) · [本项目 MIT 许可](LICENSE)
