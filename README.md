# Ethereum Dapp for Tracking Items through Supply Chain

## Submission Information
- [x] [UML Diagrams](#UML-Diagrams)
- [x] [Libraries Write-up](#Libraries-Write-up)
- [x] [IPFS Write-up](#IPFS-Write-up)
- [x] [General Write-up](#General-Write-up)

## Summary
The purpose of this project is to learn lower level components of establishing a sound web service architecture using Blockchain.  In this project, I created a dApp coffee supply chain solution on Ethereum using smart contracts with role-based permissions to track and verify a product's authenticity.  The code for this project is in the `coffee/` folder.

## Testing The dApp
Below is the output from my tests in the `test` folder.  To run the tests, simply execute `truffle test` at the command line.
```
Contract Owner: accounts[0]  0xb3609C9dB9Dd606Ba284220Bbf6F40CF7E10Ab08
Farmer: accounts[1]  0x29f4f9848967f996880A6987C6a359246EF0Bc57
Distributor: accounts[2]  0x510586612247bed21257207057c216eCC26F55bD
Retailer: accounts[3]  0xa11243014DeB418B92E74dC5BA300F69F2554364
Consumer: accounts[4]  0x9FB83E8dc0DCf739E05c01B93CB90E3d2d0F03E7


  Contract: SupplyChain
    ✓ Test that roles are correctly added to contract (184ms)
    ✓ Testing smart contract function harvestItem() that allows a farmer to harvest coffee (108ms)
    ✓ Testing smart contract function processItem() that allows a farmer to process coffee (58ms)
    ✓ Testing smart contract function packItem() that allows a farmer to pack coffee (58ms)
    ✓ Testing smart contract function sellItem() that allows a farmer to sell coffee (55ms)
    ✓ Testing smart contract function buyItem() that allows a distributor to buy coffee (67ms)
    ✓ Testing smart contract function shipItem() that allows a distributor to ship coffee (66ms)
    ✓ Testing smart contract function receiveItem() that allows a retailer to mark coffee received (65ms)
    ✓ Testing smart contract function purchaseItem() that allows a consumer to purchase coffee (52ms)
    ✓ Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain
    ✓ Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain


  11 passing (821ms)
```

## Running the dApp
Screenshots etc

### UML Diagrams
As part of the project planning, I created UML activity, sequence, and state diagrams which are included below.

#### Activity Diagram
![Activity Diagram](images/uml/activity_diagram.png)

#### Sequence Diagram
![Sequence Diagram](images/uml/sequence_diagram.png)

#### State Diagram
![State Diagram](images/uml/state_diagram.png)

#### Classes (Data Model)
![Classes Diagram](images/uml/class_diagram.png)

### Libraries Write-up
Below are the dependencies in my `packages.json` file:
```json
"dependencies": {
    "solidity-docgen": "^0.5.7",
    "truffle": "^5.1.51",
    "truffle-assertions": "^0.9.2",
    "truffle-hdwallet-provider": "^1.0.17",
    "web3": "^1.3.0"
  }
```
**Used libraries**:

- `truffle`: truffle is a development framework for Ethereum that makes it easy to compile, test, and migrate solidity contracts to Ethereum networks.  For example, I used `truffle` to deploy my smart contracts to the `Rinkeby` test network.
- `truffle-assertions`: the assertions library for truffle has convenience functions designed for solidity assertions inside of truffle tests.  I used the assertion syntax to test whether my contracts correctly emitted different events as expected.
- `truffle-hdwallet-provider`: this libarary was used to enable my truffle deployments to spend test coins from my Metamask wallet on the Rinkeby network as part of deploying my contracts to `Rinkeby`
- `web3`:


The Rinkeby contract address for this project is: `0xb2d02546AE8f64539fb365885E4A90b9ce0B56eC`
