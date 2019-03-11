# BN - BitcoinName
Bitcoin alias protocol

## Links

BN Transactions:<br> https://babel.bitdb.network/query/1DHDifPvtPgKFPZMRSxmVHhiPvFmxZwbfh/ewogICJ2IjogMywKICAicSI6IHsKICAgICJmaW5kIjogewogICAgICAib3V0LnMxIjogIjE5aUczV1RZU3NieW9zM3VKNzMzeUs0ekVpb2kxRmVzTlUiCiAgICB9LAogICAgImxpbWl0IjogMTAKICB9LAogICJyIjogewogICAgImYiOiAiWy5bXSB8IHsgdHJhbnNhY3Rpb246IC50eC5oLCBibG9jazogLmJsaywgc2VuZGVyOiAuaW5bMF0uZS5hLCBwdXNoZGF0YTogeyBiMDogXCJPUF9SRVRVUk5cIiwgczE6IC5vdXRbMF0uczEsIHMyOiAub3V0WzBdLnMyLCBzMzogLm91dFswXS5zMyB9IH1dIgogIH0KfQ==

BN State Machine:<br>
https://bn.onchain.ch/query/1G3BpTyEK6xF4LaQTHqdFBBaVxYHZzts4M

## Benefit
**BN://** insteed of **B://** Links could be included in websites. Using bn: // links instead of b: // links has the advantage of being able to dynamically include content.

Example B:// (**can not be changed** once set):<br>
``<img src="B://<TxID(1)>"``

Example BN:// (Pointer **can be changed**, because the state of the entry can be overwritten.):<br>  
``<img src="BN://<BitcoinAddress>/<alias>"``

## BN:// Protokoll
The BN: // protocol should point to the TxID e.g. of a B: // file and thus forms another layer which state can be overwritten.

=> Im not sure if it makes sense to add a type field !?
=> possible types could be: txid-pointer, folder-pointer, ?

| TxID        | Sender | Pushdata      | ??Pushdata  |Pushdata |Pushdata  |
| ----------- |:---------------:|:---------------:|:-----------:|:--------:|:----------:|
| TxID      | BitcoinAddress| BN:// BitcomAddress | ??< type > <br>(B://)    | < **alias** > (picture.jpg)  | < **pointer** > (TxID) |



#### Overwrite BN:// State
New transactions with the same alias from a sender automatically override the old state. Protocol API always outputs only the most current state.
The alias sender combination prevents an unauthorized one from changing state.

#### ...
*  An API that resolves BN: // links to txids or an API that returns even the file data can be built.
*  maybe add a type field to simulate something like directories.
*  state reset/delete actions


@SH
