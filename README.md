# OG XEN
## A gift to XEN minters from crank 1 to 3,200,000!  

**What is OG XEN?**  
OG XEN (OGX) is an immutable erc20 token contract that has also a built in merkle airdrop.  

**What is the OGX contract address?**  
[0x994e4534F2eE11Fb0ECceA68bDfe83D7d7e15034](https://etherscan.io/address/0x994e4534f2ee11fb0eccea68bdfe83d7d7e15034)  

**Who can claim OGX?**  
All owners of XEN crank between 1 and 3,200,000.  

**I own crank N, how much OGX will I get?**  
You will get the equivalent term days. If your term is 1 day, you get 1 OGX, if your term is 400 days, you get 400 OGX.  

**Is there a premine or a developer allocation?**  
No. 100% of the tokens minted will come from the 3,200,000 crank data. This token is 100% community owned.  

**How do I claim OGX?**  
The contract has a [claim(uint32 rank, address to, uint15 term, bytes32[] proof)](https://github.com/ph4n70mr1ddl3r/ogx/blob/main/contract/ogx.sol) function. Any account can call this function and pay gas, but the contract will verify that the data is part of the merkle tree and once verified, it will issue OGX tokens equivalent to the term set in the 3rd argument and send it to the address set in the 2nd argument. Inside the folder named [proofs](https://github.com/ph4n70mr1ddl3r/ogx/tree/main/proofs), there are 320 text files in the format proofsXXX.txt that contains 3,200,000 lines for each crank. There are 4 data in each line (rank, address, term, proof) that is needed to be passed to the claim function. This is [proof000.txt](https://raw.githubusercontent.com/ph4n70mr1ddl3r/ogx/main/proofs/proofs000.txt), disable line wrap in your browser and you will see 1 crank each line. Each proof file is ordered by crank with 10,000 cranks each. All merkle proofs for all 3,200,000 cranks have been precalculated to make it easier for everyone. If you are a developer familiar with merkle trees, you can also calculate your own proof.  

**How do I know that there are no backdoors or secret minting procedures?**  
Anyone can build their own merkle tree and calculate the merkle root and compare it to what is specified in the contract. The file [roots.js](https://github.com/ph4n70mr1ddl3r/ogx/blob/main/script) in the [script](https://github.com/ph4n70mr1ddl3r/ogx/tree/main/script) folder is what was used together with the raw data in [crank.zip](https://github.com/ph4n70mr1ddl3r/ogx/tree/main/raw) inside the [raw](https://github.com/ph4n70mr1ddl3r/ogx/tree/main/raw) folder.  

**Until when can we claim our OGX tokens?**  
The claim function will stop working once block height reaches [20,000,000](https://etherscan.io/block/countdown/20000000). Also token transfers will be enabled only after reaching block height [18,250,000](https://etherscan.io/block/countdown/18250000) to make sure nobody gets an unfair advantage.  

**Can we burn OGX tokens?**  
Yes, the contract implements [ERC20Burnable](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/ERC20Burnable.sol). Anyone with OGX tokens can burn their tokens.  

**What's next?**  
[Follow me](https://twitter.com/ph4n70mr1ddl3r) and I will announce if there are community built projects built using OGX. Also, check the [OGX Forum](https://github.com/ph4n70mr1ddl3r/ogx/discussions) every now and then if there are discussions. You can also post there if you have questions or you need help.
