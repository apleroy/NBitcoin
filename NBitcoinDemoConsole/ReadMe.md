# # A Bitcoin 101 Console App Demo Using C#, .NET, and NBitcoin on the RegTest Network

This article is a 101 level walkthrough of getting started programming on top of the Bitcoin network with Windows, .NET, C#, and the  [NBitcoin](https://github.com/MetacoSA/NBitcoin)  library.

There is  **_a lot_** to learn when starting on Bitcoin. I work most with C#/.NET/Windows and whenever possible like “seeing” things on the screen and clicking around with a GUI, an interactive console, and Postman. In that spirit, we’ll walk through some programming examples using only these platforms to reduce the number of learning variables.

In the article below, we’ll setup a local development to use Bitcoin Core on Windows, add in environment variables to be able to use the RegTest network, build a local Console program that can connect to a bitcoin node, create wallets and addresses, send and receive transactions, and analyze the local network. All while being able to see the programmatic results in the  [Bitcoin UI locally](https://bitcoin.org/en/bitcoin-core/features/user-interface)  and all leveraging the NBitcoin library.


## Acknowledgements and Prerequisite Reading  

Before going further, I want to highlight that all of the work in this tutorial is built on top of the  [NBitcoin library](https://github.com/MetacoSA/NBitcoin), book, and examples by  [Nicolas Dorier](https://twitter.com/NicolasDorier)  and  [@nopara73](https://twitter.com/nopara73). It is incredible to have a full C# and .NET library for Bitcoin Core with all of the  [examples](https://github.com/ProgrammingBlockchain/ProgrammingBlockchainCodeExamples)  they have provided. Everything below is me “learning by doing and writing about it” as  [gleaned from these resources](https://programmingblockchain.gitbook.io/programmingblockchain/):

[](https://github.com/MetacoSA/NBitcoin)

Comprehensive Bitcoin library for the .NET framework. - GitHub - MetacoSA/NBitcoin: Comprehensive Bitcoin library for the .NET framework.

![](https://opengraph.githubassets.com/506ec3e2faa12d0b49df7338f307a4d4531431534c36f6ae92c35cff3f9290e1/MetacoSA/NBitcoin)

This sample app would also not be possible without the incredible book and resources provided by  [Andreas Antonopoulos](https://aantonop.com/). This book is one of the best resources I have come across that goes step by step into all details of bitcoin and its blockchain.

[](https://github.com/bitcoinbook/bitcoinbook)

Before starting with this tutorial, I would highly recommend heading over to these resources if you haven't already.

## Article & Details

The full article to build this Console program is here:

## Configuration File

### RegTest

```
regtest=1
server=1
rpcallowip=127.0.0.1
rpcuser=YourRpcUsername
rpcpassword=YourRpcPassword
fallbackfee=0.0002

[test]
rpcbind=127.0.0.1
rpcport=18332

[regtest]
rpcport=18332

```

### TestNet

```
testnet=1
server=1
rpcallowip=127.0.0.1
rpcuser=YourRpcUsername
rpcpassword=YourRpcPassword
fallbackfee=0.0002

[test]
rpcbind=127.0.0.1
rpcport=18332

[regtest]
rpcport=18332
```
