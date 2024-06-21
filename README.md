MyToken Smart Contract

Overview-

This smart contract is a simple implementation of a cryptocurrency token using Solidity. It includes the ability to create (mint) and destroy (burn) tokens, while keeping track of the total supply and individual balances of token holders.

Features-

1. **Public Variables**:
    - `myTokenName`: The name of the token.
    - `myTokenAbbr`: The abbreviation of the token.
    - `totalSupply`: The total number of tokens in circulation.
2. **Mapping**:
    - `balance`: It basically maps addressws to their respective token balances.
3. **Functions**:
    - `mint`: Creates new tokens and adds them to a specified address.
    - `burn`: Destroys tokens from a specified address, reducing the total supply, with a check to ensure the address has enough tokens to burn.


Contract Details-

Variables:
    string public `myTokenName` = "Udit";
    string public `myTokenAbbr` = "Udi";
    uint public `totalSupply` = 0;

Mapping:
    mapping (address => uint) public `balance`;

Functions:
    **mint**- This function increases the totalSupply by _value and adds the same amount to the balance of _address.
    **burn**- This function decreases the totalSupply by _value and subtracts the same amount from the balance of _address. It checks if the balance of _address is 
          sufficient to burn the specified amount.


Usage:
  1- Deploy the MyToken contract to your preferred Ethereum network.
  2- Use the mint function to increase the token supply and assign tokens to specific addresses.
  3- Use the burn function to decrease the token supply and remove tokens from specific addresses, ensuring sufficient balance.
