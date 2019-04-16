### 配置项的说明

#### Preference.sublime-settings

*Sublime Text* 下的 `snippets` 和个人偏好设置

完全是个人习惯，可以借鉴，如有雷同，纯属参考

#### noscale.sublime-snippet

主要用在手机端 `H5` 页面开发时可能会用到

```html
<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no">
```

#### scale5.sublime-snippet

直接对屏幕的显示宽度做限制，无论什么尺寸的屏幕下都是一定的宽度，所以宽度可以自行修改

```html
<meta name="viewport" content="width=640,target-densitydpi=device-dpi,maximum-scale=1,user-scalable=no">
```

#### sureie.sublime-snippet

强制规定 `IE` 的渲染模式

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

#### apple.sublime-snippet

可隐藏地址栏，仅针对 *IOS* 的 `Safari`（注：*IOS7* 版本以后，`safari` 上已看不到效果）

```html
<meta name="apple-mobile-web-app-capable" content="yes">
```

#### te.sublime-snippet

*IOS* 中禁用将数字识别为电话号码和邮箱的识别 / 忽略 *Android* 平台中对邮箱地址的识别

```html
<meta name="format-detection" content="telephone=no,email=no">
```

#### mstap.sublime-snippet

*Windows Phone* 中的点击没有阴影，虽然一半测试机不会有，但还是做好以防万一

```html
<meta name="msapplication-tap-highlight" content="no">
```

#### render.sublime-snippet

启用 *360浏览器* 的极速模式，其实一般情况下不太用到

```html
<meta name="renderer" content="webkit">
```

### React-Comp.sublime-snippet

项目中开始写 *React* 新组件的初始结构

```js
import React, { Component } from 'react'
import PropTypes from 'prop-types'
import { connect } from 'react-redux'
import cn from 'classnames'

import Text from '${1:relativePath}presentational/text/Text'

import withStyles from '${1:relativePath}../core/withStyles'
import s from './${2:componentName}.scss'

const Msg_HelloWorld = { id: 'Hello-World', defaultMessage: '你好世界' }

@connect(
    state => ({}),
    {},
    null,
    { withRef: true },
)
@withStyles(s)
export default class ${2:componentName} extends Component {
    static propTypes = {

    }

    static defaultProps = {

    }

    static contextTypes = {
        intl: PropTypes.object.isRequired,
    }

    constructor (props) {
        super(props)
    }

    render () {
        const { formatMessage: fm } = this.context.intl
        return <Text className={cn(s.container, 'row-flex')}>{fm(Msg_HelloWorld)}</Text>
    }
}
```

另外更多的关于 `H5` 的开发问题及解决方案，可以参考[这里](https://github.com/jtyjty99999/mobileTech/blob/master/README.md)
