MyToken Smart Contract
Overview
This smart contract is a simple implementation of a cryptocurrency token using Solidity. It includes the ability to create (mint) and destroy (burn) tokens, while keeping track of the total supply and individual balances of token holders.

Features
Public Variables:

myTokenName: The name of the token.
myTokenAbbr: The abbreviation of the token.
totalSupply: The total number of tokens in circulation.
Mapping:

balance: It maps addresses to their respective token balances.
Functions:

mint: Creates new tokens and adds them to a specified address.
burn: Destroys tokens from a specified address, reducing the total supply, with a check to ensure the address has enough tokens to burn.
Contract Details
Variables
solidity
Copy code
string public myTokenName = "Udit";
string public myTokenAbbr = "Udi";
uint public totalSupply = 0;
Mapping
solidity
Copy code
mapping (address => uint) public balance;
Functions
mint
solidity
Copy code
function mint(address _address, uint _value) public {
    totalSupply += _value;
    balance[_address] += _value;
}
Description: This function increases the totalSupply by _value and adds the same amount to the balance of _address.
burn
solidity
Copy code
function burn(address _address, uint _value) public {
    if (balance[_address] >= _value) {
        totalSupply -= _value;
        balance[_address] -= _value;
    }
}
Description: This function decreases the totalSupply by _value and subtracts the same amount from the balance of _address. It checks if the balance of _address is sufficient to burn the specified amount.


















  
