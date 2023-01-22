---
sidebar_position: 2
---

# Approver 

Approver is a contract which is used to verify the project during the minting of a NFT. Before the minting - the request is sent to approver : the approver verifies the project info and then stores the meta data like star, fork and also calculate worth of the project.

The NFT contract calls approver contract to check whether project has been approved or not and to get the worthOfTheProject. If approver does not approve then token can not be minted.

👉 The Appover component has been added to make sure we mint only valid project and the minting process is decentralized. With approver in place - the minting is done actually by user but the NFT contract will mint only if it is approved.

## Problem

Currently approver is a centralized and managed by the creator of the project. But there are few issue with the process -

The approver can mint any project and being a single person managing means there are chances of - mistake or deliberately minting bad project. (Please note that this will never be done but we want something which is futureproof and trusted).

## Solution

So for this reason approver needs to be decentralized.
<br/>

<img src="/img/decentralize_meme.jpg" />

<br/><br/>
This is in our future roadmap but this needs lot of efforts. We will be working on this once we have enough fund.

