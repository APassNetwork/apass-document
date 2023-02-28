# 🔵 How to Integration APassOracle

### Contract

* Address: 0xffd89fe22fd620d2cba0b3aaccdde6f5ad63ce7a7b18d13c0dc61e21521affff
* Source Code: [https://github.com/AptosPassport/aoracle-contract](https://github.com/AptosPassport/aoracle-contract)

### Access off-chain

You can easily access AOracle real-time data through API.

Visit AOracle Board at [http://aptpp.com/#/aoracle](http://aptpp.com/#/aoracle/index) , choose your pair and you will get API Url like:

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The maximum delay between on-chain data and API data is 5 seconds
{% endhint %}

### Access on-chain

You should add a dependency in your project move.toml

```toml
[package]
name = "YourProject"
version = "0.0.1"
upgrade_policy = "compatible"

[dependencies]
AptosFramework = { local = "../../aptos-core-main/aptos-move/framework/aptos-framework" }
AptosStdlib = { local = "../../aptos-core-main/aptos-move/framework/aptos-stdlib" }
AptosToken = { local = "../../aptos-core-main/aptos-move/framework/aptos-token" }

// Add this line
AOracle = { git = "https://github.com/AptosPassport/aoracle-contract.git", rev = "main" }

```

Then add the module reference in the move code, and use AOracle like follow:

```rust
module YourProject::SomeModule {
  use std::error;
  use std::vector;
  use std::signer;
	
  // Use AOracle moudule
  use AOracle::oracle;
	
  /**
  * @notice Get latest recorded price from oracle
  */
  fun getPriceFromOracle(): (u64, u64) {	
    let (roundId, price, _, timestamp, _) = 
        oracle::latestRoundDataByName(string::utf8("APTUSDT"));
    (roundId, price)
  }
}
```

