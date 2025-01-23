## Satoshi Machine

Community-driven open-source Bitcoin machine software to decentralize liquidity provision in the machine. Our goal is allowing anyone to pool their sats and cash to earn fees, providing income for local communities while removing the burden of liquidity maintenance from a sole operator.

![image](https://storage.googleapis.com/geyser-images-distribution-prod-us/5b6eaa31-40de-467a-bff3-43be8111dc49_btm/image_large.webp)

There may be multiple implementations to this, including varying pricing mechanisms, for example:
- Sourcing Bitcoin price externally
  - the price is always fair
  - liquidity providers are buying/selling at the market price plus margin
  - the machine may run out of liquidity on one side
- Constant-Product AMM
  - the machine maintains a constant product equation: $supply_{BTC} * supply_{cash} = k$
  - the price is calculated as $p = supply_{cash}/supply_{BTC}$
  - thus every trade is guaranteed, but the price gets progressively worse with size and liquidity imbalance
  - as liquidity gets imbalanced to one side, this pricing mechanism incentivizes people to trade in the opposite direction
- Custom Price Curves
  - we can think of a price curve that follows externally sourced Bitcoin price when there's a healthy balance of liquidity
  - within a certain range of $supply_{cash}/supply_{BTC}$ the price is sourced from external markets
  - outside that range the price is determined by Constant Product
  - the price is fair while the liquidity is healthy
  - when liquidity is imbalanced the price is skewed to incentivize the traders to trade in the opposite direction

This is a space for collaboration and contribution from all of you. Please offer your thoughts and proposals.
