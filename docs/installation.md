# Installation

## Command-line & language server

unlike pyright, the basedpyright CLI & LSP are available as a [pypi package](https://pypi.org/project/basedpyright/) instead of an npm package.

this makes it far more convenient for python developers to use, since there's no need to install any additional tools. just install it normally via your package manager of choice:

<!-- tabs:start -->

### **pdm**

```
pdm add basedpyright
```

### **rye**

```
rye add basedpyright
```

### **uv**

```
uv pip install basedpyright
```

### **pip**

```
pip install basedpyright
```

<!-- tabs:end -->

once installed, the `basedpyright` and `basedpyright-langserver` scripts will be available in your python environment. when running basedpyright via the command line, use the `basedpyright` command:

```shell
basedpyright --help
```

for instructions on how to use `basedpyright-langserver`, see the [IDE-specific instructions below](#ides).

## IDEs

most of these IDE plugins require [the pypi package to be installed](#command-line--language-server).

### VS Code
install the extension from [the vscode extension marketplace](https://marketplace.visualstudio.com/items?itemName=detachhead.basedpyright) or [the open VSX registry](https://open-vsx.org/extension/detachhead/basedpyright)

### Neovim
BasedPyright is available through the [`nvim-lspconfig`](https://github.com/neovim/nvim-lspconfig/blob/master/doc/server_configurations.md#basedpyright) adapter for native Neovim's LSP support.  TL;DR simply add this to your Neovim's settings:
```lua
local lspconfig = require("lspconfig")
lspconfig.basedpyright.setup{}
```
Further info for this LSP server options for `nvim-lspconfig` are available on their docs, linked above.

### Vim

Vim users can install [coc-basedpyright](https://github.com/fannheyward/coc-basedpyright), the BasedPyright extension for coc.nvim.

### Sublime Text

Sublime text users can install both [LSP](https://packagecontrol.io/packages/LSP) and [LSP-basedpyright](https://packagecontrol.io/packages/LSP-basedpyright) via [Package Control](https://packagecontrol.io).

### Emacs
*⚠ basedpyright has not been tested on this editor. if you run into issues with these instructions, please raise an issue.*

Emacs users can install [eglot](https://github.com/joaotavora/eglot) or [lsp-mode](https://github.com/emacs-lsp/lsp-mode) with [lsp-pyright](https://github.com/emacs-lsp/lsp-pyright).

### PyCharm

### If using Community edition
install [pyright-for-pycharm](https://plugins.jetbrains.com/plugin/24145)

configure it to use basedpyright by specifying the path to the `basedpyright` executable:

![image](https://github.com/DetachHead/basedpyright/assets/57028336/b373a5ee-c423-4b94-b833-00b5335a9611)

### If using Professional edition
intsall [pyright-langserver-for-pycharm](https://plugins.jetbrains.com/plugin/24146-pyright-language-server). This plugin makes use of PyCharm's experimental [LSP API](https://plugins.jetbrains.com/docs/intellij/language-server-protocol.html).

configure it to use basedpyright by specifying the path to the `basedpyright-langserver` executable:

![image](https://github.com/DetachHead/basedpyright/assets/57028336/4ee471ad-68cb-410e-8b67-81c57f4bb80b)
