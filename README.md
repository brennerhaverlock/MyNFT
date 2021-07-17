
## Prerequisites

Please install or have installed the following:

- [nodejs and npm](https://nodejs.org/en/download/)
- [python](https://www.python.org/downloads/)
## Installation

1. [Install Brownie](https://eth-brownie.readthedocs.io/en/stable/install.html), if you haven't already. Here is a simple way to install brownie.

```bash
pip install eth-brownie
```
Or, if that doesn't work, via pipx
```bash
pip install --user pipx
pipx ensurepath
# restart your terminal
pipx install eth-brownie
```

2. Clone this repo
```
brownie bake nft-mix
cd nft
```

1. [Install ganache-cli](https://www.npmjs.com/package/ganache-cli)

```bash
npm install -g ganache-cli
```

### Running Scripts

The simple collectibles work on a local network,  however the advanced requires a testnet. You will need testnet rinkeby ETH and testnet Rinkeby LINK. You can find faucets for both in the [Chainlink documentation](https://docs.chain.link/docs/link-token-contracts#rinkeby). 

# Deploy ERC721
```
brownie run scripts/simple_collectible/deploy_simple.py --network rinkeby
brownie run scripts/simple_collectible/create_collectible.py --network rinkeby
```

## Verify on Etherscan

> Looking for help fixing this!

Currently, the advanced collectibles contract has an issue with ERC721 and the Chainlink contracts, so they have be verified manually. However, the simple contract can be verified if you just set your `ETHERSCAN_TOKEN`. 

### Misc
There are some helpful scripts in `helpful_scripts.py`.

# Viewing on OpenSea
After running the scripts from the `For the Advanced ERC721` section

1. Create the metadata

Metadata is the URI needed to upload data. You can either:
- Upload to IPFS yourself
- Use the metadata already created when you cloned this repo. 
