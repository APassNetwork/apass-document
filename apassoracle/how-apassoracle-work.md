---
description: Explore the decentralized APassOracle networks(beta) powered by Apters.
---

# 🔵 How APassOracle Work

APass system allow apters who hold APass NFT to mine additional $APC tokens every 24 hours as a reward. When mining tokens, apters upload feeds or datas to the chain through browsers, distributedly.

The AOracle whole plan will be divided into three steps:

#### Step 1: Centralization (Currenry Status)

The trusted nodes use the aggregation engine to collect data, pack it into small data packets and sign them. Submitted by user distribution. After the contract verification signature is passed, the oracle round is updated.

#### Step 2: Hybrid Centralization/Decentralization

When the user distribution submission frequency is reduced to a maximum delay of 60 seconds within 24 hours, the aggregation engine is placed on the front end (in browsers, user web client), and the user packs and signs locally. Submitted by user distribution. The contract receives >=10 submissions. If the data with an excessive offset value is removed and the package deviation from the feasible node does not exceed 1%, the oracle round will be updated, otherwise it will be rejected. In this process, start to record the user's data stability, and start to score its accumulation.

#### Step 3: Pure Decentralization

When the user distribution submission frequency is reduced to 24 hours and the maximum delay is within 15 seconds, the aggregation engine will be front-loaded and fully signed by the user locally. Apters who provide credible data with a high-scoring quota have higher weights. If the deviation from others exceeds 1%, the data will be discarded and weighted points will be deducted until it reaches zero(be banned). To keep one single sound, more than 10 people must provide data, and the consistency exceeds 50%.

As apters interact more frequently, the solution becomes more reliable. Apters mint $APC tokens and submit data feeds at the same time, also they are working for the whole Aptos ecosystem. These $APC tokens will be used for other consumption within our ecosystem, and we will gradually recycle and destroy it.

Now, The market data feeds are powered by Apters, which is free for the ecosystem to use forever.

Soon, the AOracle will provide VRF (Verifiable source of randomness), HTTP API and CCP (Cross-Chain Proof) services, which are additional services that need to pay $APC fees to use. The fees will be used to buy back $APC for destruction as a reward for data submitters.
