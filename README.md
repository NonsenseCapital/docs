# Nonsense Capital
<sub>What's in a name?</sub> <br />

*A proof of concept DAO, to facilitate experimentation in the fields of governance and on-chain coordination between untrusted parties beyond simple decision making.*

Nonsense Capital is a "proof of concept" decentralized fund based on [Harbour](https://www.harbourproject.io/), [Melon](https://melonport.com/) and [Aragon](https://aragon.one/). The goal is to display how various ethereum-based protocols can be combined to build dynamic and fully functional projects.

## Problem Statement

**How do we incentivize users to participate, without making it more efficient to go off and run a fund of their own?**

@todo

*Notes* <br />
"there's a clear compromise between executing fast and executing well" - Oliver Nordbjerg

"So the optimal sized organization for any specific purpose is the balance between the benefits of being a single entity/organization, versus the tradeoff of coordination challenge.
<br /> <br />
Solving things like global warming/climate change can only be done at a global scale, but fund managmenet can be done nearly as effectively on the individual level" - Luke Duncan

## Overview

The goal of Nonsense Capital is to be purely governed by its token holders without any interference from outside parties. This requires an active community that is provided the various tools needed to fully run such a system. The fund will be a generic [Melonport](https://melonport.com/) fund, where the fund manager is an [Aragon](https://aragon.one/) DAO which is controlled through the voting process facilitated by [Harbour](https://harbourproject.io/), this allows us to piece together the various strengths of all these projects and provide a cohesive ecosystem. The connection between the voting-system and the fund will be easily built on top of aragon using their [ACL system](https://blog.aragon.one/introducing-aragonos-say-hi-to-modular-and-extendable-organizations-8555af1076f3). 

**Potential Benefits**
 * Hive mind
 * Less involvement
 * Pooled assets

**Potential Drawbacks**
 * Coordination on a large scale
 * User involvement

### Governance :globe_with_meridians:

The governance of Nonsense Capital is the most important aspect, the goal of the project is to keep the system as dynamic as possible while maintaining simplicity.

#### Proposal Types

In order for Nonsense Capital to achieve full autonomy, holders need to have the ability to create a variety of proposals. 

* **ICO Contributions**  This is one of the core proposal types. It is used to diversify assets into different ICOs. This proposal has ```yes``` or ```no``` voting options, but in addition, when a holder votes ```yes``` they can also pick from a range of percentages for how much of the funds holdings they would like to contribute. <br /> <br />
One of the issues that needs to be addressed is, if the popular percentage is shared by multiple options. The current solution is that if this ever encounter, an additional voting round will be held.

* **DAO Change**  This gives token holders the ability to 100% change every aspect of the DAO. These proposals execute automatically, and work by changing configuration values on the DAO, such as dividend rates, proposal creation costs etc.

* **Buy Proposal** This proposal allows token holders to vote on purchasing of an existing token. This functionality will work automatically through the usage of various exchanges connected to [Melonport](https://melonport.com/). Holders will have the option to vote from a range of 2-10% in increments of 2% for how much ETH they think the fund should use to buy more tokens.

* **Sell Proposal** This proposal allows token holders to vote on selling a token the DAO currently holds. It is planned that this functionality also works fully automatically by using decentralized as well as hopefully centralized exchanges connected to [Melonport](https://melonport.com/). Holders will be able to vote from a range of 10-100% in increments of 10% for how many tokens they think fund should sell.

#### Delegation

In order for less informed participants to not have to waste their votes, Nonsense Capital will implement a delegation system, currently it is unclear if this will be a liquid system or another form of delegation. But this will essentially allow users to delegate their votes to elected delegates or freely to other users they deem more fit to make decisions on their behalf.

**Representative democracy with Demarchy aspects?**

#### Optimization of philosophies through Forking

@TODO explain the benefits of forking and potential mechanisms as discussed in https://github.com/NonsenseCapital/docs/issues/2

#### Combatting Spam

##### Reputation :trophy:

In a fund based DAO like Nonsense Capital, a reputation system can offer large benefits, however the objectivity in something which is often subjective can be of great difficulty to implement inside of a smart contract. For that reason it can currently not be determined what kind of reputation system the DAO will use.

@TODO more

##### Time Cooldown :hourglass:

There will be a limit placed on the amount of proposals a single user can generate within 24 hours. The time cooldown period has not yet been decided upon, however this too will be one of the attributes that can be modified in the DAO. This along with the staking required to create a proposal will drastically reduce the size of the spam attack surface.

### Useless Token :moneybag:

Usless Tokens represent a share in Nonsense Capital, they can be staked in order to gain voting rights, these rights allow particpants to signal their investment opinions. This allows them to vote on as well as create various proposals. Usless Tokens are recieved when a particpant buys into Nonsense Capital, this is done by paying in a certain amount for which they will be allocated coins at the in proportion to the current value of the fund.

### Staking

For the staking system, the contracts used will conform to [ERC900](https://github.com/ethereum/EIPs/pull/910). Most likely the [Stakebank](https://github.com/HarbourProject/stakebank) contracts will be utilized. The goal of a staking model is to prevent sybil attacks, as well as require participants to show a certain involvment that motivates them enough to stake their tokens rather than potentially trading them on an open market. Participants should additionally be incentivized to stake, the question that needs to be answered however is how.

### Exiting

A user should be allowed to exit Nonsense Capital at anytime. This will reimburse the user with their respective assets for the amount of shares which they own. To demotivate users from exiting, there *should* be an exit fee which is paid whenever removing assets from the fund.


