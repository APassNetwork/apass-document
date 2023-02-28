# ⚔ War Of Apter(WOA)

### ![](../.gitbook/assets/woa\_master.png)

### What is War of Apter(WOA) ?

War Of Apter is a fun and simple decentralized prediction game.

You bet $APT, Predict whether $APT price will UP or DOWN in next minutes. Guess correctly to win $APT!

* Predict if the price of APTUSD will be UP(Bull) or DOWN(Bear) than it was when the “LIVE” phase starts.
* If you enter an UP(Bull) position, and the “END PRICE” is higher than the “START PRICE” at the end of the 15 minute LIVE phase, you WIN! And if it’s lower, you lose.
* If you enter a DOWN(Bear) position, and the “END PRICE” is higher than the “START  PRICE” at the end of the 15 minute LIVE phase, you LOSE! If it’s lower, you win.

### What are you using for your price feed?

WOA uses Binance source for our price feeds for real-time price updates on the WOA oracle contract every 30 seconds.

The source URL: **** [**https://www.binance.com/en/trade/APT\_USDT?theme=dark\&type=spot**](https://www.binance.com/en/trade/APT\_USDT?theme=dark\&type=spot)****

### How is the payout calculated?

* Payout Ratio for UP Pool = Total Value of Both Pools ÷ Value of UP Pool
* Payout Ratio for DOWN Pool = Total Value of Both Pools ÷ Value of DOWN Pool

For example, if there’s 15 $APT in the DOWN side of a round, and the overall prize pool is 150 $APT, the DOWN payout ratio will be (150/15)=10x.

* Payout Amount = Payout Ratio × Position × (1 - Treasury Fee)

In the above case, if the round ends on a DOWN result, if you committed 2 $APT to a DOWN position, you’d get a payout of (2\*10) × (1-0.05) = 19 $APT. Your profit would be 17 $APT (19 - 2).

In testnet, the treasury fee is currently set at 1%: this may be subject to changes, which would be announced on AptosPassport official communication channels. **Treasury fees are used to buy back or burn $APT tokens.**

### Is there a time limit before I can collect my winnings?

No, you’ll be able to collect your winnings at any time in the future. Open the "Histroy" page and you will find the records.

