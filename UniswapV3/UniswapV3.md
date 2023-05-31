Uniswap V3
===

## Table of Contents

[TOC]

## Introduction

Different from V2!

1. Increased capital efficiency
2. Fine-tuned control to liquidity providers
3. Improve accuracy and convenience of the price oracle
4. Has more flexible fee structure
   
constant product market maker formula是沒效率的（用在V1,V2）,只有小比例流動池中的資產可以在適當的價格交易

1. 集中流動性：流動性提供者（LPs）能夠通過在任意價格範圍內"限制"其流動性，從而提高池的資本效率，並允許LPs近似其首選的儲備曲線，同時與池的其他部分高效地聚合。
2. 彈性費用：交換費用不再被鎖定在0.30％。相反，每個池（每個資產對可以有多個池）的費用檔位在初始化時設定。
初步支持的費用檔位為0.05％、0.30％和1％。UNI治理可以在此集合中添加其他值。
3. 協議費用治理：UNI治理在設定協議收取的交換費用比例方面具有更大的靈活性（第6.2.2節）。

4. 改進的價格預測器：Uniswap v3提供了一種讓用戶查詢最近價格累加器值的方式，從而避免了在測量TWAP的期間必須在準確開始和結束時對累加器值進行檢查點的需求（第5.1節）。

5. 流動性預測器：合約提供了一個時間加權平均流動性預測器（第5.3節）。



Concentrated Liquidity
---

### Range Orders

ARCHITECTURAL CHANGES
---
### Multiple Pools Per Pair
### Non-Fungible Liquidity

GOVERNANCE
---

ORACLE UPGRADES
---
### Oracle Observations
### Geometric Mean Price Oracle
### Liquidity Oracle

IMPLEMENTING CONCENTRATED LIQUIDITY
---
### Ticks and Ranges
### Global State
### Tick-Indexed State
### Position-Indexed State


## REFERENCES

[1] Hayden Adams, Noah Zinsmeister, and Dan Robinson. 2020. Uniswap v2 Core. Retrieved Feb 24, 2021 from https://uniswap.org/whitepaper.pdf

[2] Guillermo Angeris and Tarun Chitra. 2020. Improved Price Oracles: Constant Function Market Makers. In Proceedings of the 2nd ACM Conference on Advances in Financial Technologies (AFT ’20). Association for Computing Machinery, New York,NY,UnitedStates,80–91. https://doi.org/10.1145/3419614.3423251

[3] Michael Egorov. 2019. StableSwap - Efficient Mechanism for Stablecoin Liquidity. Retrieved Feb 24, 2021 from https://www.curve.fi/stableswap-paper.pdf

[4] Allan Niemerg, Dan Robinson, and Lev Livnev. 2020. YieldSpace: An Automated Liquidity Provider for Fixed Yield Tokens. Retrieved Feb 24, 2021 from https: //yield.is/YieldSpace.pdf

[5] Abraham Othman. 2012. Automated Market Making: Theory and Practice. Ph.D. Dissertation. Carnegie Mellon University.

