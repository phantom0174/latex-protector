# About the repo

## Introduction

This is an auxiliary tool to facilitate the katex-rendering process of posts in hexo-based blogs.
For further information, see [this post](https://phantom0174.github.io/2023/01/lightweight_hexo_latex_rendering/) and [this post](https://phantom0174.github.io/2023/01/latex-protector/).

## Usage

```py
from latex_protector import Protector


target_folder_root = [
    "./source/_posts/",
    "./source/about/"
]

protector = Protector(target_folder_root)

protector.protect()
```

## Custom Syntax

Furthermore, you can enclose a section with two `<!--lp:skip-some-->` syntax to skip partial protection,
or add a `<!--lp:skip-all-->` syntax at the beginning of the file to skip the entire protection of the `md` file.

Examples:

```md
<!--lp:skip-some-->

$$
\text{This section will not be protected.}\\
A_i + B_j = C_k
$$

<!--lp:skip-some-->
```

```md
<!--lp:skip-all-->

This file will not be protected.

...
...
...

```
