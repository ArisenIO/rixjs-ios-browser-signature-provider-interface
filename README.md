# ARISEN Signature Provider for ARISEN Authenticator in iOS
A [Signature Provider Interface](https://github.com/ARISENIO/arisen-signature-provider-interface) for communicating with an authenticator from iOS Safari using the [ARISEN Authentication Transport Protocol Specification](https://github.com/ARISENIO/arisen-authentication-transport-protocol-spec).

## Overview
When plugged into `arisenjs`, this signature provider enables iOS web applications to route signing requests to an iOS authenticator app. Full instructions for `arisenjs` can be found [here](https://github.com/ARISENIO/arisenjsv1).

## Notes
This signature provider currently only works for mobile Safari.

## Installation
```bash
yarn add arisen-ios-browser-signature-provider-interface
```

## Basic Usage
```javascript
import { Api, JsonRpc } from "arisenjsv1"
import { SignatureProvider } from "arisen-ios-browser-signature-provider-interface"

const rpc = new JsonRpc("RPC_ENDPOINT_HERE")
const signatureProvider = new SignatureProvider({
  declaredDomain: "YOUR_DOMAIN", // This domain must have a `chain-manifests.json` file at the root
  returnUrl: "YOUR_DOMAIN",
})
const api = new Api({
  rpc,
  signatureProvider,
})

api.transact(...)

```

## Links
- [Signature Provider Interface](https://github.com/arisenio/arisen-signature-provider-interface)
- [ARISEN Authentication Transport Protocol Specification](https://github.com/ARISENIO/arisen-authentication-transport-protocol-specification)

## Contribution
Check out the [Contributing](https://github.com/ARISENIO/arisen-ios-browser-signature-provider-interface/blob/develop/CONTRIBUTING.md) guide and please adhere to the [Code of Conduct](https://github.com/ARISENIO/arisen-ios-browser-signature-provider-interface/blob/develop/CONTRIBUTING.md#conduct)

## License
[MIT licensed](https://github.com/ARISENIO/arisen-ios-browser-signature-provider-interface/blob/develop/LICENSE)
