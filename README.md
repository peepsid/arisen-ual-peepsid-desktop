# UAL for PeepsAuthDesktop Authenticator

This authenticator is meant to be used with [PeepsAuthDesktop](https://get-peepsid.com/) and [Universal Authenticator Library](https://github.com/arisenual/universal-authenticator-library). When used in combination with them, it gives developers the ability to request transaction signatures through PeepsAuthDesktop using the common UAL API.

![PeepsLabs](https://img.shields.io/badge/PeepsLabs-5cb3ff.svg)

# About PeepsLabs

PeepsLabs repositories are experimental.  Developers in the community are encouraged to use PeepsLabs repositories as the basis for code and concepts to incorporate into their applications. Community members are also welcome to contribute and further develop these repositories. Since these repositories are not supported by Peeps, we may not provide responses to issue reports, pull requests, updates to functionality, or other requests from the community, and we encourage the community to take responsibility for these.

## Supported Environments
- The PeepsAuthDesktop Authenticator only supports Desktop Browser Environments

## Getting Started

`yarn add ual-peepsid`

#### Dependencies

You must use one of the UAL renderers below.

React - `@arisenual/reactjs-renderer`


PlainJS - `@arisenual/plainjs-renderer`


#### Basic Usage with React

```javascript
import { PeepsAuthDesktop } from 'ual-peepsid'
import { UALProvider, withUAL } from '@arisenual/reactjs-renderer'

const exampleNet = {
  chainId: '',
  rpcEndpoints: [{
    protocol: '',
    host: '',
    port: '',
  }]
}

const App = (props) => <div>{JSON.stringify(props.ual)}</div>
const AppWithUAL = withUAL(App)

const peepsid = new PeepsAuthDesktop([exampleNet], { appName: 'Example App' })

<UALProvider chains={[exampleNet]} authenticators={[peepsid]}>
  <AppWithUAL />
</UALProvider>
```

## Contributing

[Contributing Guide](https://github.com/arisenual/ual-peepsid/blob/develop/CONTRIBUTING.md)

[Code of Conduct](https://github.com/arisenual/ual-peepsid/blob/develop/CONTRIBUTING.md#conduct)

## License

[MIT](https://github.com/arisenual/ual-peepsid/blob/develop/LICENSE)

## Important


See [LICENSE](./LICENSE) for copyright and license terms.

All repositories and other materials are provided subject to the terms of this [IMPORTANT](./IMPORTANT.md) notice and you must familiarize yourself with its terms.  The notice contains important information, limitations and restrictions relating to our software, publications, trademarks, third-party resources, and forward-looking statements.  By accessing any of our repositories and other materials, you accept and agree to the terms of the notice.
