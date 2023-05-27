---
sidebar_position: 1
---

# NFT 

NFT stands for non fungible tokens. It represents digital records of different art on blockchain.

OSNFT stands for OpenSource NFT. It represents open source project as art.

The NFT contract is deployed at 

* Testnet (Mumbai) - 0x89D0BB9246940AeBa9dC5328D2850fc308b2bdA7

## Identification

Each NFT is represented by a tokenId which is the hash of the project URL.

```
const tokenId = hash("github.com/ujjwalguptaofficial/mahaljs");
```

## Metadata

The NFT contract stores minimum information which is needed for identifying the NFT and owner. Following information are stored on chain - 

* NFT id
* NFT owners 
* Investments info
* creator of NFT

The meta data is stored in centralized database and Repo providers like github is considered as source of truth. Thus actual metadata stays with your project repo providers.

The meta data is dynamic, meaning attributes like stars, forks etc are updated with time and thus it should be also updated on NFT. The project owner can update the metadata from the UI.

## Validation

Users might abuse the system by minting any url as a project or by minting the same project with different urls.

That is why we have a verification mechanism. Each NFT mint is validated by backend and a signature is generated which is required for tokenizing or minting NFT. It guarantees that each project has been validated and only valid projects are minted.
