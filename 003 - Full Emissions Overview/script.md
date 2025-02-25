We're going to go over how emissions work throughout the entire bittensor system.

Right now, every block, 1 TAO is emitted into the network.  This is reduced by half every 4 year halving.


1.  TAO pool emission Distribution

A total of 1 TAO is split between each subnet pool (TAO_in), the amount of TAO emitted into each subnet pool is it's current price divided by the sum of all subnet prices.  So if a subnet's price is currently 0.05, and we add up all the subnets prices and we get a value of 2, then the amount of tao emitted to this subnet's pool in 1 block is 0.05/2 = 0.025 TAO.  (it's actually ema EMA_price / EMA_sum)

2. Alpha pool emission distribution

Separately, every block, up to a maximum of 1 alpha is emitted to each subnet pool.  Just like the TAO emissions, this is reduced by half every 4 year halving.
Once we know the TAO emitted to the pool, we can calculate the alpha to be emitted into the pool.  So continuing our example, the price is 0.05, and 0.025 is being emitted to the pool, so 0.025/0.05 = 0.5 alpha will be emiited into the pool.

3. Alpha - Participant emissions per subnet

Separately, every block, 1 alpha is emitted to the participants.
Of this 1 alpha per subnet, 18% is awarded to the subnet owner, 41% to miners, and the last 41% is split between validators and their stakers.

The 41% miner rewards are given to miners based on how well they perform their subnet's task as determined by the subnet owner.

3a. Validator emission breakdown

The 41% validator rewards are given to validators based their vtrust, you can think of vtrust as how reliable a validator is, if the validator has high uptime and is quick to update their machines when subnet owners update their subnet's code, and the validator is properly checking miners (as the subnet owner says they should) the validator will have a higher vtrust.  see my yuma consensus video for how vtrust works in a little more detail.

So for staker rewards, the 41% of the 1 alpha awarded to validators is split between all the validators based on their stake weight which combines their TAO with their alpha in each subnet.

Remember you can stake in 2 ways:
  Stake TAO on the root subnet (subnet 0)
  Stake alpha on any subnet

Over time the proportion of emissions that go to alpha stakers will grow, incentivizing more investment in alpha.  At the time this video was made, we are here in the graph, if you're watching in a few months, we might be here.  So right now, let's say that root stakers get 90% of emissions.

Right now, there's a stronger emphasis on alpha (for example 1 alpha staked to subnet 9 is worth more for emissions on subnet 9 than 1 TAO).  Right now, alpha is has around 5x more impact on emissions than TAO.

Lets say that the taostats gets 20% of the emissions for subnet 9 (0.41 x 0.2 = 0.082).  We split that 0.082 into 2 piles: the rewards that go to root stakers, and the rewards that go to subnet stakers.  Remember our root proportion is at 90%.  This means that 90% of that 0.082 (0.074) alpha emission will be converted to TAO and awarded to TAO stakers.  The remaining 10% of that 0.082 (0.0082) will go to alpha stakers.

To find out your individual portion of this, you simply determine what percent of your validator's stake is your own.  If I own 10 TAO and my validator has a total of 100,000 TAO and alpha on the subnet, I'll get 10/100,000 = 0.01% worth of alpha every block (0.074 x 0.00001 = 0.00000074).  There are 7200 blocks in a day, so 0.00000074 x 7200 = 0.0053 alpha worth of tao per day for this subnet.

The same goes with the 8% of the alpha emissions that remain in alpha- it will be split between the alpha stakers staking to taostats.  If I have 10 alpha staked [or is it 10 TAO worth of alpha?], then i'll get 0.01% worth of the remaining 10% (0.0082) every alpha block (0.0082 * 0.00001 * 7200 = 0.0005904 alpha per day.


Notably, validators can set a "take", which is a portion of your alpha.  For most validators right now it's around 10%.  So your takehome will be reduced by approx 10% at the end. (fading numbers in the animation to reflect this)

Takeaways:
  Think of TAO emissions as affecting the market cap of bittensor, whereas alpha doesn't dilute bittensor's market cap, it's internal to the system and as of right now, all subnet alpha tokens are priced in TAO.  [need analogy for this...]
  You'll notice that 1 TAO is emitted every block, but more than 1 alpha is emitted every block.  So alphas retain their 21m max supply, but their halving schedules will be faster (less than 4 years) than TAO's halving.
  For 2025, it really matters where we are on the alpha weight/emissions graph, in 2026 and beyond, the ratio won't change much.
  what is interesting is that validators receive tao AND alpha for validating on a subnet.


  I think it's interesting to look at emissions and see the people behind the numbers.  The subnet owners take a big risk by purchasing their slot, they're like the entrepreneurs, if they're successful, their 18% cut will help them recoup their costs.
  The miners are the workers, not just any workers, but workers who are rewarded for their innovation and exceeding expectations.  They get a large 41% chunk of the emissions.
  Validators and their stakers are paid the remaining 41%.   Validators are paid for maintaining their machines running validation code and adding to the network.
  Alpha stakers are paid to find the most valuable subnets as fast as possible.
  Alpha stakers support subnets by increasing their subnet's payouts...
[need to think further about how to phrase this]

----------------------

As of this video, mar xx 2025, everything in this video is accurate, however bittensor is updated quite often and the way emissions work may change.  See the description for updates not reflected in the video.


