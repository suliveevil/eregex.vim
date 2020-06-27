# eregex.vim

在 Vim 中使用 Perl 风格的正则表达式

## 安装

推荐使用 Vim 8 内置包管理系统和 Git 进行安装。

也可以通过第三方包管理工具 vundle vim-plug dein 等进行安装。


## 快速开始

### 搜索

安装之后，只需像往常一样按下 <kbd>/</kbd> 或 <kbd>?</kbd>。

这两个键都将映射为 `:M/` 命令，此时你可以开始使用 PCRE 正则表达式来进行搜索。

你可以通过调用 `eregex#toggle` 函数来开启或关闭本插件的键盘映射。

你可以在你的`.vimrc` 中这样设置：

    nnoremap <leader>/ :call eregex#toggle()<CR>

然后你就可以使用 <kbd><leader>/</kbd> 来开启或关闭 eregex.vim。

### 替换

使用 `:%S//` (大写字母 S) 触发 perl 风格的正则表达式替换。

更多信息见 `:help eregex` 。

## 配置

如果要默认不使用本插件，在你的 `.vimrc` 中写入：

    let g:eregex_default_enable = 0

将默认搜索分隔符 `/` 和 `?`改为其他，则可以这样设置：

    let g:eregex_forward_delim = '/'
    let g:eregex_backward_delim = '?'

设置像 perl 正则表达式一样默认大小写敏感：

    let g:eregex_force_case = 1

你可以通过修饰符 `/i` 随时改变这个设置。

## Changes

### 2.62

* Support ignorecase, smartcase. Add force case sensitive mode.

### 2.61

* Support for ignorecase

### 2.60

* Support for the backword search.
* Support for the count argument.
* Use function to auto map keys.
* Support for custom search delimeters.
* hlsearch works fine.

## License

Author     : 安久津  
Origin     : [eregex.vim][origin]  
Maintainer : othree  

See `:help eregex-license-to-use` for license information.

[origin]:http://www.vector.co.jp/soft/unix/writing/se265654.html
