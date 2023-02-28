# 📎 Resolver API

### Domain to Address

```javascript
// Replace "test@apt" with your APT domain name.
const name = "test@apt";

// The supported networks are "mainnet","testnet","devnet".
const network = "testnet";

const response = await fetch(`https://aptpp.com/api/v1/${network}/address/${name}`);
const { address } = await response.json();
```

### Address to (Primary)Domain

```javascript
// Replace "address" with the address you want to lookup.
const address = "0x1234...abcdef";

// The supported networks are "mainnet","testnet","devnet".
const network = "testnet";

const response = await fetch(`https://aptpp.com/api/v1/${network}/name/${address}`);
const { name } = await response.json();
```

### Get all domain name records

```javascript
// Replace "test@apt" with your APT domain name.
const name = "test@apt";

// The supported networks are "mainnet","testnet","devnet".
const network = "testnet";

const response = await fetch(`https://aptpp.com/api/v1/${network}/record/${name}`);
const result = await response.json();
```

\
Result Samples:

```json
{
  "status": 200,
  "records": {
    "data": {
      "data": [
        {
          "key": "1",
          "value": "0x0000...0000",
          "name": "APT",
          "type": "string",
          "group": "address"
        }
      ]
    },
    "domain": "test",
    "expiration": "1695972146",
    "regtime": "1664436146",
    "tokenid": {
      "property_version": "0",
      "token_data_id": {
        "collection": "Aptos Passport",
        "creator": "0x0000...0000",
        "name": "test@apt"
      }
    },
    "metadata": {
      "default_properties": {
        "map": {
          "data": [
            {
              "key": "creator",
              "value": {
                "type": "vector<u8>",
                "value": "0x0000...0000"
              }
            }
          ]
        }
      },
      "description": "Aptos Passport Desc",
      "largest_property_version": "0",
      "maximum": "1",
      "mutability_config": {
        "description": false,
        "maximum": false,
        "properties": true,
        "royalty": false,
        "uri": false
      },
      "name": "test@apt",
      "royalty": {
        "payee_address": "0x0000...0000",
        "royalty_points_denominator": "0",
        "royalty_points_numerator": "0"
      },
      "supply": "1",
      "uri": "https://aptpp.com/nftpic/test@apt"
    },
    "addr": "0x0000...0000"
  }
```
