---
sidebar_position: 2
---

# Approver 

Approver is a contract which is used to verify the project during the minting of a NFT. Before the minting - the request is sent to approver : the approver verifies the project info and then stores the meta data like star, fork and also calculate worth of the project.

The NFT contract calls approver contract to check whether project has been approved or not and to get the worthOfTheProject. If approver does not approve then token can not be minted.

