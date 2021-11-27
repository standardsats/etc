## Problem
All economical activities of general citizens are measured in local currency units, while Lightning Network (LN) is a by-design monoasset network based on Bitcoin. Some services like Strike (and Chivo?) bridge this by implementing proprietary closed-loop settlement solutions for limited use cases. But the industry of ‘fiat denominated layers’ lacks of:

 - Interoperability across LN network with native properties
 - LN backward compatibility
 - Having fiat denominated accounts backed with sats
 - Instant hedge instrument against Bitcoin volatility for fiat-based business and new bitcoin users convenience

MCap of stablecoins surpassed $300B, making it a proven “glue” / bridge / layer of abstraction between fiat and bitcoin markets for centralized institutions. But stablecoin implementation on top of native bitcoin lightning “payment rails” still does not exist. And costs incurred for stablecoin settlements on any other networks are far away from day-to-day transactions standards, making the Bitcoin-based real-world economy dysfunctional.

## Solution

The proposal is based on recently announced “hosted channels” standard implementation (aka “custodial channels” or “host-channels”). Host-channels could be modified to support constant nominal value in fiat currency while being programmatically backed by corresponding amount of sats. The most advantageous part of the proposal is that payments from/to such fiat channels will be transferred on top of LN network original nodes w/o any limitations.

This way users can finally split the experience between fiat<–>Bitcoin while maintaining 100% compatibility with LN specifications. Technically client-side app generates standard LN messages / packets and host-side, after settling client-host fiat relations, provides routing of payments in the network according to the protocol rules.

## Market Opportunity

There is economical value in hosted channels itself (see [Liquidity abstraction in Lightning Network](https://notgeld.medium.com/liquidity-abstraction-in-lightning-network-3d7a1d76ac82)) however for average low-income user or small business owner the value proposition becomes especially important when Bitcoin experiences short term downward volatility. In any case we will always be recommending to drain hosted/fiat channels and swapping sats on to cold storage. Our vision is that Standard Sats will provide valuable service without need for being long-term custodian of the users funds.

Such channels might become the foundation for running native Bitcoin-banks of almost any scale, that target both global and local audience with minimized infrastructure and open-sourced client- and host-side code. Since the protocol itself might be open, the end user applications may be also open and modular. 

Possible use cases are limitless:

 - Instant global remittances in local currencies interop using LN rails with minimum possible FX spread
 - User/merchant can instantly control the exposure of his savings/current account into Bitcoin from 0% to 100% using slider or programmable logic, at a fraction of cost.
 - Convenient and interoperable local merchant trading denominated in fiat units.

The fiat-channel module for lightning node could be used both for:

 - trust-based community bank in the remote unbanked village
 - a submodule of a bank-application infrastructure for country-wide bank, integrated with KYC/AML

## Connecting Legacy Finance and Bitcoin Banks

A lightning node can be an organic part of OpenBankProject applications. We may consider two ways one can participate in a permissionless network and monetize its effect:

- Liquidity bridge
- Smaller community bank or a branch of	the larger bank

The first one may rely on third-party customer OBP API while the second one is supposed	to be driven by	more advanced subordinary-type OBP API.	Creation of the	new bank with bank-correspondent demands significantly larger resources so we are focusing on bridging-like functionality of our service. In this case, the user may deposit money via standard bank transfer and, when funding is confirmed, invoke a fiat channel. The stable fiat-denominated value will allow to utilize liquidity without rush and mindfully plan business-activity related to the freshly created channel.

We believe that sats will become a standart!
