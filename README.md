# Getting started with Stellar Smart Contracts

Smart contracts are self-executing programs with the terms of an agreement written directly into the code. They automatically enforce and execute the terms of the contract when predefined conditions are met. Developers must define the rules and logic of the contract while also ensuring security. Once written and tested, smart contracts are deployed to the blockchain, where they become immutable and publicly accessible.

This project walk through how to get set up to write smart contracts on Stellar, plus an introduction to testing, storing data, and deploying your contracts. It also provides an array of example contracts for use.

Tutorial from https://developers.stellar.org/docs/build/smart-contracts/getting-started

## Run the container

```bash
docker compose up -d
```

## Access the container to execute the following commands

```bash
docker compose exec app bash
```

## Run the tests

```bash
cargo test
```

## Build the contract

```bash
stellar contract build
```

## Deploy the contract hello-world to Testnet

```bash
stellar contract deploy \
    --wasm target/wasm32-unknown-unknown/release/hello_world.wasm \
    --source dev \
    --network testnet
```

This returns the contract's id, starting with a `C`. In this example, we're going to use `CBT3DECFK3LIVI7L4RBYVTSVKTRMDJCZ25OXMA5NSOERO7SZY2JJ4Y3C`, so replace it with your actual contract id.

## Interact with the deployed contract

```bash
stellar contract invoke \
    --id CBT3DECFK3LIVI7L4RBYVTSVKTRMDJCZ25OXMA5NSOERO7SZY2JJ4Y3C \
    --source dev \
    --network testnet \
    -- \
    hello \
    --to RPC
```

The following output should appear.

```bash
["Hello","RPC"]
```
