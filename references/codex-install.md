# 在 Codex 中安装鹈鹕时代技能

使用 Git 安装时，在终端执行下列命令。Windows 可使用 PowerShell，macOS 和 Linux 可使用系统终端。

## 在多个项目中使用

```sh
git clone https://github.com/Kiki2018888/pelican-era-skills.git "$HOME/.agents/skills/pelican-era-film"
```

## 只在一个项目中使用

在项目根目录打开终端，运行下面的命令。

```sh
git clone https://github.com/Kiki2018888/pelican-era-skills.git .agents/skills/pelican-era-film
```

## 从 ZIP 安装

在 [GitHub 仓库首页](https://github.com/Kiki2018888/pelican-era-skills)选择 **Code → Download ZIP**。解压后，将含有 `SKILL.md` 的文件夹改名为 `pelican-era-film`。把这个文件夹放进个人主目录或项目根目录下的 `.agents/skills/`。安装后的目录结构如下。

```text
.agents/skills/pelican-era-film/
├── SKILL.md
├── agents/
├── assets/
├── examples/
├── references/
└── scripts/
```

## 开始使用

在 Codex 的技能列表中选择 **鹈鹕时代技能**，或在提示词里输入 `$pelican-era-film`。如果列表里没有出现这项技能，检查 `SKILL.md` 的位置，然后重新打开 Codex。

> 用 $pelican-era-film 做一个 5 秒的唐代白描动画。一只松鼠推开窗，把松果放上窗台。

制作动画需要 Node.js 22 或更高版本。观看生成的 HTML 只需浏览器。[使用说明](../使用说明.md)
