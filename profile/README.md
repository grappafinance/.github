
<div align="center">
  <h1 > Welcome to Grappa Finance</h1>
  
  <img height=80 src="https://avatars.githubusercontent.com/u/121327714"> </image>

  <h4 align="center"> An option protocol connecting DeFi derivatives liquidity </h4>
  
<p align='center'>
    <img src='https://i.imgur.com/A04IOW6.jpg' alt='grappa' width="520" />
</p> 

<div style="max-width:550px">
<p align="center" style="font-size:2vw;color:grey">
  Grappa is a grape-based pomace brandy originally made to prevent waste by using leftovers. We believe there are lots of waste in capital when it comes to DeFi options, and we are here to change that.
  </p>
</div>
</div>

## Introduction

Grappa is a project dedicated to establishing an open and permissionless foundation, with the objective of advancing the DeFi options space.

We firmly believe that the core principles of DeFi are composability and decentralization. Currently, the DeFi options landscape faces significant challenges due to liquidity fragmentation. This primarily arises from the absence of a reliable foundational layer that can gain unanimous consensus for building.

Grappa aims to be the shared settlement layer that everyone can agree on, enabling maximized composability across various protocols. It will provide a solid foundation for diverse risk management and parameter choices, facilitating seamless options exchange across a wide range of products.

## What Exactly Are We Building

### 1. Shared Settlement Layer: `Grappa` Contract

At the core of our project is a permissionless contract that's designed to settle any instrument with a predefined expiry and a fixed value determined at that expiry. This encompasses instruments akin to cash-settled European call or put options, as well as spreads (e.g., call or put spreads) and even exotic options such as the "up-and-out call option". More about this central contract can be found in our [core-cash](https://github.com/grappafinance/core-cash) repository.
By our design, each "instrument" can be minted by different "margin engines." While these engines share the same settlement logic, the tokens they create are non-fungible, and their risks are entirely separate. Through this architecture, we decouple the margining logics from the settlement logic, making it possible for different engines to develop their own products, while the shared settlement logic ensures the possibility of liquidity exchange.

Once we have multiple engines and oracles built, we can maximize the strength of Grappa and build a liquidity exchange AMM on top of different margin engines.

### 2. Different Risk Engines

Currently, we are in the process of developing three distinct engines that will be connected to the Grappa contract:
1. [Full collat Engine](https://github.com/grappafinance/full-collat-engine)
2. [Cross Margin Engine](https://github.com/grappafinance/cross-margin-engine)
3. [Partial collat engine](https://github.com/grappafinance/partial-collat-engine)

These engines will suit different needs for different option products, and we welcome anyone to build premissionless Apps on top of these engines.

### 3*. The `Pomace` Contract

In contrast to the Grappa contract, which settles instruments akin to "cash-settled" options, the Pomace contract is designed to facilitate "physical" settlement of assets. For instance, it handles physically settled options wherein, on the day of expiry, a long holder can exercise their right to swap the assets at a predetermined price, provided they possess an option token. More details about this can be found in our [core-physical](https://github.com/grappafinance/core-physical) repository.

Following a similar architecture as `Grappa`, we permit various engines to mint "similar" option tokens with identical terms, but with different engines backing the liquidity. Currently, only the [Cross Margin Engine](https://github.com/grappafinance/cross-margin-engine) supports the Pomace contract.

## Funding

This project is fully open-source and publicly funded via [Gitcoin](https://gitcoin.co/grants/7713/grappa-finance).
