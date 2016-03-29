# 编辑器配置


## Atom
安装 atom 插件

- [linter][1]
- [linter-eslint][2]
- [linter-stylelint][3]

`apm install editorconfig linter linter-eslint linter-stylelint`

或者通过`Packages->Settings View->Install packages/Themes`搜索上面的包名进行安装

安装插件后需要重启atom

## Sublime Text
安装 Sublime Text 插件

打开"Package Control: Install Package" (Ctrl+Shift+P),安装下列插件

- [EditorConfig][4]
- [Babel][5]
- [Sublime-linter][6]
- [SublimeLinter-contrib-eslint][7]
- [SublimeLinter-contrib-stylelint][8]

对于部分特殊的扩展需要将 babel 作为默认的语法

- 使用这个扩展打开一个`.js`文件
- 从菜单栏选择`View`
- 然后选择`Syntax -> Open all with current extension as... -> Babel -> JavaScript (Babel)`
- 对于其它的扩展重复上面的步骤


  [1]: https://atom.io/packages/linter
  [2]: https://atom.io/packages/linter-eslint
  [3]: https://atom.io/packages/linter-stylelint
  [4]: https://packagecontrol.io/packages/EditorConfig
  [5]: https://packagecontrol.io/packages/Babel
  [6]: https://packagecontrol.io/packages/SublimeLinter
  [7]: https://packagecontrol.io/packages/SublimeLinter-contrib-eslint
  [8]: https://packagecontrol.io/packages/SublimeLinter-contrib-stylelint
