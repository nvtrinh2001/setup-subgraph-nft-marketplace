# Subgraph Setup for The Graph

By using The Graph, we can deploy our application (in this case: NFT Marketplace) in a decentralized layer.

# Quick Start

1. Install Subgraph CLI

`yarn global add @graphprotocol/graph-cli`

2. Log into [The Graph UI](thegraph.com/studio/subgraph) and create a new Subgraph

3. Initialize your Subgraph

`graph init --studio YOUR_SUBGRAPH_NAME`

4. Authenticate within the CLI

`graph auth --studio YOUR_DEPLOY_KEY`

5. Update your `subgraph.yaml`

- Update the `address` with your NftMarketplace Address
- Update the `startBlock` with the block right before your contract was deployed

6. Build

Generates code in the `generated` folder based on your `schema.graphql`

`graph codegen`

Generates `build` folder to be uploaded to The Graph

`graph build`

7. View UI

Back in your hardhat project, mint and list an NFT with:

`yarn hardhat run scripts/mint-and-list.js --network rinkeby`
