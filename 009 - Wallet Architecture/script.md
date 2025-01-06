Lets disambiguate between hotkey, coldkey, hot wallet, cold storage.

"hot wallet" and "cold storage" are general crypto concepts.  A hot wallet is a wallet that has performed a transaction on the blockchain, whereas cold storage refers to a wallet that has never been connected to an internet-connected computer- a wallet that is very secure.  You can receive crypto to a cold storage wallet.  However once you send crypto from that cold storage wallet, you'll have turned it into a hot wallet.  Hot wallets are less secure than cold storage.

These are not to be conflated with "hotkeys" and "coldkeys", these are bittensor-specific concepts.

If you are a regular user or staker, when you create a wallet in your wallet app, you'll be given a 12 or 24 word phrase to securely write down.  Those words are called a nmemonic, your nmemonic allows you to access your funds, they are your "coldkey".  If your computer gets hit by a meteor or otherwise destroyed, and you've physically written down the nmemonic on a piece of paper and stored it, you'll still be able to recover your funds using the nmemonic on any other computer.  When you send TAO to a friend via a wallet app, you're sending TAO from your coldkey to your friend's coldkey.  Wallet apps don't create hotkeys.

Miners and validators are the only ones who create hotkeys.

**Miners**

Miners use hotkeys to register on subnets.  Before a miner registers on a subnet, they create a hotkey.  The registration process associates their hotkey with a slot in the subnet.  Mining rewards are distributed to hotkeys.  Then miners move the funds from their hotkey to their coldkey then they sele their rewards on an exchange by sending their TAO from their coldkey to an exchange.  Many hotkeys can be associated with one coldkey, this is useful for miners who use multiple miner slots or who mine on multiple subnets.

**Validators**

Each validators has 1 hotkey that allows users to stake to them.

So if you're staking, you'll be staking to your favorite validator's hotkey.  The way this works is that you tell the blockchain which validator's hotkey you want to stake your coldkey funds with.  The funds move from your coldkey (or wallet) to a spreadsheet in the blockchain that associates your coldkey with the validator's hotkey.  At no point does the validator have access to your funds.  When you want to unstake, the blockchain simply puts your staked funds back into your wallet and deletes the entry from the staking spreadsheet.

So in summary:
* A coldkey is a traditional crypto wallet.
* A hotkey is used by validators for staking and by miners for mining.
* A hot wallet is a wallet that has sent a transaction.
* A cold wallet (or cold storage) is a wallet that has been generated offline by a device that will never touch the internet.
