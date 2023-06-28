
<div align="center">
  <h1 > Welcome to Grappa Finance</h1>
  <h3 style="font-size:2.2vw;color:grey">
  An option protocol that focuses on composability and capital efficiency.
  </h3>
  <img height=60 src="https://i.imgur.com/vSIO8xJ.png"> </image>

  <h5 align="center"> Don't waste your capital.</h5>
  
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

Grappa is a project driven to establish an open, permissionless foundation that aims to advance the DeFi options space.

We hold the conviction that the key principles of DeFi are composability and decentralization. Presently, the DeFi options realm is facing significant hurdles due to liquidity fragmentation. This is largely because there isn't a reliable base layer that everyone feels secure building upon.

Grappa strives to become this base layer, answering a variety of needs, while also offering an efficient exchange layer (aggregator). This will enable individuals to exchange options across diverse products with ease.

## Funding

This project is fully open-source and publicly funded via [Gitcoin](https://gitcoin.co/grants/7713/grappa-finance).

## What Exactly Are We Building??

### 1. The `Grappa` Contract

At the core of our project is a permissionless contract that's designed to settle any instrument with a predefined expiry and a fixed value determined at that expiry. This encompasses instruments akin to cash-settled European call or put options, as well as spreads (e.g., call or put spreads) and even exotic options such as the "up-and-out call option". More about this central contract can be found in our [core-cash](https://github.com/grappafinance/core-cash) repository.

Each "instrument" can be minted by different "engines". While these engines share the same settlement logic, the tokens they create are non-fungible, and their risks are entirely separate. Currently, we are in the process of developing three distinct engines that will be connected to the Grappa contract:
1. [Cross Margin Engine](https://github.com/grappafinance/cross-margin-engine)
2. [Full collat Engine](https://github.com/grappafinance/full-collat-engine)
3. [Partial collat engine](https://github.com/grappafinance/partial-collat-engine)


### 2. The `Pomace` Contract

In contrast to the Grappa contract, which settles instruments akin to "cash-settled" options, the Pomace contract is designed to facilitate "physical" settlement of assets. For instance, it handles physically settled options wherein, on the day of expiry, a long holder can exercise their right to swap the assets at a predetermined price, provided they possess an option token. More details about this can be found in our [core-physical](https://github.com/grappafinance/core-physical) repository.

Following a similar architecture as `Grappa`, we permit various engines to mint "similar" option tokens with identical terms, but with different engines backing the liquidity. Currently, only the [Cross Margin Engine](https://github.com/grappafinance/cross-margin-engine) supports the Pomace contract.
