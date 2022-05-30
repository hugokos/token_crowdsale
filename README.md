## Token Crowdsale

This project is a non-fungible token called KaseiCoin that is ERC-20 compliant and that will be minted by using a `Crowdsale` contract from the OpenZeppelin Solidity library.

The crowdsale contract will manage the entire crowdsale process, allowing users to send ether to the contract and in return receive KAI, or KaseiCoin tokens. The contract will mint the tokens automatically and distribute them to buyers in one transaction.

## Technologies

Project uses:

[Solidity](https://docs.soliditylang.org/en/v0.8.14/)

[Remix IDE](https://remix-project.org/)

[Ganache](https://trufflesuite.com/ganache/)

[OpenZepplin](https://www.openzeppelin.com/contracts)
---

## Installation Guide

# Complete the following steps:

Launch solidity code in Remix IDE to deploy and run transactions on the blockchain


---

## Usage

Utilise Remix to interact with the smart contract. You can set accounts for the joint savings account and utilize the deposit and withdrawl smart contract. See example screenshots below:



**Sample Code:**
/*
contract KaseiCoinCrowdsaleDeployer {
    // Create an `address public` variable called `kasei_token_address`.
    address public kasei_token_address;    
    // Create an `address public` variable called `kasei_crowdsale_address`.
    address public kasei_crowdsale_address;

    // Add the constructor.
    constructor(
       string memory name,
        string memory symbol,
        address payable wallet // this address will receive all Ether raised by the sale
    ) public {
        // Create a new instance of the KaseiCoin contract.
        KaseiCoin token = new KaseiCoin(name, symbol, 0);
        
        // Assign the token contract’s address to the `kasei_token_address` variable.
        kasei_token_address = address(token);

        // Create a new instance of the `KaseiCoinCrowdsale` contract
        KaseiCoinCrowdsale kasei_crowdsale = new KaseiCoinCrowdsale(1, wallet, token);
            
        // Aassign the `KaseiCoinCrowdsale` contract’s address to the `kasei_crowdsale_address` variable.
        kasei_crowdsale_address = address(kasei_crowdsale);

        // Set the `KaseiCoinCrowdsale` contract as a minter
        token.addMinter(kasei_crowdsale_address);
        
        // Have the `KaseiCoinCrowdsaleDeployer` renounce its minter role.
        token.renounceMinter();
    }
}
*/
```

**Screen Shots from Ganache**


---

## Contributors

Hugo Kostelni

---

## License

Open Source
'