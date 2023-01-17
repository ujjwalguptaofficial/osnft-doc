---
sidebar_position: 1
---

# NFT 

The NFT is represented by tokenId which is hash of project URL and is created by calling the `mint` method in NFT contract. 

The NFT contract stores only the information which are needed for identifying the NFT and owner like -

* NFT id
* NFT ownership 
* Share of NFT
* Percentage cut


The meta data is stored in database and repo providers like github is considered as source of truth. Thus actuall meta data stay with your project repo providers.

The meta data is dynamic means attributes like stars, fork etc are updated with time and thus it should be also updated on nft.

The project owner can update the meta data from the UI.