* in dtao, each subnet will have its own token (alpha, beta, gamma, ...) . Emissions in each subnet will no longer be in tao, but paid in the token of that subnet. For simplicity, we refer to subnet tokens generically as alpha.

* The only way to buy alpha tokens is through tao. The only way to sell alpha tokens is to buy tao.

* Purchase and sale of alpha and tao is through the use of liquidity pools.

* Bittensor terms are tao_in and alpha_in (the amounts of tao/ alpha in the LP)

* The “value” of alpha is tao_in/alpha_in

* Buying alpha - add tao to LP.. receive alpha_out staked to a validator.

* Alpha_in * tao_in =k there is a constant that the two sides of the pool must add up to.

* Every block: tao emission is added to tao_in (or alpha emission is added to alpha in).. AND one alpha is added to alpha_staked (to split amongst SN owner, miner, valis and stakeholders)

* This changes k buy however much is added in….

* IDK if we bring in slippage?
	* Slippage - if you buy alpha with tao, you get alpha based on the new exchange rate with your added tao in the pool.s o you always get a little bit less than you expected.