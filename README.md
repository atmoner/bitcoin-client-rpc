![bitcoinclientrpc](https://i.imgur.com/fJoGTUb.png)
 
 
# Bitcoin-client-rpc 

*   [What is it?](#what-is-it "What is it?")
*   [Installation](#installation "Installation")
*   [Usage](#usage "Usage")


## What is it? 
It is a library that allows you to interact with the json-rpc part of a bitcoin client (regardless of the coin)
A simple initialization with the client's rpc identifier and you will be able to recover all the information from bitcoin-cli

## Installation 

`npm i bitcoin-client-rpc`

## Usage  

    const bitcoinRpc = require('bitcoin-client-rpc');
    const bitCoin = new bitcoinRpc('localhost', '9888', 'rpcUsername', 'rpcPass');
    
    bitCoin.call('getinfo', [], function (err, resB) {
    	if (err !== null) {
    		console.log('Bitcoin RPC error: ' + err )
    	} else {
    		console.log(resB.result)		
    	}
    })

