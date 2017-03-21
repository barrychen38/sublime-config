#### 推荐好用的 Sublime Text 插件

* [AutoFileName][1]
* [Brackets Highlighter][3]
* [JsFormat][4]
* [Emmet][5]
* [DocBlockr][6]
* [MarkdownHighlighting][8]
* [SCSS][9]
* [SublimeCodeIntel][11]
* [AdvancedNewFile][12]
* [Babel][13]
* [Nodejs][14]
* [Jade.tmbundle][15]
* [vue-syntax-highlight][16]
* [AngularJS][17]
* [Better Coffeescript][18]
* [SFTP][19]
* [GitGutter][20]

#### 快捷键的重新绑定

这里包括了 `macOS` 和 `Windows` 下的快捷键，现在本人转到 `Mac` 平台开发，由于公司电脑配置的还是 `Windows`，所以顺带也附上了。 

#### bh_core.sublime-settings

对 `Brackets Highlighter` 插件做的一些修改。

#### SFTP

可以免费试用，但是会有弹窗出来提示你购买，所以在网上找了一个万能 *Key*，放在 `SFTP -> Settings - User` 里就好。

```json
{
  "email": "xiaosong@xiaosong.me",
  "product_key": "d419f6-de89e9-0aae59-2acea1-07f92a"
}
```

现在我已经没有弹窗提示了。

### GitGutter

可以在编辑文件中实时监测显示 *git 文件* 的修改状态，感觉还不错的样子。

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

#### 喜欢的主题

* [Dracula][10]
* *Monokai*
* *Mac Classic*

[1]: https://github.com/BoundInCode/AutoFileName	
[3]: https://github.com/facelessuser/BracketHighlighter
[4]: https://github.com/jdc0589/JsFormat
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
[17]: https://github.com/angular-ui/AngularJS-sublime-package
[18]: http://aponxi.github.io/sublime-better-coffeescript/
[19]: https://wbond.net/sublime_packages/sftp
[20]: https://github.com/jisaacks/GitGutter