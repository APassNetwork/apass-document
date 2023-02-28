# 🌠 Quick Integration Guide

#### Welcome, developers! We offer fast integration options for you to choose.

[resolver-api.md](resolver-api.md "mention") fit for native environments.

[sdk-for-apass.md](sdk-for-apass.md "mention") fit for Wallets, DApp base on Javascript environments.



On your DApp, you can integration using SDK like this code

```javascript
// Using SDK sample
const { AptDomain } = require('aptpp-js');

var aptdomain=new AptDomain( {network:'testnet'} );

async function ReverseAddressName(input_address, cb) {
    if( input_address.startsWith('0x') ){

        let { domain } = await aptdomain.reverse( input_address);
        if( domain ) {
            //got a domain bind on this address
            cb(input_address,domain);
        }
    }
}

const input_address = '0x879b4e92b720ead64a8218e9b4cced26825e88e9923ef8b5eb4d610967433c45';

ReverseAddressName(input_address,function(address,domain){
    
    // Now, you can update address to domain on your DApp or Wallet
    console.log(address,domain);

});


```
