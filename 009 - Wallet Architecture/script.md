Lets disambiguate between hotkey, coldkey, private key, public key, hot wallet, cold storage.

"hot wallet" and "cold storage" are general crypto concepts.  A hot wallet is a wallet that has performed a transaction on the blockchain, whereas cold storage refers to a wallet that has never been connected to an internet-connected computer- a wallet that is very secure.  You can receive crypto to a cold storage wallet.  Typically, sending crypto from that cold storage wallet turns that wallet into a hot wallet, though there are ways around this.  I'll do a video on how to safely do transactions like staking from a cold wallet in another video.  Hot wallets are less secure than cold storage, hot wallets are susceptible to viruses, keyloggers, hacks, etc, whereas cold wallets are not.

These are not to be conflated with "hotkeys" and "coldkeys", these are bittensor-specific concepts.

If you are a regular user or staker, when you create a wallet in your wallet app, you'll be given a 12 or 24 word phrase to securely write down.  Those words are called a mnemonic, your mnemonic allows you to access your funds, they are your "coldkey".  If your computer gets hit by a meteor or otherwise destroyed, and you've physically written down the mnemonic on a piece of paper and stored it, you'll still be able to recover and access to your funds using the mnemonic on any other computer.  Wallet apps don't create hotkeys.

When you send TAO to a friend via a wallet app, you're sending TAO from your coldkey to your friend's coldkey.

Public keys and Private keys are also general crypto concepts.  A crypto wallet consists of 2 parts:
* A public key is a bunch of letters and numbers that you can tell anyone, it's public.  In bittensor, typically it starts with a 5.  If you want to receive crypto, you have to provide your public key to the sender for them to know where to send it.  If you want to check your wallet balance on taostats.io you can simply put the public key into the search and find your wallet's balance.
* A private key is the real thing to keep secret.  It's a longer bunch of letters and numbers that you never tell anyone, it's private.  Your private key allows you to transfer funds out of your wallet.  You can recreate your private key and public key with your mnemonic, so safely store and protect your mnemonic.  If anyone gets access to your private key or mnemonic, they can steal your funds.

A simple way to think about this is that your public key is your bank account number (it allows you to receive money), and your private key is the password or pin for your bank account.

So to be abnoxiously specific, when you send TAO to a friend via a wallet app, the wallet app is using your wallet's private key to send TAO from your coldkey wallet to your friend's coldkey's public key.  Similar to using your password to login to your bank account to send money to a friend's bank account number.

In bittensor, if someone asks you for your coldkey, they're asking you for the public key of your wallet in order to see your account balance or send you money.  Again, never send your private key to anyone, it's private.

Hotkeys are another type of wallet in bittensor.

Miners and validators are the only ones who create hotkeys.

**Miners**

Miners use hotkeys to register on subnets.  Before a miner registers on a subnet, they create a hotkey.  The registration process associates their hotkey with a slot in the subnet.  Mining rewards are distributed to hotkeys.  Then miners move the funds from their hotkey to their coldkey then they sele their rewards on an exchange by sending their TAO from their coldkey to an exchange.  Many hotkeys can be associated with one coldkey, this is useful for miners who use multiple miner slots or who mine on multiple subnets.

**Validators**

Validators use hotkeys to allow users to stake to them.

So if you're staking, you'll be staking to your favorite validator's hotkey.  The way this works is that you tell the blockchain which validator's hotkey you want to stake your coldkey funds with.  The funds move from your coldkey (or wallet) to a spreadsheet in the blockchain that associates your coldkey with the validator's hotkey.  At no point does the validator have access to your funds.  When you want to unstake, the blockchain simply puts your staked funds back into your wallet and deletes the entry from the staking spreadsheet.

So in summary:
* Public keys are like your bank account number.
* Private keys are like your bank account password.
* A coldkey is a traditional crypto wallet.
* A hotkey is used by validators for staking and by miners for mining.
* A hot wallet is a wallet that has been connected to the internet.
* A cold wallet (or cold storage) is a wallet that has been generated offline by a device that will never touch the internet.
