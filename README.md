# on-contract-event
Subscribe to smart contract events, which is [currently broken on Lotus w/ Ethers@6](https://github.com/filecoin-project/lotus/issues/11589).

## Usage

```js
import { onContractEvent } from 'on-contract-event'

const it = onContractEvent({
  contract,
  provider,
  rpcUrl,
  rpcHeaders
})
for await (const event of it) {
  console.log({
    name: event.name,
    args: event.args
  })
}
```

## API

### `onContractEvent()`

Options:

- `contract`: Ethers contract
- `provider`: Ethers provider
- `rpcUrl`: JSON-RPC endpoint URL
- `rpcHeader`: JSON-RPC headers object
- `signal`: Optional `AbortSignal`
