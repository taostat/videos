We're going to go over how emissions work throughout the entire bittensor system.

Right now, every block, 1 TAO is emitted into the network.  This is reduced by half every 4 year halving.


1.  TAO pool emission Distribution

A total of 1 TAO is split between each subnet pool (TAO_in), the amount of TAO emitted into each subnet pool is it's current price divided by the sum of all subnet prices.  So if a subnet's price is currently 0.05, and we add up all the subnets prices and we get a value of 2, then the amount of tao emitted to this subnet's pool in 1 block is 0.05/2 = 0.025 TAO.  (it's actually ema EMA_price / EMA_sum)

2. Alpha pool emission distribution

Separately, every block, up to a maximum of 1 alpha is emitted to each subnet pool.  Just like the TAO emissions, this is reduced by half every 4 year halving.
Once we know the TAO emitted to the pool, we can calculate the alpha to be emitted into the pool.  So continuing our example, the price is 0.05, and 0.025 is being emitted to the pool, so 0.025/0.05 = 0.5 alpha will be emiited into the pool.

3. Alpha - Participant emissions per subnet

Separately, every block, 1 alpha is emitted to the subnet participants.  As with the TAO emissions, this is reduced by half every 4 year halving.
Of this 1 alpha per subnet, 18% is awarded to the subnet owner, 41% to miners, and the last 41% is split between validators and their stakers.

The 41% miner rewards are given to miners based on how well they perform their subnet's task as determined by the subnet owner.

3a. Validator emission breakdown

The 41% validator rewards are given to validators based their vtrust, you can think of vtrust as how performant a validator is, if the validator has high uptime and is quick to update their machines when subnet owners update their subnet's code, and the validator is properly checking miners (as the subnet owner says they should) the validator will have a higher vtrust.  see my yuma consensus video for how vtrust works in a little more detail.

Validators can use a feature called "child hotkey".  This allows a validator to NOT validate on a subnet, but instead point their weight (in staked TAO and alpha) to another validator for a particular subnet to receive a portion of their weight.  We'll do another video on child hotkeys [or do we already have one...? I thought doug did one, maybe just ignore child hotkeys for this vid?]

Remember you can stake in 2 ways:
  Stake TAO on the root subnet (subnet 0)
  Stake alpha on any subnet

Over time the proportion of emissions that go to TAO vs alpha will tip more to benefit alpha stakers than TAO stakers. [to rephrase]

So for staker rewards, the 41% of the 1 alpha awarded to validators is split between all the validators based on their stake weight which combines their TAO with their alpha in each subnet.  With a stronger emphasis on alpha (for example 1000 alpha staked to subnet 9 is worth more for emissions on subnet 9 than 1000 TAO).  Right now, alpha is worth around 5x more than TAO for calculating stake weight, but this may be adjusted in the future.

Lets say the taostats gets 10% of the emissions for subnet 9.  We split that 10% into 2 piles: the rewards that go to root stakers, and the rewards that go to subnet stakers.  Lets say the root proportion is at 20%.  This means that 20% of that 10% (2%) alpha emission will be converted to TAO and awarded to stakers.  The remaining 80% of that 10% (8%) will go to alpha stakers.
[maybe talk here about validator "take"]

The 2% of the alpha emission that is converted to TAO will be split between all of the root stakers staking to taostats.  [In a proportional way, what are the words here...]

The same goes with the 8% of the alpha emissions that remain in alpha- it will be split between the alpha stakers staking to taostats.



Takeaways:
  Think of TAO emissions as affecting the market cap of bittensor, whereas alpha doesn't dilute bittensor's market cap, it's internal to the system and as of right now, all subnet alpha tokens are priced in TAO.  [need analogy for this...]


  I think it's interesting to look at emissions and see the people behind the numbers.  The subnet owners take a big risk by purchasing their slot, they're like the entrepreneurs, if they're successful, their 18% cut will help them recoup their costs.
  The miners are the workers, not just any workers, but workers who are rewarded for their innovation and exceeding expectations.  They get a large 41% chunk of the emissions.
  Validators and their stakers are paid the remaining 41%.   Validators are paid for maintaining their machines running validation code and adding to the network.  Alpha stakers are paid to find the most valuable subnets as fast as possible.
[need to think further about how to phrase this]

----------------------

As of this video, mar xx 2025, everything in this video is accurate, however bittensor is updated quite often and the way emissions work may change.  See the description for updates not reflected in the video.


