# PoolTogether Staking Vault

## Overview

The staking vault is an ERC4626 vault that takes deposits of an underlying asset and mints shares at a 1:1 ratio. The vault has no yield source and will always redeem shares at a 1:1 ratio with assets.

## Deployments

| Network | Contract                 | Deployment Address                                                                                                    |
| ------- | ------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| Base    | PrizeStakingVaultFactory | [0x48492f83D9e1d848d33a461D49a2071A6FdcC037](https://basescan.org/address/0x48492f83d9e1d848d33a461d49a2071a6fdcc037) |

## Development

### Installation

You may have to install the following tools to use this repository:

- [Foundry](https://github.com/foundry-rs/foundry) to compile and test contracts
- [direnv](https://direnv.net/) to handle environment variables
- [lcov](https://github.com/linux-test-project/lcov) to generate the code coverage report

Install dependencies:

```
npm i
```

### Compile

Run the following command to compile the contracts:

```
npm run compile
```

### Coverage

Forge is used for coverage, run it with:

```
npm run coverage
```

You can then consult the report by opening `coverage/index.html`:

```
open coverage/index.html
```

### Code quality

[Husky](https://typicode.github.io/husky/#/) is used to run tests when committing.

[Prettier](https://prettier.io) is used to format TypeScript and Solidity code. Use it by running:

```
npm run format
```

[Solhint](https://protofire.github.io/solhint/) is used to lint Solidity files. Run it with:

```
npm run hint
```

### CI

A default Github Actions workflow is setup to execute on push and pull request.

It will build the contracts and run the test coverage.

You can modify it here: [.github/workflows/coverage.yml](.github/workflows/coverage.yml)
