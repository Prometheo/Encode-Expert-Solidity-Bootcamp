1.) What information is held for an Ethereum account: There are 4 info held for an Ethereum account, they are:
    
     1. The Nonce: An incremental digit that indicates the number of transactions sent from the ethereum account,
        it helps to make sure particular transactions only happen ones!
      2. Balance: The balance of native token held by this account(ETH,MATIC,BNB), denominated in Wei.
      3. codeHash: This is the hash of the computer code contained in an account, ususally an empty string for EOAs,
           but contract accounts contains heir programmed instructions.
      4. storageRoot: This is the hash of the account's storage trie(which is the hash of the storage content of the account)


2.) Where is the full Ethereum state held: Ethereum state is stored in the nodes participating in the Blockchain.

3.) What is a replay attack ? which 2 pieces of information can prevent it ?
    
    A play attack is basically carying out a transaction on two different networks,
    so basically if you signed off a transaction on Network one, 
    malicious user can take your signature in transaction1 on network1,
    create another transaction on Network 2 and use teh signature from Transaction1.
    This can be solved with the inclusion of blocknumber and chainId in your signature,
    this way, when the signature is taken to a different chain,
    the signature does not match.
   
   
4.) What checks are made on transactions for view functions ?

        Vew functions evoke transactions that only reads state, they do not modify state, hence when this kind of transactions come in,
        the data field is checked,
        since normally this field contains the code to be run by the evm for this function,
        the data is checked to make sure that there is no state modifying instructio,
            
