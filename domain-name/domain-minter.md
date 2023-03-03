# ⛏ Domain Minter

Each domain name can mint $APC oncetime for every 24 hours. The amount of rewards is determined by one's own generation, and the top-level parent domain name length.

| ZERO Length | ZERO     | FIRST                                     | SECOND                                  |
| ----------- | -------- | ----------------------------------------- | --------------------------------------- |
| 3 char      | 1.0 $APC | <p>0.4 $APC </p><p>0.1 $APC(feedback)</p> | <p>0.2 $APC<br>0.05 $APC(feedback)</p>  |
| 4 char      | 0.8 $APC | <p>0.32 $APC<br>0.08 $APC(feedback)</p>   | <p>0.16 $APC<br>0.04 $APC(feedback)</p> |
| 5 char      | 0.6 $APC | <p>0.24 $APC<br>0.06 $APC(feedback)</p>   | <p>0.12 $APC<br>0.03 $APC(feedback)</p> |
| 6+ char     | 0.4 $APC | <p>0.16 $APC<br>0.04 $APC(feedback)</p>   | <p>0.08 $APC<br>0.02 $APC(feedback)</p> |



> **The mathematical formula**\
> MINT\_ONE\_DAY = ( 0.2 \* ( 8 - MIN( 6, DOMAIN\_LENGTH ) ) ) / POW( 2, GEN )

If it is not a ZERO domain name (subdomain or grandchild domain), 20% of these rewards will be fed back to the father.

To participate in "Domains Minter", you need to

> 1. Have a Passport domain name on the mainnet.
> 2. Enter the NFT CARD tab of the My Domains interface, collecting your $APC once a day.
> 3. It is worth mentioning that you can increase the number of purchased subdomains by upgrading your domain name. Subdomains also have minting rights, and each subdomain will return a portion of $APC to the main domain after each collecting. Note: The number of collectable $APC per day is not cumulative, collecting daily would be ideal.
