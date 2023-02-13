## Ethers Simple Storage


to compile our code:
	yarn solcjs --bin --abi --include-path node_modules/ --base-path . -o . SimpleStorage.sol
	
	
in package.json we can add this bash code line to compile.

we need abi and binray compile.---> for this we need package called fs.

when we send a transaction we have data object that we can fill with binary that 
tells the ethereum that tells our blockchain to deploy our smart contract.

1 ) make the transaction detail ---> tx
2 ) sign the transaction ---> can be sent
	we need sign our transaction and sign it to our blockchain
	

if we call just sendTransaction() with detail first singning and then sending


recap: 

we're going to connect our ganache instance, connect a wallet with a private key and provider.

we grab the ABI and BINARY of our contract and connect them to a new contractFactory object witch is connected to our wallet.
so that wallet we'll deploy the contract.

we'll deploy the contract with deploy() method and we wait one block for that transaction finish.


when we call the function on the contract we get a transaction response, when we wait for the transaction response to finish we get the transaction receipt.



we're going to set this script up to run our encrypt key one time and then we 
can remove our private key from anywhere in our workspace.

then save that in the new file(after encrypt).

after that we can delete our private key from our .env script.
read that file in our deploy script and create a wallet from that.

we're not connecting our wallet with a provider.
when we make our transaction with our contractFactory we need to make sure the
wallet knows about the provider here.

----> wallet = await wallet.connect(provider)

we can also add prettier as a node js module that can tell other users who don't have a vs code:
	after we install prettier with: $yarn add prettier prettier-plugin-solidity
	
	
	
	
dploying to a testnet:


