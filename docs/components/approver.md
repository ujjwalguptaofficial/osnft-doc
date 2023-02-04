---
sidebar_position: 2
---

# Approver 

Approver is a contract which is used to verify the project during the minting of a NFT. Before the minting - the request is sent to approver : the approver verifies the project info and then stores the meta data like star, fork and also calculate worth of the project.

The NFT contract calls approver contract to check whether project has been approved or not and to get the worthOfTheProject. If approver does not approve then token can not be minted.

The Approver contract is deployed at 

* Mainnet (Polygon) - 0x1E25125e5e03290c0E0A95e83f7236F66a7eEf17
* Testnet (Mumbai) - 0xb5d23fB812F4B7428DCDa7c2dfdFc0179A18E926

## Why

👉 The Appover component has been added to make sure we mint only valid project and the minting process is decentralized. With approver in place - the minting is done actually by user but the NFT contract will mint only if it is approved.

The Appprover emit an event `ProjectApproved` when project is approved.

```
ProjectApproved(bytes32 indexed tokenId, address indexed account);
```
