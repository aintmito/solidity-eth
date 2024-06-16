# MyToken

This Solidity program is a simple Contract program that demonstrates the basic syntax and functionaly of the Solidity programming language. The purpose of this program is to serve as a starting point for people like me who are new to Solidity and wants to know the fundamentals of how crypto wallet works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions that mints and burns tokens. This program serves as a simple introduction to Solidity programming. It can be used as a basis and can further improve to a more complex projects in the future.

## Getting Started

### Executing program

* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

* Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSuppply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public
    {
        totalSuppply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public
    {
        if(balances[_address] >= _value)
        {
            totalSuppply -= _value;
            balances[_address] -= _value;
        }
        
    }
}
```

* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

* Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

* Once the contract is deployed, you can interact with it by checking the tokenName, tokenAbbr, and totalSupply variables to check their values. After checking their values, in the left-hand sidebar, scroll up so you can check the "Account" that gives example addresses that you can use for testing the program and copy the default address that is already selecting in the dropdown menu.

* Once the address is copied, select the mint function from the left-hand side bar and paste the address in the _address field and enter a value that is greater than 0 in the _vvalue field, then press transact. Now press the totalSupply to call the variable to check the updated value.

* Lastly, select the burn function from the left-hand side bar and paste the address in the _address field and enter a non-negative value in the _value field and make sure that the value is less than the totalSupply so you'll be able to check if it's really working, press transact after entering a value. Now press the totalSupply to call the variable to check the updated value.

## Authors

[Miguel Andre Encomienda](https://www.linkedin.com/in/miguel-encomienda-526593292/)


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details