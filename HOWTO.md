
## How to Claim OGX Tokens

Step 1.  
Confirm that you have previously claimed crank anywhere from 1 to 3,200,000 (already minted or still waiting won't matter, if you own the crank, you qualify).  

Step 2.  
Locate your merkle proof in one of the files inside the proofs folder https://github.com/ph4n70mr1ddl3r/ogx/tree/main/proofs.  
There are 3,200,000 lines in 320 files ordered by crank. Each line has 4 data that is needed when claiming.  
When opening the file, make sure you have word wrap disabled since these are long lines.  
The format is crank, address, term, proof. The proof is enclosed in brackets and is composed of 32 byte hex numbers separated by commas.  
When using etherscan to claim, you'll need to remove the quotation marks in each hash.  

Step 3.  
Go to the contract https://etherscan.io/address/0x994e4534f2ee11fb0eccea68bdfe83d7d7e15034 then open the contract tab then press the write contract button. 

Step 4.  
Press Connect to Web3 button.  

Step 5.  
Go to the 4th function named claim, then fill up the 4 arguments.  
In the 4th argument (proof bytes32[]), make sure you remove the quotation marks.  
So it should look like this:  
`[0x74854f1dea34ec8d0f4ba91782a32fa7cc915a6a6937b98a092e0ac4d4abe9d7,0xb5dfa60b9b938ec0333ede31a3f75064c479ff487919bb19699c8e66fa8d94d3,0x1f7b1c46b4f03bc876993109ff58935f75afc32ea96177dfa5425e64ee8569c8,0x292badb35bfc9dc2df01bc60c90fa2b93d7a4227369eabcfd3321fab8856333b,0xac1b529c75aaf3590f0f3c5b37d2db78d150d0adfb9c9de400e4c5431f1c44ab,0x0558cafcbea68b9cdde133590be9e8369270a0068dc72dd94bfe83b806b0a3cb,0x6cd26e4a8facd00687ae31eae01713a0921f018abdc402dbe89542bb5abf05b5,0x5a5bfabf85c3e69fb4ff8d0703614b077394f9a3405e67742d37404e29e9e848,0x0a4d058db120123786d2fa670f54447ae5216d31637ad11a260799a766e40897]`

The actual proof should be longer since it has more hexadecimal numbers than the one shown here.  

Step 6.  
Press Write and and confirm the transaction in metamask.  
You can use any account to pay for the transaction but the OGX tokens will be sent as indicated in the proofsXXX.txt file since that's the original address that you specified when you initially claimed your crank.  

Step 7.  
Once the transaction is confirmed, you should get OGX tokens equal to the term days of your crank. You'll be able to transfer it after block 18,250,000.  

Step 8.
Repeat the same process for each crank that you own.  

Congratulations.
Why you should claim OGX? It could be something big, it's relatively scrace, there should be no whales and at block 20,000,000 claiming will stop.  
