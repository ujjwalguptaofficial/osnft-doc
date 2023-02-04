---
sidebar_position: 1
---

# NFT 

NFT stands for non fungible tokens. It represents digital record of different art on blockchain. 

OSNFT stands for OpenSource NFT. It represents opensource project as art.

The NFT contract is deployed at 

* Mainnet (Polygon) - 0xf8c8c9315c9A0434B7077AB519F0Ed1A8E0CC749
* Testnet (Mumbai) - 0x8CE6cB2982339c11f4643fDA2d4448A424AA5847

## Identification

Each NFT is represented by a tokenId which is hash of project URL.

```
const tokenId = hash("github.com/ujjwalguptaofficial/mahaljs");
```

## Metadata

The NFT contract stores minimum information which are needed for identifying the NFT and owner. Following information are stored on chain - 

* NFT id
* NFT ownership 
* Share of NFT
* Percentage cut
* creator of NFT

The meta data is stored in centralized database and Repo providers like github is considered as source of truth. Thus actual meta data stay with your project repo providers.

The meta data is dynamic means attributes like stars, fork etc are updated with time and thus it should be also updated on nft. The project owner can update the meta data from the UI.

## Validation

Users might abuse the system by minting any url as a project or by minting the same project with different url.

That is why we have approving mechanism. Each NFT mint is validated by adminstrator using [approver contract](/components/approver). It guarantess that each project has been validated and only valid projects are minted.

The NFT emits an event which can be used to know what project is being minted and attribute. This allows anyone to verify and making everything trustable.

```
ProjectMint(
    string indexed projectUrl,
    NFT_TYPE nftType,
    uint32 share
);
```