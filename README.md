
- **Interoperability with Web2**: The HTTPS outcall feature permits canisters to reach out to any web service in a replicated fashion, using deterministic response results.

## How this example works

This example creates a canister smart contract with two functions: 
- The first function makes a call to the Ethereum mainnet through the [ICP EVM RPC canister](https://internetcomputer.org/docs/current/developer-docs/multi-chain/ethereum/evm-rpc/overview) using the PublicNode RPC provider and [HTTPS outcalls](https://internetcomputer.org/docs/current/developer-docs/smart-contracts/advanced-features/https-outcalls/https-outcalls-overview). It retrieves log information from Ethereum about a specific address and topic.
  -  If this function returns a successful result, it calls the second function.
-  The second function sends Bitcoin to a specified address.
  - In this example, the Bitcoin transaction is fabricated and will not send a real transaction. Instead, the expected result is a "Malformed transaction" error message. This is because creating a Bitcoin transaction is out of the scope of this workshop, but can be accomplished by following the ICP developer docs:
  - [Bitcoin integration overview](https://internetcomputer.org/docs/current/developer-docs/multi-chain/bitcoin/overview)
  - [Bitcoin addresses](https://internetcomputer.org/docs/current/developer-docs/multi-chain/bitcoin/using-btc/generate-addresses)
  - [Bitcoin transactions](https://internetcomputer.org/docs/current/developer-docs/multi-chain/bitcoin/using-btc/create-transactions)
  - [Bitcoin integration: How it works](https://internetcomputer.org/docs/current/references/bitcoin-how-it-works)

## Why use Motoko?

Motoko is a modern, general-purpose programming language specifically to author ICP canister smart contracts and utilize ICP’s unique features and architecture. It is designed to be approachable for programmers who have some basic familiarity with object-oriented and/or functional programming:JavaScript, Rust, Swift, TypeScript, C#, or Java. It uses an actor-based model and orthogonal persistence for simple, safe, and efficient data storage without a database or secondary memory.

## Prerequisites

- You will need to have [dfx installed](https://internetcomputer.org/docs/current/developer-docs/getting-started/install/#installing-dfx-via-dfxvm).

## Running this project locally

```
dfx start --background
dfx deploy
```

Note: Not all functionality of this project will work locally, and it is recommended to deploy this project to the mainnet.

## Deploying to the mainnet

```
dfx deploy --network ic
```

### Obtaining cycles

To deploy to the mainnet, you will need cycles, the currency used to pay gas fees on ICP. To obtain cycles during HackMIT:

- Request a coupon code from the ICP HUB team on Discord in the HackMIT channel.
- Go to [https://faucet.dfinity.org](https://faucet.dfinity.org).
- Insert your coupon code and follow the on-screen instructions to redeem.

#### Notes
- You will need to have [dfx installed](https://internetcomputer.org/docs/current/developer-docs/getting-started/install/#installing-dfx-via-dfxvm).
- Cycles coupon is good for 10T cycles, which is typically enough for deploying a frontend and backend canister.
- Recommendation: Do not deploy to the mainnet until your dapp is complete.

## Resources 

- [ICP Developer Docs](https://internetcomputer.org/docs/current/developer-docs/getting-started/overview-of-icp)
- [ICP Developer Journey tutorial series](https://internetcomputer.org/docs/current/tutorials/developer-journey/)
- [Motoko documentation](https://internetcomputer.org/docs/current/motoko/main/getting-started/motoko-introduction)
- [Chain Fusion overview](https://internetcomputer.org/docs/current/developer-docs/multi-chain/overview)
- [Bitcoin integration overview](https://internetcomputer.org/docs/current/developer-docs/multi-chain/bitcoin/overview)
- [Bitcoin addresses](https://internetcomputer.org/docs/current/developer-docs/multi-chain/bitcoin/using-btc/generate-addresses)
- [Bitcoin transactions](https://internetcomputer.org/docs/current/developer-docs/multi-chain/bitcoin/using-btc/create-transactions)
- [Bitcoin integration: How it works](https://internetcomputer.org/docs/current/references/bitcoin-how-it-works)
- [Ethereum integration overview](https://internetcomputer.org/docs/current/developer-docs/multi-chain/ethereum/overview)
- [EVM RPC canister overview](https://internetcomputer.org/docs/current/developer-docs/multi-chain/ethereum/evm-rpc/overview)
- [EVM RPC canister: How it works](https://internetcomputer.org/docs/current/developer-docs/multi-chain/ethereum/evm-rpc/how-it-works)
- [Using the EVM RPC canister](https://internetcomputer.org/docs/current/developer-docs/multi-chain/ethereum/evm-rpc/evm-rpc-canister)
- [Other Chain Fusion example projects](https://internetcomputer.org/docs/current/developer-docs/multi-chain/examples)
