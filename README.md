# vscode-snippets-mobx-react README

create code snippets at mobx react
now it can support rematch!

## normal

| Prefix  | Method                                              |
| ------: | --------------------------------------------------- |
| `imp→`  | `import moduleName from 'module'`                   |
| `imn→`  | `import 'module'`                                   |
| `imd→`  | `import { destructuredModule } from 'module'`       |
| `exp→`  | `export default moduleName`                         |
| `enf→`  | `export const functionName = (params) => { }`       |
| `edf→`  | `export default (params) => { }`                    |
| `met→`  | `methodName = (params) => { }`                      |
| `fre→`  | `arrayName.forEach(element => { }`                  |
| `fof→`  | `for(let itemName of objectName { }`                |
| `fin→`  | `for(let itemName in objectName { }`                |
| `sti→`  | `setInterval(() => { }, intervalTime`               |
| `sto→`  | `setTimeout(() => { }, delayTime`                   |
| `prom→` | `return new Promise((resolve, reject) => { }`       |
| `cp→`   | `const { } = this.props`                            |
| `cs→`   | `const { } = this.state`                            |

## React

| Prefix      | Method                                                                              |
| ----------: | ----------------------------------------------------------------------------------- |
| `est→`      | `this.state = { }`                                                                  |
| `cwm→`      | `componentWillMount = () => { }` DEPRECATED!!!                                      |
| `cdm→`      | `componentDidMount = () => { }`                                                     |
| `scu→`      | `shouldComponentUpdate = (nextProps, nextState) => { }`                             |
| `cwup→`     | `componentWillUpdate = (nextProps, nextState) => { }` DEPRECATED!!!                 |
| `cdup→`     | `componentDidUpdate = (prevProps, prevState) => { }`                                |
| `cwun→`     | `componentWillUnmount = () => { }`                                                  |
| `cwun→`     | `componentWillUnmount = () => { }`                                                  |
| `gdsfp→`    | `static getDerivedStateFromProps(nextProps, prevState) { }`                         |
| `gsbu→`     | `getSnapshotBeforeUpdate = (prevProps, prevState) => { }`                           |
| `ren→`      | `render() { return( ) }`                                                            |
| `sst→`      | `this.setState({ })`                                                                |
| `ssf→`      | `this.setState((state, props) => return { })`                                       |
| `props→`    | `this.props.propName`                                                               |
| `state→`    | `this.state.stateName`                                                              |


### `rmcp`

```javascript
import React, { Component } from 'react'
import { observer, inject } from 'mobx-react'
import PropTypes from 'prop-types'

@inject('store')
@observer
export default class Add extends Component {
  static propTypes = {
  }
  render() {
    return <div></div>
  }
}

```

### `rmsc`

```javascript
import { observable, action, configure, runInAction } from 'mobx'

configure({ enforceActions: true })

export default class A {
  @observable
  name = ''

  @action
  async functionName (params) {
    runInAction(() => {
    })
  }
}

```

### `rmcpf`

```javascript
import React, { Component, Fragment } from 'react'
import PropTypes from 'prop-types'
import { observer, inject } from 'mobx-react'

@inject('store')
@observer
export default class $1 extends Component {
  static propTypes = {
  }
  render() {
    return (
      <Fragment>
      </Fragment>
    )
  }
}

```

### `rcws`


```javascript
import React, { Component } from 'react'
import PropTypes from 'prop-types'
import Style from './index.less'

export default class $0 extends Component {
  static propTypes = {
  }
  constructor() {
    super()
    Style.use()
  }

  componentWillUnmount () {
    Style.unuse()
  }
  render() {
    return (
      <>
      </>
    )
  }
}

```

### `rpsr`

```javascript
import React, { Component } from 'react'
import { connect } from 'react-redux'
import PropTypes from 'prop-types'
import { createContainer } from 'utils/hoc'

class $1 extends Component {
  static propTypes = {
    actions: PropTypes.object.isRequired,
  }
  state = {}
  constructor (props) {
    super(props)
    //this.props.actions.get()
  }
  
  render () {
    return (
      <>
        <div />
      </>
    )
  }
}

const mapState = state => ({
  error: state.common.error,
})

const mapDispatch = dispatch => ({
  actions: {
    // createDataTrack: dispatch.common.createDataTrack,
    get: dispatch.idx.get,
  },
})

export default createContainer(
  connect(
    mapState,
    mapDispatch
  )($1)
)

```


### `ratp`

```javascript
import request from 'utils/fetch'
export default {
  get (params) {
    return request.get('your api url', params)
  },
  post (params) {
    return request.post('your api url', params)
  },
}

```


**Enjoy!**
