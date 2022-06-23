# Notes

- hash functions map text data to integer numbers / key  --> hash function  --> hash
- sometimes diff inputs get the same output = colission
- example: 1 Alice calls coin and makes commitment 2 Bob flips coin and reveals result 3 Alice reveals what she committed
- situation: block has 10 transactions = 10 hashes. Those hashes are being combined in a merkle tree until you have 1 hash (Root hash)
- any little change would result in other root hash so the block would then be invalid
- Root hash + previous block header hash + nonce ---> cryptographic hash function ---> difficulty target
- miners are adjusting the nonce until they find the right one
- UTXOs define where each blockchain transaction starts and finishes
- the Byzantine generals problem is a game theory problem that describes how difficult it is for parties to reach a consensus without the help of a central party
- 




