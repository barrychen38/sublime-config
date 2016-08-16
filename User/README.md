### 配置项的说明

#### Preference.sublime-settings

Sublime Text 下的 snippets 和个人偏好设置

完全是个人习惯，可以借鉴，如有雷同，纯属参考

#### noscale.sublime-snippet

主要用在手机端 H5 页面开发时可能会用到

```html
<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
```

#### sureie.sublime-snippet

强制规定 `IE` 的渲染模式，不想每次打一遍

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

#### apple.sublime-snippet

可隐藏地址栏，仅针对 *IOS* 的 `Safari`（注：*IOS7.0* 版本以后，`safari` 上已看不到效果）

```html
<meta name="apple-mobile-web-app-capable" content="yes">
```

#### tel.sublime-snippet

*IOS* 中禁用将数字识别为电话号码 / 忽略 *Android* 平台中对邮箱地址的识别

```html
<meta name="format-detection" content="telephone=no">
```

#### author.sublime-snippet

在页面中声明创造代码的传奇者😂

```html
<meta name="Author" content="Funnychen38">
```

#### rcm.sublime-snippet & rcp.sublime-snippet

手机和 *PC* 端可能会用到的一些重置样式，规定了只能在 *scss* 文件中使用，可自行修改

> source.scss ==> source.css