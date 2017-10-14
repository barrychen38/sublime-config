### 推荐好用的插件

* [AutoFileName][1]
* [Brackets Highlighter][3]
* [HTML-CSS-JS Prettify][4]
* [Emmet][5]
* [DocBlockr][6]
* [MarkdownHighlighting][8]
* [SCSS][9]
* [SublimeCodeIntel][11]
* [AdvancedNewFile][12]
* [Babel][13]
* [Nodejs][14]
* [Jade.tmbundle][15]
* [PlainTasks][16]
* [TypeScript][18]
* [SFTP][19]
* [GitGutter][20]
* [SublimeLinter][21]
* [SublimeLinter-contrib-eslint][22]
* [SublimeLinter-contrib-tslint][23]

### 快捷键的重新绑定

主要包含了 `macOS` 和 `Windows` 下的快捷键。

### bh_core.sublime-settings

对 `Brackets Highlighter` 插件做的一些修改。

### Default.sublime-settings

对修改 `Tab` 的一些颜色修改，还是喜欢原来的样式。

### SFTP

可以免费试用，但是会有弹窗出来提示你购买，所以在网上找了一个万能 *Key*，放在 `SFTP -> Settings - User` 里就好。

```json
{
  "email": "xiaosong@xiaosong.me",
  "product_key": "d419f6-de89e9-0aae59-2acea1-07f92a"
}
```

### GitGutter

可以在编辑文件中实时监测显示 *git 文件* 的修改状态，如果升级了 *git* 注意修改当前的版本，防止没有提示。

```json
{
  "git_binary": "/usr/local/bin/git"
}
```

以下代码可以自定义边框的符号颜色，作者已经配好了颜色，追求高度审美的程序猿可以考虑自行配色。

```html
<dict>
  <key>name</key>
  <string>GitGutter deleted</string>
  <key>scope</key>
  <string>markup.deleted.git_gutter</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#F92672</string>
  </dict>
</dict>
<dict>
  <key>name</key>
  <string>GitGutter inserted</string>
  <key>scope</key>
  <string>markup.inserted.git_gutter</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#A6E22E</string>
  </dict>
</dict>
<dict>
  <key>name</key>
  <string>GitGutter changed</string>
  <key>scope</key>
  <string>markup.changed.git_gutter</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#967EFB</string>
  </dict>
</dict>
<dict>
  <key>name</key>
  <string>GitGutter ignored</string>
  <key>scope</key>
  <string>markup.ignored.git_gutter</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#565656</string>
  </dict>
</dict>
<dict>
  <key>name</key>
  <string>GitGutter untracked</string>
  <key>scope</key>
  <string>markup.untracked.git_gutter</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#565656</string>
  </dict>
</dict>
```

### TypeScript

需要多开一个功能：

```json
{
  "enable_typescript_language_service": true
}
```

### SublimeLinter

其他语法格式检测工具依赖于这个，所以在 `Settings - User` 里的 `"linters"` 需要添加如下内容：

```json
{
  "eslint": {
    "@disable": false,
    "args": [],
    "excludes": []
  },
  "tslint": {
    "@disable": false,
    "args": [],
    "config_filename": "tslint.json",
    "excludes": [
        "**/node_modules/**"
    ]
  }
}
```

`"paths"` 修改如下：
```json
{
  "linux": [],
  "osx": [
    "/Users/barry/.nvm/versions/node/v6.11.3/bin"
  ],
  "windows": []
}
```

> 使用 nvm 才会有效，所以填写的 nvm 下 node 的目录

### 喜欢的主题

* [Dracula][10]
* *Monokai*

[1]: https://github.com/BoundInCode/AutoFileName	
[3]: https://github.com/facelessuser/BracketHighlighter
[4]: https://github.com/victorporof/Sublime-HTMLPrettify
[5]: http://emmet.io/
[6]: https://github.com/spadgos/sublime-jsdocs
[8]: https://github.com/braver/MarkdownHighlighting
[9]: https://github.com/MarioRicalde/SCSS.tmbundle
[10]: http://zenorocha.github.io/dracula-theme/
[11]: https://github.com/SublimeCodeIntel/SublimeCodeIntel
[12]: https://github.com/skuroda/Sublime-AdvancedNewFile
[13]: https://babeljs.io/
[14]: https://github.com/tanepiper/SublimeText-Nodejs
[15]: https://github.com/davidrios/jade-tmbundle
[16]: https://github.com/vuejs/vue-syntax-highlight
[18]: https://github.com/Microsoft/TypeScript-Sublime-Plugin
[19]: https://wbond.net/sublime_packages/sftp
[20]: https://github.com/jisaacks/GitGutter
[21]: https://github.com/SublimeLinter/SublimeLinter3
[22]: https://github.com/roadhump/SublimeLinter-eslint
[23]: https://github.com/lavrton/SublimeLinter-contrib-tslint