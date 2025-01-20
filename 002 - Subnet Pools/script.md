
What are subnet pools, and how do they work in bittensor?

For clarity: Liquidity pools, alpha pools, and subnet pools all refer to the same thing.  We're going to use the term subnet pools.

Before we start, recall that alpha is essentially a staked token in a subnet.  Similar to shares that pay dividends.

Subnet pools
------------------------
Subnet pools are the way that we buy and sell alpha in subnets.  If you want to purchase alpha in a subnet, the only way to get it is through it's subnet pool.

When you send TAO to a pool, you receive alpha.

When you send alpha to a pool you receive TAO.

A subnet pool contains a bucket of TAO and a bucket of alpha.

Lets say there is a pool that has a total of 40 TAO and 100 alpha.

The price for alpha is calculated by dividing the # of TAO in the pool by the # of alpha in the pool.

In our case the price is 40 TAO divided by 100 alpha, which makes a price of 0.4 TAO per alpha


Slippage
------------------------
In our example, 0.4 TAO isn't quite the final price you'll be paying, but it's very close.  There are no fees for using the subnet pool, but there is slippage.  Slippage is similar to a fee in that you'll be paying a bit more to do your transaction.  The reason we call it slippage is because it difers from fees in 2 ways:
The amount you'll be paying in slippage is determined by the market
No one profits from slippage.

Slippage should be calculated by your wallet or app when you go to purchase alpha, but lets look at how its calculated.

The number of TAO multiplied by the number of alpha in the pool is a value we call "k"; it sort of represents the total liquidity in the pool.  k stays the same during a transaction with the subnet pool.

In our example 40x100 = 4,000 = k

If we send 1 TAO to the pool, there's now 41 TAO in the pool.

In order to balance the pool so that k stays the same (4,000), we need to reduce the alpha to 97.56.

41x97.56  = 4,000.

So for our 1 TAO we'll receive 2.44 alpha: that's a rate of 0.410 TAO per alpha.

In this example the slippage was 0.01 TAO per alpha or 2.5%, brutal.

To get the new price remember, we simply divide the number of TAO by the number of alpha: 41/97.56 = 0.42 TAO per alpha

-----------------
Now, lets reset our example and instead purchase only 0.1 TAO worth of alpha.

40x100 = 4,000 = k

If we send 0.1 TAO to the pool, there's now 40.1 TAO in the pool.

In order to balance the pool so that k stays the same (4,000), we need to reduce the alpha to 99.751.

40.1 x 99.751  = 4,000.

So for our 0.1 TAO we'll receive 0.249 alpha: that's a rate of 0.402 TAO per alpha.  A better rate than the previous example.

In this example the slippage was 0.002 TAO per alpha or 0.5%, much better.

After our transaction, the new price is 40.1/99.751 = 0.402 TAO per alpha

-----------------
Now of course this works in the other direction as well, I won't bore you with any more math, but if I send 1 alpha to the pool, I will receive X and my slippage was Y, or Z%.  After our transaction, the price becomes B TAO per alpha.

As participants purchase and sell alpha, the equilibrium between the 2 sides of the pool shifts to make sure k stays constant.

Takeaways/Tips
------------------------
* When you purchase alpha, you'll be prompted to pick a validator to stake your alpha with.  You'll want to choose a validator that you think is doing a good job and is beneficial to the subnet.
* Instead of buying large sums of alpha at once, consider buying small amounts over time to reduce slippage.  Dollar Cost Averaging (DCA) is your friend here.
* Over time, the amount of total liquidity (k) in every pool slowly increases via emissions [see another video for how emissions work].  So slippage on older subnets will be lower than on newer subnets, meaning that older subnets will be cheaper, as far as slippage goes, to transact with.
* I want to note that there is 1 key difference between a regular decentralized exchange liquidity pool and subnet pools:  No one owns the alpha nor TAO in bittensor's liquidity pools.  So there's no way to add liquidity to a pool and receive a yield like there is in a traditional liquidity pool.



TO FIX
-----------

Buying small amounts over time is a common investment strategy called dollar cost averaging (DCA) usually used to reduce exposure to volatility, but in a bittensor subnet pool it may help reduce slippage as well.

* When you purchase alpha, you'll be prompted to pick a validator to stake your alpha with.  You'll want to choose a validator that you think is doing a good job and is beneficial to the subnet.

So in our example 40 TAO divided by 100 alpha, makes a price of 0.4 TAO per alpha

Another example (unstaking)

You might be wondering why I used the word per instead of a slash when I referred to tao per alpha.  This is because the slash in trading doesn't mean the same thing as a slash in math.  When we refer to the bitcoin price we usually denote it like this (100k btc/usdt), despite how it's written it doesn't mean 100k bitcoin per usdt, it means 100k usdt per bitcoin.
