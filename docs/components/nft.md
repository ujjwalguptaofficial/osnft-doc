---
sidebar_position: 1
---

# NFT 

NFT stands for non fungible tokens. It represents digital record of different art on blockchain. 

OSNFT stands for OpenSource NFT. It represents opensource project as art.

The NFT contract is deployed at 

* Testnet (Mumbai) - 0x89D0BB9246940AeBa9dC5328D2850fc308b2bdA7

## Identification

Each NFT is represented by a tokenId which is hash of project URL.

```
const tokenId = hash("github.com/ujjwalguptaofficial/mahaljs");
```

## Metadata

The NFT contract stores minimum information which are needed for identifying the NFT and owner. Following information are stored on chain - 

* NFT id
* NFT owners 
* Investments info
* creator of NFT

The meta data is stored in centralized database and Repo providers like github is considered as source of truth. Thus actual meta data stay with your project repo providers.

The meta data is dynamic means attributes like stars, fork etc are updated with time and thus it should be also updated on nft. The project owner can update the meta data from the UI.

## Validation

Users might abuse the system by minting any url as a project or by minting the same project with different url.

That is why we have verification mechanism. Each NFT mint is validated by backend and a signature is generated which is required for tokenizing or minting NFT. It guarantess that each project has been validated and only valid projects are minted.
