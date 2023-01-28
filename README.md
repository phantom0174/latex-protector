# About the repo

## Introduction

This is an auxiliary tool to facilitate the katex-rendering process of posts in hexo-based blogs.
For further information, see [this post](https://phantom0174.github.io/2023/01/lightweight_hexo_latex_rendering/).

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
