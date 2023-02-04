---
sidebar_position: 3
---

# NFT Marketplace 

NFT marketplace allows you to sell, buy, create auction, bidding on the auction basically everything through which NFT can be transferred to different people.

The Marketplace contract is deployed at 

* Mainnet (Polygon) - 0x59A180903d4F51B74385FABFcd27F4f614b71324
* Testnet (Mumbai) - 0x40744b3Da26f29626c58F87339C4130CBd42a27b

## sell

A user who owns the NFT can place on sale for some determined amount. The sell is visible on the marketplace UI.

The sell requires - input amount and payment token.

## buy

A NFT placed on sale can be bought by anyone with a value equal greater than sell amount. The NFT will be tranferred to buyer immediately.

## Auction

Auction can be created to sell the NFT. Auction requires three inputs - 

* Initial bid amount
* Payment token - erc20 token 
* Until time

During the auction - anyone can bid with amount higher than bid amount and process keeps repeating untill the expiry time. The last bidder can claim the NFT which will tranfer the NFT.

## Bid

Bid allows you to participate in an auction of NFT. You can place a BID with the higher amount than the current bid amount and you will become the current bidder.

If someone bids higher than you - then they becomes the current bidder and if no one does then you stayed as current bidder.

When auction is expired - you can claim the NFT which will does two things -

* transfer the payment amount to seller with some cuts tranferred to marketplace
* transfer the NFT to you

## cancelSell

Once placed on sell - user can also cancel the sell.

