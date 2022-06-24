# Notes (made during studying)

- hash functions map text data to integer numbers / key  --> hash function  --> hash
- sometimes diff inputs get the same output = colission
- example: 1 Alice calls coin and makes commitment 2 Bob flips coin and reveals result 3 Alice reveals what she committed
- situation: block has 10 transactions = 10 hashes. Those hashes are being combined in a merkle tree until you have 1 hash (Root hash)
- any little change would result in other root hash so the block would then be invalid
- Root hash + previous block header hash + nonce ---> cryptographic hash function ---> difficulty target
- miners are adjusting the nonce until they find the right one
- UTXOs define where each blockchain transaction starts and finishes
- the Byzantine generals problem is a problem that describes how difficult it is for parties to reach a consensus without the help of a central party
- solution: protocol which adoptes a procedure among the parties to make choices (e.g. PoW, PoS, etc.)
- PoS is type of consensus mechanism used by blockchains to achieve distributed consensus
- in PoS ETH staked by validators act as collateral which can be taken if bad behaviour from validator
- in PoS time is divided into slots (12 seconds) and epochs (32 slots)
- final block: Block can never be changed again
- staking replaces mining as the consensus mechanism in PoS
- beacon chain manages the registry of validators
- slashing: punishment for stakers (if bad behaviour)
- sharding: database partitioning where large databases are divided into smaller clusters to reduce data burden and improve scalability
- randomnes: data produced in an unpredictable way
- ethereum client: software which contains the EVM program and memory pool, client process 
- memory pool: location of signed transactions ready to get included in a block gets stored
- client process: sends transactions from the mempool to the EVM
- critical functions of EVM is to store the “state” of all accounts and what information those accounts store
- EVM stores state according to a data structure called a “Merkle Patricia trie”, which is able to contain all the key:value pairs of all addresses on ethereum
- value/state for each address is itself an encoding of the hash of the address’s respective code, a hash of the data stored by the account, its balance, and the number of transactions it’s carried out // represented as a nonce
- bytecode is the low-level language that the EVM reads to compute state transitions
- Already experienced with Solidity so skipped that part
- synthetics (e.g. DAI) are collateralized, decentralized stablecoins
- custodial stablecoins (e.g. USDT, USDC) are centralized, collateralized stablecoins
- synthetics carry the danger of oracle dependency, which = risk
- if DAI drops under 1 dollar (e.g. $0.99) then stability fee rises (to $1.01) (this goes both ways)
- blockchain cannot access data outside of its state (e.g. ETHUSD price, the
weather today, content at a URL, etc.)
- sandwich attack is a form of front-running that targets protocols by placing one order right before the trade and one right after it
- 





