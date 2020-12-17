# szuthesis

Shenzhen University Undergraduate Thesis

[![](https://github.com/liuchengxu/szuthesis/workflows/CI/badge.svg)](https://github.com/liuchengxu/szuthesis/actions?query=workflow%3ACI)

## 简介

论文主要关于推荐系统，重点研究在利用隐式反馈的推荐算法上如何融合内容信息, 算法模型为 `Bayesian Personalized Ranking + Content`，可以 [点击这里](https://liuchengxu.github.io/szuthesis/pdf/thesis.pdf) 查看论文. 

论文使用 LaTeX 撰写，对于 LaTeX 初学者撰写论文应当有一定借鉴意义.

- [src/thesis](https://github.com/liuchengxu/szuthesis/tree/gh-pages/src/thesis) 为论文的 LaTeX 工程目录, 源文件中给出了诸多注解。

- [src/dissertation_defence](https://github.com/liuchengxu/szuthesis/tree/gh-pages/src/dissertation_defence) 为答辩时使用的 slides, 详情请 [点击这里](https://liuchengxu.github.io/szuthesis/pdf/dissertation_defence.pdf).

在入门 LaTeX 的过程中，也积累了一些经验，新手或值得一看：

- [从零开始LaTeX快速入门](https://liuchengxu.github.io/blog-cn/posts/quick-latex/)

- [LaTeX实战经验:新手须知](http://blog.csdn.net/simple_the_best/article/details/51244631)

## 依赖项

安装 `texlive >= 2019`（详情请见 [TeX Live 的官方网站](https://tug.org/texlive/)）

## 构建

### latexmk

如果使用 `latexmk` 进行自动构建，执行以下命令

``` bash
cd src/thesis/
latexmk -xelatex main.tex
```

更多关于 `latexmk` 的信息可以参考 [这个入门指南](https://mg.readthedocs.io/latexmk.html) 或是 [latexmk 在 CTAN 上的主页](https://www.ctan.org/pkg/latexmk/)。

### 手动编译

如果想要手动编译，执行以下命令

``` bash
cd src/thesis/
xelatex main.tex
bibtex main.aux
xelatex main.tex
xelatex main.tex
```
