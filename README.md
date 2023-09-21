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

**Notes**  
I'll execute the claim for crank 1 to demonstrate and update this readme for details.

**Update**  
Crank 1 claimed. I executed it and paid for gas.
In line 1 of proof000.txt is the data for crank 1.

crank: 1  
address: 0xcc3f4a70965a85c4c65fd54ffb1527e618335212  
term: 20  
proof: 
 ["0x74854f1dea34ec8d0f4ba91782a32fa7cc915a6a6937b98a092e0ac4d4abe9d7","0xb5dfa60b9b938ec0333ede31a3f75064c479ff487919bb19699c8e66fa8d94d3","0x1f7b1c46b4f03bc876993109ff58935f75afc32ea96177dfa5425e64ee8569c8","0x292badb35bfc9dc2df01bc60c90fa2b93d7a4227369eabcfd3321fab8856333b","0xac1b529c75aaf3590f0f3c5b37d2db78d150d0adfb9c9de400e4c5431f1c44ab","0x0558cafcbea68b9cdde133590be9e8369270a0068dc72dd94bfe83b806b0a3cb","0x6cd26e4a8facd00687ae31eae01713a0921f018abdc402dbe89542bb5abf05b5","0x787dd7a2afe2577ab66353f99bdb4bd202bdbb3962dca22981a7b126b6bcca79","0x5b6945161589a0244799f5a62dd3a0fa4372c912d9fec900391a6cbe5fa3ce0e","0x5a5bfabf85c3e69fb4ff8d0703614b077394f9a3405e67742d37404e29e9e848","0x0a4d058db120123786d2fa670f54447ae5216d31637ad11a260799a766e40897","0xaa3553f76e242ea114d924b31e987cbb9bc421a855f345ee59c4cb2568e02277","0x5bcc649cffcffc6107d0662337d25ddaabf61cf338ddd5e233ed7cb493aaf2c1","0x4a5636fbc86a45cb95732350b0e6156157b4af8150ced8559aa82ec077a56f6f","0x444260b65364de24baffc13e2ea28f4ac70fad7b28e1468c94a3a86e55800428","0x3d8db4010af468d8ba8e2bb97d104c887bcc86dbcef774a1426946a392a8a1de","0x0e6e19e9361e7d0d1eabf2c13016fcbf7fce7583023e03d394150f765fd15524","0x8d19ec3ff54da167d6cef73decca85b0acef96b6d902d96c1287b833ce666f6e","0x481f814b9e3257b658be69288a0c0ffc7b1fbe04dc0499470a5555323fc27fce","0x6aa8d29f7477dc1723dcd7543fe7044b34199f195051eac5753cc18bfda43044","0xb2f2e2fa3aa6608a5dbe94389f11567ce7b8b11ac139756269e122502ce8ad53","0xa47fc50fd83d67a8f125b367d3ae14aac5d6ee676a97a7fe6003e7c4b9a2a688"]  

Transaction:  
[https://etherscan.io/tx/0xb6aff4564a1b87fdb9a5c75de59da9ebc53c53e2ef967753dff72d85008df84f](https://etherscan.io/tx/0xb6aff4564a1b87fdb9a5c75de59da9ebc53c53e2ef967753dff72d85008df84f)  
Cost to claim: 0.00088483 ETH   
If using etherscan to claim, remove the quotation marks in the proof:  
[0x74854f1dea34ec8d0f4ba91782a32fa7cc915a6a6937b98a092e0ac4d4abe9d7,0xb5dfa60b9b938ec0333ede31a3f75064c479ff487919bb19699c8e66fa8d94d3,0x1f7b1c46b4f03bc876993109ff58935f75afc32ea96177dfa5425e64ee8569c8,0x292badb35bfc9dc2df01bc60c90fa2b93d7a4227369eabcfd3321fab8856333b,0xac1b529c75aaf3590f0f3c5b37d2db78d150d0adfb9c9de400e4c5431f1c44ab,0x0558cafcbea68b9cdde133590be9e8369270a0068dc72dd94bfe83b806b0a3cb,0x6cd26e4a8facd00687ae31eae01713a0921f018abdc402dbe89542bb5abf05b5,0x787dd7a2afe2577ab66353f99bdb4bd202bdbb3962dca22981a7b126b6bcca79,0x5b6945161589a0244799f5a62dd3a0fa4372c912d9fec900391a6cbe5fa3ce0e,0x5a5bfabf85c3e69fb4ff8d0703614b077394f9a3405e67742d37404e29e9e848,0x0a4d058db120123786d2fa670f54447ae5216d31637ad11a260799a766e40897,0xaa3553f76e242ea114d924b31e987cbb9bc421a855f345ee59c4cb2568e02277,0x5bcc649cffcffc6107d0662337d25ddaabf61cf338ddd5e233ed7cb493aaf2c1,0x4a5636fbc86a45cb95732350b0e6156157b4af8150ced8559aa82ec077a56f6f,0x444260b65364de24baffc13e2ea28f4ac70fad7b28e1468c94a3a86e55800428,0x3d8db4010af468d8ba8e2bb97d104c887bcc86dbcef774a1426946a392a8a1de,0x0e6e19e9361e7d0d1eabf2c13016fcbf7fce7583023e03d394150f765fd15524,0x8d19ec3ff54da167d6cef73decca85b0acef96b6d902d96c1287b833ce666f6e,0x481f814b9e3257b658be69288a0c0ffc7b1fbe04dc0499470a5555323fc27fce,0x6aa8d29f7477dc1723dcd7543fe7044b34199f195051eac5753cc18bfda43044,0xb2f2e2fa3aa6608a5dbe94389f11567ce7b8b11ac139756269e122502ce8ad53,0xa47fc50fd83d67a8f125b367d3ae14aac5d6ee676a97a7fe6003e7c4b9a2a688]
