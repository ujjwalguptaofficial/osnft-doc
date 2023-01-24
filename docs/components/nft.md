---
sidebar_position: 1
---

# NFT 

The NFT is represented by tokenId which is hash of project URL and is created by calling the `mint` method in NFT contract. 

The NFT contract stores only the information which are needed for identifying the NFT and owner. Following information are stored on chain - 

* NFT id
* NFT ownership 
* Share of NFT
* Percentage cut
* creator of NFT

The meta data is stored in centralized database and Repo providers like github is considered as source of truth. Thus actual meta data stay with your project repo providers.

The meta data is dynamic means attributes like stars, fork etc are updated with time and thus it should be also updated on nft. The project owner can update the meta data from the UI.

## Validation

Users might abuse the system by minting any url as a project or by minting the same project with different url.

That is why we have approving mechanism. Each NFT mint is validated by adminstrator using approver contract. It guarantess that each project has been validated and only valid projects are minted.

The NFT emits an event which can be used to know what project is being minted and attribute. This allows anyone to verify and making everything trustable.

```
ProjectMint(
    string indexed projectUrl,
    NFT_TYPE nftType,
    uint32 share
);
```