
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
In our example, 0.4 TAO isn't quite the final price you'll be paying, but it's very close.  There is a tiny flat fee for using the subnet pool at the time of this video it's 0.0005 TAO.  Slippage is more important to be aware of.  Slippage is similar to a fee in that you'll be paying a bit more to do your transaction.  The reason we call it slippage is because it difers from fees in 2 ways:
The amount you'll be paying in slippage is determined by the market
No one profits from slippage.

Slippage should be calculated by your wallet or app when you go to purchase alpha, but lets look at how its calculated.

In our example, if we send 1 TAO to the pool, at a price of 0.4 we might expect to get back 2.5 ALPHA.  2.5 multiplied by 0.4 is 1 tao.  Lets go deeper.

The number of TAO multiplied by the number of alpha in the pool is a value we call "k"; it sort of represents the total liquidity in the pool.  k stays the same during a transaction with the subnet pool.

In our example 40taox100alpha = 4,000 = k

When we send 1 TAO to the pool, there's now 41 TAO in the pool.

In order to balance the pool so that k stays the same (4,000), we need to reduce the alpha to 97.56.

41x97.56  = 4,000.

This reduction is a difference of 2.44 alpha.

So for our 1 TAO we'll actually receive 2.44 alpha.

Slippage is the difference between the expected price and what we actually received.
In this example the slippage was 0.06 alpha or 2.4%, pretty high.

To get the new price after our transaction, remember, we simply divide the number of TAO by the number of alpha: 41/97.56 = 0.42 TAO per alpha
we
-----------------
Now, lets reset our example and instead purchase only 0.1 TAO worth of alpha, so we might expect to receive 0.25 ALPHA.

There's now 40.1 TAO in the pool.

In order to balance the pool so that k stays the same at 4,000, we need to reduce the alpha to 99.751.

40.1 tao multiplied by 99.751 alpha keeps our K at 4000.
So for our 0.1 TAO we'll receive 0.249 alpha, which is a slippage of 0.001 alpha or 0.24%.  A better rate than the previous example.

The new price becomes 0.402.

-----------------
Now of course this works in the other direction as well, I won't bore you with any more math, but if we send that same 0.249 alpha back to the pool, we might expect to receive 0.1001 TAO due to the price increase from the last transaction.  We will actually receive 0.1 tao and the slippage was again 0.24%.  After our transaction, the price returns to 0.4 TAO per alpha.

As participants purchase and sell alpha, the equilibrium between the 2 sides of the pool shifts to make sure k stays constant.

Takeaways/Tips
------------------------
* Instead of buying large sums of alpha at once, consider buying small amounts over time to reduce slippage.  Dollar Cost Averaging (DCA) is your friend here.
* Over time, the amount of total liquidity (k) in every pool slowly increases via emissions.  So slippage on older subnets will be lower than on newer subnets, meaning that older subnets will be cheaper, as far as slippage goes, to transact with.
* I want to note that there is 1 key difference between a regular decentralized exchange liquidity pool and subnet pools:  No one owns the alpha nor TAO in bittensor's liquidity pools.  So there's no way to add liquidity to a pool and receive a yield like there is in a traditional liquidity pool, we'll breakdown how emissions grow the liquidity in subnet pools in another video.



TO FIX
-----------
Slippage is the difference between the expected price and what we actually received.

