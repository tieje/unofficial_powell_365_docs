+++
title = "Setup for Contributors"
weight = 100
+++

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Local Repo Setup](#local-repo-setup)
- [Recommended VSCode Extensions](#recommended-vscode-extensions)

## Local Repo Setup

1. [Install Rust](https://www.rust-lang.org/tools/install)
   1. Add `~/wherever-it-is/.cargo/bin` to path.
2. [Install Zola](https://www.getzola.org/documentation/getting-started/installation)
   1. If you're on Windows or M1 Mac, I recommend building from source
      1. `git clone https://github.com/getzola/zola.git`
      2. `cd zola && cargo build --release`
      3. Add the resulting `zola` executable to path.
3. `zola serve`

## Recommended VSCode Extensions

```toml
Name: Markdown All in One
Id: yzhang.markdown-all-in-one
Description: All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
Version: 3.5.0
Publisher: Yu Zhang
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one
```
