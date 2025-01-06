* difference between hotkey and coldkey
  * coldkey=main wallet, not to be confused with cold storage
  * hotkey=used to facilitate stuff like mining and staking
    * you receive mining rewards to your hotkey and then move the money to your coldkey and from there you can sell it on an exchange.
    * you receive staking rewards to your hotkey, then when you unstake the funds end up in your coldkey and again you can then sell it on an exchange.
  * hotkeys are associated with a coldkey, a coldkey can have many hotkeys
  * when you write down your nmemonic, your secret 12 words that unlock your wallet- those 12 words are your coldkey
  * your wallet app is a coldkey, there are no hotkeys in your wallet app.
  * Staking associates your CK with the vali's HK via a blockchain db.  You retain 100% control over your funds, validators don't control the funds you've delegated to them.

* how is a wallet related to coldkeys/hotkeys
  * a wallet app will show your coldkey balance plus the hotkey balances that are associated with your wallet's coldkey.
