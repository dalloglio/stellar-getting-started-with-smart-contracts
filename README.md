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
