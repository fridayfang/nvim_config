## 我的neovim 配置

### 基础配置
1. 禁用了上下左右的按键，连续输入jk作为<esc>
2. `h,j,k,l`作为基础的移动`f`可以进行搜索式的移动,`b,w`可以进行word级别的移动
3. `leader`键映射为,
4. 如何进行复制，粘贴：
    - 从normal模式进入visual模式(按v/V)
    - `h,j,k,l`移动来选定操作区域(选中区域会光标高亮)
    - y表示复制，p表示粘贴
5. 如何进行简单的搜索:
    - 从normal模式输入/就能进行搜索
    - 然后输入想要搜索的文本，enter光标会停在第一个匹配的地方，然后可以进行编辑
感觉上述5个操作可以满足简单的快速文本编辑的功能

`map` 命令可以查看所有快捷键的映射
### 插件列表

比较好用的插件：
- `nerdtree`(<F3>启动)\
\<C-w-w\> 可以在`nerdtree`和打开文件的buffer切换\
\<Leader\>1 可以切换到第一个buffer
- `nerdcommenter`(,ci)
- `auto-pair`(比coc-pair好用)
- `markdown-preview`(支持即改即显示，快捷键,m)
- `coc-vim`(包括相关coc插件，支持LSP方式补全\
安装`coc-clangd`支持clangd的补全(先要安装c`clangd`)\
需要较好效果的补全需要:
1.  `compile_command.json`, 通过cmake 根据CMakeLists.txt生成
2.  在`.bashrc/.zshrc`中加入`CPLUS_INCLUDE_PATH`(加入需要搜索的头文件目录),这样可以自动补全include头文件
- `floaterm`(轻松进入终端，可以查看执行结果而不用退出nvim)\
,ft 开启一个新终端\
,fh 隐藏终端

- `vim-surround` 轻松对文本增减括号\
normal mode: \ 
`ds'`: 去除''\
`cs'[`: 改'为[\
`ysw"`:对光标单词加""\
`yss"`:对整行加""\

vision mode: \

选中文本(`v/V`), 按S[:文本加上[]
## 最终效果:
![](./nvim.png)


