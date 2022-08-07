# p2p

 ### p2p trading using 2 of 3 bitcoin multisig
 
![5cb779319e173360240cf25c_image-blogpost-p2p-directory@2x](https://user-images.githubusercontent.com/94559964/183299645-f7d16297-b851-437c-a069-eee898d9e4d9.jpg)



 1. Enter public keys for Alice and Bob
 2. It will create a 2 of 3 multisig address with the public keys (Alice, Bob and Carol)
 3. Alice will send BTC to multisig address because she is the seller in this trade.
 4. Bob will enter the withdrwal address to receive bitcoin.
 5. Bob will send money to Alice's bank account. Alice will confirm it and sign the transaction.
 6. Bob will sign the transaction.
 7. Carol will finalize the signed transaction and broadcast it.

 :information_source: 10% fee for the trade goes to Carol in release transaction, 0.00010000 BTC in the below transaction. Rest amount is sent to Bob.

 An example trade using the python script (signet):

 ```
Enter public key for alice: 02c821b4b60fa909f0242b600c5f1eae7a4e8129198acb19658c8f8821d6e97446
Enter public key for bob: 0295761376e042cff7c2a064de4ea3cc8031c4633c96c73804735aa7be0e9dd800

Alice should send BTC to 2NAVgKcyzUYzVjEiJqEH5DizbiFa4ntqyDm for trade. This is a 2of3 multisig address.

Descriptor for multisig: sh(multi(2,02c821b4b60fa909f0242b600c5f1eae7a4e8129198acb19658c8f8821d6e97446,0295761376e042cff7c2a064de4ea3cc8031c4633c96c73804735aa7be0e9dd800,02d75d7d44daba64fdb1d164276725618402701a0ff0d3e2039deb574f20c71591))#fyqaumdk

100000 sats received in aad75b57f90b54c35d4d8ba4593862d1b17eace5774785c014b13c8f9650730f:1

Bob should send money to Alice's bank account for completing this trade.

Enter the withdrawal address for bob:tb1qe7tkgkfuz7dvapcs9f97lkhp6w8drxjwaw78pj

Transaction in PSBT format to release funds from 2of3 multisig (10 percent fee paid to carol and rest goes to bob):
cHNidP8BAHECAAAAAQ9zUJaPPLEUwIVHd+WsfrHRYjhZpItNXcNUC/lXW9eqAQAAAAD/////AqhbAQAAAAAAFgAUz5dkWTwXms6HECpL79rh047Rmk4QJwAAAAAAABYAFJYdY/0HicoU32origIXwmfhYqVqAAAAAAAAAAA=

Enter signed transaction:cHNidP8BAHECAAAAAQ9zUJaPPLEUwIVHd+WsfrHRYjhZpItNXcNUC/lXW9eqAQAAAAD/////AqhbAQAAAAAAFgAUz5dkWTwXms6HECpL79rh047Rmk4QJwAAAAAAABYAFJYdY/0HicoU32origIXwmfhYqVqAAAAAAABAHICAAAAAeFmSah4mE++AeetFPCkzd2+1TT/rV/+c/PDSTxSZf+BAAAAAAD+////AvEH61NRBgAAFgAUnUXrMBNFz82N5rENzq1P4d3IkgCghgEAAAAAABepFL018Z06Zln+p1ypJU9wYSveqhq7hx6QAQABB/wARzBEAiANGIKAzLA+zDWu6VmhQgu5WxPwps4nZyByXX4oYEchOAIgT+eN5RB1iERmg9tnoFuUq2aby/Bnbv7yElnzNsx+aUcBRzBEAiBdnNvx86ysuUDZZOqTAzplo8iynxwLja5cE8X6kw10yQIgTNq2TBIwPjrJgNwqi9fkXpHz5yXoIFLPVU5IZb5GeTsBTGlSIQLIIbS2D6kJ8CQrYAxfHq56ToEpGYrLGWWMj4gh1ul0RiEClXYTduBCz/fCoGTeTqPMgDHEYzyWxzgEc1qnvg6d2AAhAtddfUTaumT9sdFkJ2clYYQCcBoP8NPiA53rV08gxxWRU64AIgIDxjoKE84p6KKpUWZR6z9jSlpXimLG4pYAtYQ/UQub8YMQilV92gAAAIAAAACAAwAAgAAA

89000 sats sent to Bob in 537c8381b2ff9428f2bcc02b897cdc8fe4da2c1aeca4491c02a41431d0f183f6
```

---

Funding transaction: [`aad75b57f90b54c35d4d8ba4593862d1b17eace5774785c014b13c8f9650730f`](https://mempool.space/signet/tx/aad75b57f90b54c35d4d8ba4593862d1b17eace5774785c014b13c8f9650730f)  

Release transaction: [`537c8381b2ff9428f2bcc02b897cdc8fe4da2c1aeca4491c02a41431d0f183f6`](https://mempool.space/signet/tx/537c8381b2ff9428f2bcc02b897cdc8fe4da2c1aeca4491c02a41431d0f183f6)

---


