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
**Enjoy!**
