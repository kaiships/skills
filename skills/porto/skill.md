# Porto

Manage Porto account abstraction - upgrade wallets, send transactions with stablecoin gas, check balances.

## Usage

```
/porto <command> [options]
```

## Commands

### Upgrade EOA to Porto Account
```
/porto upgrade <chain>
```
Upgrades an existing wallet to a Porto Account using EIP-7702. Enables paying gas with USDC/USDT.

### Send Transaction
```
/porto send <to> <amount> [token] [fee-token] [chain]
```
Send a transaction using Porto. Pay gas with stablecoins instead of native tokens.

- `to` — Recipient address
- `amount` — Amount to send
- `token` — Token to send: eth, usdc, usdt (default: eth)
- `fee-token` — Gas payment: usdc, usdt, native (default: usdc)
- `chain` — Target chain (default: ethereum)

### Check Status
```
/porto status <address> [chain]
```
Check if an address is upgraded to Porto, view balances across chains.

### List Capabilities
```
/porto caps
```
Show supported chains and Porto features.

## Supported Chains

**Mainnets:** ethereum, base, optimism, arbitrum, polygon, bnb, celo, gnosis, berachain, katana

**Testnets:** sepolia, baseSepolia, optimismSepolia, arbitrumSepolia, berachainBepolia, hoodi

## Process

1. **Identify command** — upgrade, send, status, or caps
2. **Get private key** — Ask user for private key if needed (upgrade/send commands)
3. **Execute via porto-cli** — Run the appropriate command
4. **Report result** — Show transaction ID, status, or balances

## Examples

```
/porto upgrade ethereum
/porto send 0x1234...abcd 0.1 eth usdc ethereum
/porto status 0x1234...abcd
/porto caps
```

## Security

- Private keys are only used locally for signing
- Never log or store private keys
- Keys are passed directly to porto-cli, not stored

## Dependencies

Requires porto-cli: `npm install -g porto-cli` or use via `npx porto-cli`

## Source

https://github.com/kaiships/porto-cli
