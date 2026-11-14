# Der Ring des Nibelungen · 尼伯龙根的指环

瓦格纳《尼伯龙根的指环》唱词三语对照本：德文原文、英文译本、中文译本，LaTeX 排版，A5 开本。

目前完成第一部《莱茵的黄金》（Das Rheingold）。

## 目录

```
.
├── README.md
└── Das-Rheingold/
    ├── Das-Rheingold-Libretto-de.tex   # 德文原文
    ├── Das-Rheingold-Libretto-en.tex   # 英文译本
    ├── Das-Rheingold-Libretto-zh.tex   # 中文译本
    ├── Das-Rheingold-Libretto-de.pdf
    ├── Das-Rheingold-Libretto-en.pdf
    └── Das-Rheingold-Libretto-zh.pdf
```

三个版本按同一结构排列：人物表、场次、角色名、舞台指示、唱词逐行对应，便于对照阅读。

## 构建

需要 TeX Live（含 `tgpagella`、`ctex`、`fandol` 等宏包）。

```bash
cd Das-Rheingold

# 德文、英文
pdflatex Das-Rheingold-Libretto-de.tex
pdflatex Das-Rheingold-Libretto-de.tex
pdflatex Das-Rheingold-Libretto-en.tex
pdflatex Das-Rheingold-Libretto-en.tex

# 中文（ctexbook，需 XeLaTeX）
xelatex Das-Rheingold-Libretto-zh.tex
xelatex Das-Rheingold-Libretto-zh.tex
```

跑两遍是为了目录页码稳定。

## 翻译说明

- 德文底本为瓦格纳原脚本。
- 英文为逐行工作译本，尽量保留原句的句法与头韵。
- 中文以“信、达、雅”为原则；韵文按中文语感重新断句，不逐字硬译。
- 莱茵河女儿的无词呼喊（`Weia! Waga! Wallala...`）按声音功能译为“喂呀／哗啦／嘿呀”，不采用“韦亚／瓦加”这类容易被读成人名的音译。
- 舞台指示统一用灰色斜体排出，与唱词区分。

## 状态

- [x] Das Rheingold / 莱茵的黄金
- [ ] Die Walküre / 女武神
- [ ] Siegfried / 齐格弗里德
- [ ] Götterdämmerung / 诸神的黄昏

## 许可

瓦格纳的德语脚本已进入公有领域。英文、中文译文及排版版权归本项目作者所有；如需转载或再分发，请先联系。若希望以开源许可证发布，可在上传前补一个 `LICENSE`。

## English

A trilingual edition of Wagner's *Der Ring des Nibelungen* libretto — German original, English translation, and Chinese translation — typeset in LaTeX (A5). *Das Rheingold* is complete; the remaining three operas are planned.

Build with `pdflatex` for the German and English editions, and `xelatex` for the Chinese edition (`ctexbook`). See the commands above.

Translation note: the Rhinemaidens' wordless cries are rendered as Chinese sound-words (喂呀／哗啦／嘿呀) rather than name-like transliterations.
