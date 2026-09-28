# IdeaVim 配置

个人 IntelliJ IDEA（IdeaVim）配置，基于 `<Space>` 作为 leader 键。

## 使用

将 `ideavimrc` 复制到用户目录并重命名为 `.ideavimrc`：

```bash
cp ideavimrc ~/.ideavimrc
```

改完后在 IDE 中执行 `:source ~/.ideavimrc` 生效。

## 主要特性

- **jk 映射 Esc**：插入模式下 `jk` 退出插入模式并触发 IDE Escape（关闭补全弹窗等）
- **输入法自动切换**：Normal 模式自动切英文，回到 Insert 恢复中文（需 IdeaVimExtension 插件）
- **书签**：`ma` 设置书签，`g1`-`g5` 跳转到对应书签
- **窗口操作**：`<leader>w` 系列管理编辑器分屏
- **IDE Action 映射**：
  - `<leader>a` Find Action，`<leader>c` 跳转类，`<leader>b` 书签列表
  - `gd` / `gi` / `gs` 跳转声明 / 实现 / 父方法
  - `U` 查找用法，`R` 重命名，`==` 格式化代码，`--` 优化导入
  - `,r` 运行，`,d` 调试，`,b` 切换断点
- **多光标**：`<C-n>` 选择下一处相同词，`<C-x>` 跳过，`<C-p>` 移除
- **补全与缩进**：Tab 在弹窗中接受补全，否则缩进

## 依赖插件（IdeaVim 内置功能开关）

```vim
set easymotion
set surround
set argtextobj
set multiple-cursors
set exchange
set highlightedyank
set textobj-entire
set NERDTree
set ReplaceWithRegister
```

`keep-english-in-normal-and-restore-in-insert` 需要安装 [IdeaVimExtension](https://plugins.jetbrains.com/plugin/9615-ideavim-extension) 插件。
