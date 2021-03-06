# system-L
[![Stars](https://img.shields.io/github/stars/mbinary/system-L.svg?label=Stars&style=social)](https://github.com/mbinary/system-L/stargazers)
[![Forks](https://img.shields.io/github/forks/mbinary/system-L.svg?label=Fork&style=social)](https://github.com/mbinary/system-L/network/members)
[![Repo size](https://img.shields.io/github/repo-size/mbinary/system-L.svg)]()
[![License](https://img.shields.io/badge/LICENSE-MIT-blue.svg)](LICENSE)
[![Language](https://img.shields.io/badge/language-python3.5+-orange.svg)]()
[![build](https://github.com/mbinary/system-L/workflows/build/badge.svg)]()
[![Coverage](https://codecov.io/gh/mbinary/system-L/branch/master/graph/badge.svg)](https://codecov.io/github/mbinary/system-L?branch=master)


## Descripton
It's a formal logic deduction based on system-L
### Symbols
- `~`: negation
- `->`: deduce (denoted as '>')
### Axioms
The three basic axioms:
* L1: `p->(q->p)`
* L2: `(p->(q->r)) -> ((p->q)->(p->r))`
* L3: `~q->~p -> (p->q)`

### Deduction
`{p,p->q} |- q`

Read this [book](src/mathematical-logic.pdf) or click [here](https://en.wikipedia.org/wiki/Mathematical_logic) to see more details.

## Methods
To prove one proposition:
* Firstly, Use deduction theorem to de-level the formula and get a proposition variable or a proposition in form of `~(...)`. Let's denote it as `p` or `~p`.
* Next, Create a set called `garma` and fill it with some generated formulas which is deduced from the above axioms, some theorems and conclusions.
* Then, Search `p` or `~p` in `garma`, or further, using modus ponent(MP) to deduce  `p` or `~p`.
* Finally, if MP can't prove it, use `Proof by contradiction` instead.

## Requirements
python modules
* sympy

## Visual
![](src/sys-L.png)

## To do
* 将证明过程对象化,便于处理,打印(英文版,中文版),
* 其他连接词的转换
* 处理简单的, 有一定模式的自然语言, 形成命题推理

## Licence
[MIT](LICENCE)
