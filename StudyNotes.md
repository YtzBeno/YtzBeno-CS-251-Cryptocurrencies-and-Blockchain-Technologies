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
- x * y = k !!!
-  e.g. there's a pool with 20,000 USDC and 10 ETH. K would be 200,000. If you wanted to sell 1 ETH, ETH in the pool increases to 11. For the equality to hold, USDC must decrease to 20,000 / 11 = 18,181.82 / You receive 20,000 - 18,181.82 = 1,818.18 USDC for 1 ETH
- SP = x / y (SP = spot price)
- example above: new SP = 18,181.82 / 11 = 1,652.89
- no privacy/anonymity Bitcoin & Ethereum, everyhting can be found on the chain (e.g. wallets, values, transactions, etc.)
- mixing creates the possibility that many people could've sent the transaction, therefor the more people the higher anonymity
- Monero uses ring signatures, to anyone observing, it’s impossible to tell whose key was used to sign, making the transaction anonymous
- ZKPs and commitments could allow private transactions on a public blockchain 
- there's a big demand from all kind of parties for private transactions 
- ZKPs allow a third party provider to also output a proof of computational integrity which guarantees the output you received is correct
- ZKPs allow you to selectively hide some or all inputs around a computational statement
- verifiable computation with ZKPs allow L1s to outsource transaction processing to off-chain high-performance systems (aka Layer 2s). This enables blockchain scaling without compromising on security. As an example, StarkWare is building a scalable smart contract platform, StarkNet, using a special-purpose virtual machine that runs ZK-friendly code. Aztec also enables their Layer 2 programs to run privately, without leaking any information about a user’s transactions
- L1 chain like Zcash allows transactors to hide senders, receivers, or amounts using ZKPs, as an opt-in (Zcash)
- problem: ZKPs are slow! (due to complex operations and non ZKP friendly software)
-  proof systems (e.g. Plonk) take a computation that’s expressed in a ZK-friendly format along with some inputs and output a proof
-  ZKPs will require hardware acceleration
-  soundness: If a statement is false, no dishonest prover can unilaterally convince an honest verifier that they possess knowledge about the correct input
-  with ZKPs a prover can validate every single transaction, bundle them all together and generate a proof of this computation
-  when all nodes are synchronized, they only need to verify that the proof is valid, and there is no need to recalculate all transactions
-  ultimate goal of zkEVM is actually to apply it to L1, replacing our current EVM
-  
-  





