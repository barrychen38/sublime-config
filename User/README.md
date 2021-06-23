### 配置项的说明

#### Preference.sublime-settings

*Sublime Text* 下的 `snippets` 和个人偏好设置

完全是个人习惯，可以借鉴，如有雷同，纯属参考

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
