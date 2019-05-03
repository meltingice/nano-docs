#### account
Refers to an address (starts with `xrb_` or `nano_` which are interchangeable) that you control the private keys of. An address is a reinterpretation of the 256-bit public key using BASE32 encoding and a checksum.

#### active transaction
A newly downloaded block to the node which enters into the voting process.

#### ad hoc accounts
Accounts not derived from a private seed which can be held in the node wallet through the wallet ID. These accounts are only recommended for use with advanced systems.

#### announcement rounds
A repeating 16 second cycle on the node during which votes are collected for active transactions in attempt to reach quorum.

#### block

#### Block Lattice
The Block Lattice is a data-structure in which individual accounts control their own blockchain. This allows transactions to be added quickly without conflict and sent to the network for confirmation.

#### bootstrap network
A sub-network established between peers via Transmission Control Protocol (TCP) for managing bulk transmission of blocks. This is used on initial bootstrapping of peers and when out-of-sync peers attempt to fill large gaps in their ledgers. This is available within all Nano networks (main, beta and test networks).

#### bootstrapping
During initial sync, the nano\_node requests old transactions to independently verify and populate its local ledger database. Bootstrapping will also occur when the nano\_node becomes out of sync with the network.

#### circulating supply
133,248,290.903662 NANO

#### election

#### genesis

#### inbound send
A block with funds being transferred to an [account](#account) owned by a [wallet](#wallet) on your node

#### live network
A sub-network established between peers via User Datagram Protocol (UDP) for communicating newly published blocks, votes and other non-bootstrap related traffic. This is available within all Nano networks (main, beta and test networks).

#### peers
Nodes connected over the public internet to share Nano network data.

#### pending
A transaction state where a block sending funds was published and confirmed by the network, but a matching block receiving those funds has not yet been confirmed.

#### Proof-of-Work (PoW)
A Proof-of-Work is a piece of data which satisfies certain requirements and is difficult (costly, time-consuming) to produce, but easy for others to verify. In some systems this data is a central part of the security model used to protect against double-spends and other types of attacks, but with Nano it is only used to increase economic costs of spamming the network.

#### quorum
When the delta between the two successive blocks of a root is > 50% of the online voting weight

#### rebroadcasting representative
A Nano account with >= 0.1% (133,248.290903662 NANO) voting weight delegated to it. When configured on a node which is online, it will rebroadcast votes for each block to it's peers to help the network reach consensus.

#### representative
A Nano account with > 0 voting weight delegated to it. Unlike [rebroadcasting representatives](#rebroadcasting-representative), when configured on a node which is online it will not send out votes and thus won't participate in network-wide consensus.

#### root
The [account](#account) if the block is the first block on the account, otherwise it is the previous hash included in the block.

#### seed
A 256-bit random value usually represented to the user as a 64 character hexidecimal (0-9 and A-F) value. Private keys are derived from a seed.

#### unchecked (blocks)

#### unopened account
An account address that does not have a first block on it (which must be a block to receive Nano sent from another account, cannot be a block only changing the representative).

#### unpocketed
See [pending](#pending) 

#### voting
Each node configured with a [representative](#representative) votes on every block by appending their representative signature and a sequence number to the hash. These will be sent out to peers by [rebroadcasting representatives](#rebroadcasting-representative) only.

#### voting weight
The amount of weight delegated to a [representative](#representative).

#### wallet
A wallet is an organizational object in a nano\_node that holds a single seed from which multiple accounts are deterministically derived via a `uint32` index starting at 0. Private keys are derived from the seed and index as follows:

$$
k_{private} = blake2b(seed || index)
$$

#### WALLET_ID
A 256-bit random value name/identifier for a specific wallet in the local nano\_node database. The WALLET\_ID **is not** stored anywhere in the network and is only used in the local nano\_node. Even though a WALLET\_ID looks identical to a seed, do not confuse the WALLET\_ID with a seed; funds cannot be restored with a WALLET\_ID. Do not backup the WALLET\_ID as a means to backup funds.

#### work peers
Node peers which are configured to generate work for transactions at the originating nodes request.