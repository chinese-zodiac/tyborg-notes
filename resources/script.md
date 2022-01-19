---
description: In-game currency stablecoin with loose USD peg.
---

# Script

Script is the primary in-game currency for trading, paying fees, and making regular everyday purchases. Script is backed by Gold and is loosely pegged to 1 USD using bonds and rebase. Whenever Script is worth more than 1.05 USD, new Script is minted to accounts staking GOLD in the Reserve. When Script falls below 0.95 USD, the Reserve opens Treasury Bonds which can be minted by burning Script and redeemed when Script is between 1.00 and 1.05 USD. Thus the Script supply expands when over peg (expansionary epochs) and decreases when under peg (contractionary epochs).&#x20;

Script and Bonds are not transferrable outside of the Tyborg game. They can be used in in-game marketplaces, banks, and can be transferred between players in the same location.

Whenever Script is used in game, there is a 3% transaction fee. Additionally, all Script spent on subscriptions is burned.

### Epochs

Each epoch is 8 hours. The TWAP of the Script/USD pair in the capital money market is used to determine the type of epoch - whether it is expansionary, contractionary, or stable.

#### Expansionary Epoch

An expansionary epoch is one where the TWAP was over 1.05 at the end of the epoch. The table below determines the minting of new Script. 80% of Script is minted to the Gold Reserve stakers and 20% is minted to the Empire Treasury and sold.

| Supply    | Mint  |
| --------- | ----- |
| >1m       | 3%    |
| 1m-4m     | 2.5%  |
| 4m-8m     | 2%    |
| 8m-16m    | 1.5%  |
| 16m-40m   | 1.25% |
| 40m-100m  | 1%    |
| 100m-500m | 0.75% |
| 500m-2b   | 0.5%  |
| 2b+       | 0.25% |

During expansionary Epochs, TBONDS can be redeemed for SCRIPT with a redemption bonus of 10%.

#### Contractionary Epoch

No Script can be minted during Contractions. Contractions are triggered when the Script TWAP for the 8 hour epoch is below 0.95. 3% of the Script supply can be minted as TBOND per epoch with a debt cap of 35% (TBOND supply divided by SCRIPT supply must be less than 0.35). TBONDs can be minted at the Reserve Bank with 1 SCRIPT burned for 1 TBOND.

#### Stable Epochs

No Script is minted during Stable Epochs. TBONDS can be redeemd at a rate of 1 TBOND for 1 SCRIPT with no redemption bonus.

## Subscription Tiers

Subscription gets energy, energy is used for all the game for every action, the tiers are estimates for fights but actual energy would be also used on trading, events, inventory, traveling, and any other in-game action that alters the game state. The subscription is either burned by the Tyborg holding the subscription, or when creating a new Tyborg is burned by the wallet minting the new Tyborg. When a new, higher level subscription is added, the remaining time in the current subscription level is moved to the end of the current subscription.&#x20;

All subscriptions are paid in Script, excluding subscriptions provided in airdrop events. New Subscriptions are ERC721s minted in the Registration Office structure.

<table><thead><tr><th>Title</th><th data-type="number">Script per month</th><th data-type="number">Energy Cap</th><th data-type="number">Energy per Day</th></tr></thead><tbody><tr><td>TBD </td><td>5</td><td>150</td><td>100</td></tr><tr><td>TBD </td><td>15</td><td>800</td><td>400</td></tr><tr><td>TBD </td><td>30</td><td>3000</td><td>1000</td></tr><tr><td>TBD </td><td>50</td><td>8000</td><td>2000</td></tr><tr><td>TBD </td><td>80</td><td>20000</td><td>4000</td></tr><tr><td>Hedge Knight</td><td>120</td><td>70000</td><td>10000</td></tr></tbody></table>

## Earning Script

### Hunting

All resources dropped by Hunts can be sold for Script. Hunt creatures with rarer drops that are worth more on the Markets. Each Market will have a different rate, so check the local Market rates or travel to a different province to get better prices.

### Land

When Tyborgs use your structures, you can set a fee they pay in Script. Attract more Tyborgs to your land to increase your earnings. Build structures that Tyborgs use to earn some of their Script.

### Trade

In game markets can have different prices. Rarer resources are easier to find farther from the capital and may be cheaper in some provinces. Tyborgs can carry resources between markets to arbitrage price differences. Additionally, many rare collectibles and resources can fluctuate in value over time providing many trading opportunities for the Tyborg with an unusually mercenary mind.

### Staking Gold

In Banks, Tyborgs can deposit Gold to earn Script mints from rebases during expansionary epochs, when Script is over $1.&#x20;

### Staking USDC

USDC ([1USDC](https://explorer.harmony.one/address/0x985458e523db3d53125813ed68c274899e9dfab4)) can be staked in the Money Market as liquidity. Deposit USDC which is automatically converted in USDC/SCRIPT liquidity. You can withdraw your USDC at any time. Earnings are in SCRIPT.

USDC staking has no impermanent loss. When you withdraw your stake, you will receive USDC equal in value to your original deposit. In some uncommon cases, part of the redemption will be in Script.

There is a 1% withdraw fee when unstaking USDC.

### Investing

Landlords may also have their own bank branches accepting deposits and promising a return based on the output of their Land - but beware of unscrupulous Landlords who may decide to confiscate the assets of the bank, or lazy Landlords who let their Bank degrade and default.
