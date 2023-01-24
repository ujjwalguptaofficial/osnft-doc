---
sidebar_position: 2
---

# Approver 

Approver is a contract which is used to verify the project during the minting of a NFT. Before the minting - the request is sent to approver : the approver verifies the project info and then stores the meta data like star, fork and also calculate worth of the project.

The NFT contract calls approver contract to check whether project has been approved or not and to get the worthOfTheProject. If approver does not approve then token can not be minted.

👉 The Appover component has been added to make sure we mint only valid project and the minting process is decentralized. With approver in place - the minting is done actually by user but the NFT contract will mint only if it is approved.

The Appprover emit and event when project is approved.

```
ProjectApproved(bytes32 indexed tokenId, address indexed account);
```
