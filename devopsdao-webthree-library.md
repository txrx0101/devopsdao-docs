Devopsdao is a community driven project to build an ecosystem of blockchain software development, as a part 
of our community contribution effort we have took the development of webthree library (a fork of web3dart) 
in order to keep Dart language ecosystem consistent with the recent updates of Ethereum network.

# WebThree

WebThree — a web3 library for dart that allows you to interact with a local or remote ethereum node using HTTP or WebSocket. Suports custom credentials providers like WalletConnect and Metamask.

Fork of original web3dart 2.3.5 by simolus3, incorporating all changes from other forks.

# Features

Connect to an Ethereum node with the rpc-api, call common methods
Send signed Ethereum transactions
Generate private keys, setup new Ethereum addresses
Call functions on smart contracts and listen for contract events
Code generation based on smart contract ABI for easier interaction

# 2.5.0 first WebThree version

Renaming library to WebThree in order to maintain a community developed fork.
Bumping version number to 2.5.0, pull requests are greatly appreciated. No breaking changes were made.

the reason for creating this fork from https://github.com/simulous/web3dart 2.3.5 was that web3dart 2.4.1 currently published at https://pub.dev/packages/web3dart/ Github repo https://github.com/xclud/web3dart has factored out contract generator and metamask integration, making a breaking change. The following changes were implemented:

1. added stubs for dart_wrappers.dart and dart:js, added conditional dependencies import to metamask example in order to support web and other platform builds from a single codebase.

2. fix signPersonalMessage to use modern personal_sign instead of eth_sign

3. fix type issues in getTransactionHistory

4. Merged all reasonamble commits from the forks network, 
thank you @@simolus3 @superkeka @alexeyinkin @xclud @TheGreatAxios @rgplvr @thegamenicorus @MahmoudKhalid @superkeka from @superkeka/web3dart

5. Make EthereumAddress Comparable

6. StateMutability error when parsing json abi that contains an event simolus3/web3dart#13

7. Make getTransactionByHash nullable

8. Expose number utility functions simolus3/web3dart#3

9. decodeCall Uses the known types of the function parameters to parse them from the binary call data. The reverse of [encodeCall].

10. make rpc call public

11. Add block number to BlockInformation, add BlockInformationWithTransactions, add getBlockByNumberWithTransactions.

12. API Documentation on how to create the wallet files, HD wallets simolus3/web3dart#2

13. Fix fetching mempool transactions that do not yet have blockHash

14. Erc20 class support for name, symbol and decimals functions. from @GangemiLorenzo/web3dart

15. add sender to generated contract read

16. add argSender to generated contracts from @kryptogo/web3dart

17. add toMap for tx receipt

18. add value for eth_call from @thegamenicorus/web3dart

19. fix filter not found

20. add getTransactionHistory

21. keep rpc running

22. add getPendingTransactions from @thelazyindian/web3dart

23. Accept Null message Fix EIP1559Information from @MahmoudKhalid/web3dart

24. Fix EIP1559Information

25. Added getGasInEIP1559 method

26. Added feeHistory method from @rgplvr/web3dart fix fetchChainIdFromNetworkId from @naiba/web3dart

27. fix uint8list overflow

# Recent Changes

## 2.5.4

* added js_util_stub.dart to support javascript object conversion for metamask
* fixed getFeeHistory
* fixed getBlockInformation
* changed from solc to solcjs

## 2.5.3

* fixed getGasInEIP1559
* fixed sender type in contract generator

## 2.5.2

* return build.yaml for contract generator

## 2.5.1

* update pubspec