### 推荐好用的插件

* [AutoFileName][1]
* [BracketHighlighter][3]
* [Color Highlighter][7]
* [HTML-CSS-JS Prettify][4]
* [Emmet][5]
* [DocBlockr][6]
* [MarkdownHighlighting][8]
* [Sass][2]
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
* [SublimeLinter-eslint][22]
* [SublimeLinter-tslint][23]
* [Sublime​Linter-annotations][24]

### Default (OSX).sublime-keymap

对 `macOS` 下的一些快捷键的重新绑定。

### bh_core.sublime-settings

对 `BracketHighlighter` 插件做的一些修改。

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

### AdvancedNewFile

当有多个项目在一个窗口的时候，每次建立文件都是以第一个为主，修改如下属性后，就能新建的时候在当前项目的文件下。

```json
{
  "default_root": "current"
}
```

### GitGutter

可以在编辑文件中实时监测显示 *git 文件* 的修改状态，如果升级了 *git* 注意修改当前的版本，防止没有提示。

```json
{
  "git_binary": "${your_git_path}"
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

### Nodejs

```json
{
  "node_path": "${your_node_path}"
}
```

### SublimeLinter

其他语法格式检测工具依赖于这个，所以在 `Settings - User` 里的 `"linters"` 需要添加如下内容：

```json
{
  "eslint": {
    "disable": false,
    "args": [],
    "excludes": [
      "**/node_modules/**"
    ],
    "env": {
      "PATH": "${your_node_bin_path}"
    }
  },
  "tslint": {
    "disable": false,
    "args": [],
    "config_filename": "tslint.json",
    "excludes": [
        "**/node_modules/**"
    ],
    "env": {
      "PATH": "${your_node_bin_path}"
    }
  },
  "annotations": {
    "disable": false,
    "args": [],
    "errors": [
      "FIXME",
      "TODO",
      "@todo"
    ],
    "excludes": [],
    "warnings": [
      "NOTE",
      "README",
      "XXX"
    ],
    "env": {
      "PATH": "${your_node_bin_path}"
    }
  },
}
```

`"styles"` 修改如下：

```js
[
  {
    // Used to determine the color. E.g. region.<colorish>, with one of
    // redish, orangish, yellowish, greenish, bluish, purplish, pinkish.
    "scope": "region.yellowish markup.warning.sublime_linter",

    // The error type this style definition will match for.
    // An array which can contain "warning" and/or "error".
    // If omitted will match both.
    "types": ["warning"]
  },
  {
    // Determines, for overlapping errors, which one is visualised.
    "priority": 1,

    // The icon displayed in the gutter area
    // - "circle", "dot" or "bookmark"
    // - "none" to remove the icon
    // - A path to an icon file like
    //   "Packages/SublimeLinter/gutter-themes/Blueberry Cross/error.png"
    // - One provided by a gutter theme (e.g. "warning" or "error").
    //   In theme Default: warning, error, cog, x,
    //   and diamond, heart, pointer, square, star, triangle, which all
    //   also have an -outline variant.
    "icon": "dot",

    // The highlight style:
    // - "none"
    // - "fill", "outline",
    // - "solid_underline", "squiggly_underline", "stippled_underline"
    // The underline styles are replaced with outlines when there is
    // whitespace in the problem region, because underlines aren't drawn
    // on whitespace (ST issue #137).
    "mark_style": "solid_underline",

    "scope": "region.redish markup.error.sublime_linter"
  }
]
```

### 喜欢的主题

* *Monokai*

<!-- Links -->

[1]: https://github.com/BoundInCode/AutoFileName
[2]: https://github.com/braver/SublimeSass
[3]: https://github.com/facelessuser/BracketHighlighter
[4]: https://github.com/victorporof/Sublime-HTMLPrettify
[5]: https://github.com/sergeche/emmet-sublime
[6]: https://github.com/spadgos/sublime-jsdocs
[7]: https://github.com/Monnoroch/ColorHighlighter
[8]: https://github.com/braver/MarkdownHighlighting
[11]: https://github.com/SublimeCodeIntel/SublimeCodeIntel
[12]: https://github.com/skuroda/Sublime-AdvancedNewFile
[13]: https://github.com/babel/babel-sublime
[14]: https://github.com/tanepiper/SublimeText-Nodejs
[15]: https://github.com/davidrios/jade-tmbundle
[16]: https://github.com/vuejs/vue-syntax-highlight
[18]: https://github.com/Microsoft/TypeScript-Sublime-Plugin
[19]: https://wbond.net/sublime_packages/sftp
[20]: https://github.com/jisaacks/GitGutter
[21]: https://github.com/SublimeLinter/SublimeLinter
[22]: https://github.com/SublimeLinter/SublimeLinter-eslint
[23]: https://github.com/SublimeLinter/SublimeLinter-tslint
[24]: https://github.com/SublimeLinter/SublimeLinter-annotations
