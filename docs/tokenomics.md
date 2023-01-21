---
sidebar_position: 3
---

# Tokenomics

The whole OSNFT DAPP ecosystem is powered by **OSD coin**. It is a utility token which is used at different places for providing different services.

The total supply of OSD coin is - 1 Billion.

## Use

OSD coin is used for following services - 

* Mint NFT 
* Burn NFT
* Sell priority
* Cancel sell
* Referral reward - limited time 
* Quiz game


The usage are not limited to these services only. With time more features will be added in ecosytem and thus more usage.

### Mint NFT

OSD coin is needed to mint the NFT. The value of OSD coin is calculated based on star and fork count of the project called as `worthOfProject`. The `worthOfProject` can not be greater than 1.

```
function worthOfProject(uint256 starCount,uint256 forkCount) public view returns (uint256) {
    uint256 value = (_starConstant * starCount) +
        (_forkConstant * forkCount);
    require(value > 0, "require_worth_above_zero");
    // worth can not be more than one token
    return value > _oneToken ? _oneToken : value;
}

```

The OSD coin is burnt in minting of the project decreasing the totalSupply of the OSD coin.

> It is similar to burning fuel for reaching the destination from the source.

### Burn NFT

Similar to minting NFT - the OSD coin worthOfProject is burned for burning NFT.

> It is similar to burning fuel for reaching back to source from the destination. Although you are at same point the work was done.

### Sell priority

Sell priority can be used to change the ordering of the the sell in marketplace. You can specify sell priority and NFT with highest priority will be shown in marketplace for sell. The investors who are quickly buying and selling can use this facility to better invest.

The OSD amount is directly proportional to the `sellPriority` value and calculated by following formulla -

```
_sellPriorityConstant = 1000000000000000; // 10^15 - allows sell Priority to be 1000 in one OSD
sellPriority * _sellPriorityConstant
```

### Cancel sell

Cancelling sell is very common and it creates kind of bad environment in the whole ecosystem. In order to prohibit this marketplace take `0.1` OSD to cancel sell.

### Referral reward

A referral reward is given to users whose referral project is successfully minted within expiry time. The reward is 1 OSD (might change) and it will be runing for limited time.


### Quiz game

> Quiz game is supposed to increase awareness about the project and reward to users.

In order to interact with users - the creators can run quiz games and reward them with OSD. There can be many quiz games but currently in ROADMAP is - 

1. Asking questions and right answerer will ge the reward. This help creators increase the awareness of the project.