
What are liquidity pools, and how will they work in bittensor?

For clarity: Liquidity pools, alpha pools, and subnet pools all refer to the same thing.  We're going to refer to them in this video as subnet pools.

Subnet pools
------------------------
A subnet pool contains a bucket of TAO and a bucket of alpha.

When you send TAO to the pool, you receive alpha staked to a validator.

When you send alpha to the pool you receive TAO.

Lets say there is a pool that has a total of 40 TAO and 100 alpha.

When you go to actually purchase alpha, you'll see the price.

The price for alpha is calculated by dividing the # of TAO in the pool by the # of alpha in the pool.

In our case this is 40 / 100 = 0.4 TAO per alpha


Slippage
------------------------
In our example, 0.4 TAO isn't quite the final price you'll be paying, but it's very close.  There are no fees for using the subnet pool, but there is slippage.  Slippage should be calculated by your wallet or app when you go to purchase alpha, but lets look at how its calculated.

The number of TAO multiplied by the number of alpha in the pool is a value we call "k"; it sort of represents the total liquidity in the pool.  k stays the same during a transaction with the subnet pool.

In our example 40x100 = 4,000 = k

If we send 1 TAO to the pool, there's now 41 TAO in the pool.

In order to balance the pool so that k stays the same (4,000), we need to reduce the alpha to 97.6.

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

The new price is 40.1/99.751 = 0.41 TAO per alpha


Takeaways/Tips
------------------------
* Instead of buying large sums of alpha at once, consider buying small amounts over time to reduce slippage.  Dollar Cost Averaging (DCA) is your friend here.
* Over time, the amount of total liquidity (k) in every pool slowly increases via emissions [see another video for how emissions work].  So slippage on older subnets will be lower than on newer subnets.
* I want to note that there is 1 key difference between a regular decentralized exchange liquidity pool and subnet pools:  No one owns the alpha nor TAO in bittensor's liquidity pools.  So there's no way to add liquidity to a pool and receive a yield like there is in a traditional liquidity pool.

