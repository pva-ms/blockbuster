# BlockBuster

BlockBuster -> "Busting Solana blocks into little peices to index and operate on the programs therein" - Noone - 1995

This repositiory is the home for Metaplex Program Parsers. Program parsers are cannonical libraries that take a transaction or account update from a geyser plugin and parse them coprrecly according to Metaplex smart contracts. This sort of parsing is hard to automate as it must contain some knowledge of the api structure of the contract which is not fully describable yet via IDLS. Things like remainign accounts, optional accounts and complex instruction data are not always 100% clear what they mean without knowldege of the contract. 

## Mode of Operation
This library works best as a consumer of messages sent via a geyser plugin using the [Plerkle Serialization](https://github.com/metaplex-foundation/digital-asset-validator-plugin) library by metaplex. Its 
The types from that library are FlatBuffer based currently and are the wire format of messages coming out of Plerkle into the rest of the infrastructure.
For more information about Plerkle and the [Digital Asset RPC infrastructure](https://github.com/metaplex-foundation/digital-asset-validator-plugin) It can however be used in any general programs provided you can create the data in the FlatBuffer types.

## Scope

This library contains parsers for the following programs and the parsers are specific to how these contracts relate to metaplex assets.

* Gummyroll (Solana)
* Bubblegum (Metaplex)
* Spl Token (Solana)
* Token Metadata (Metaplex)
* Auction House (Metaplex)
* Candy Machine (Metaplex)
* Hydra (Metaplex)
