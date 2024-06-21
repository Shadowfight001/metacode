MyToken Smart Contract

Overview-

This smart contract is a simple implementation of a cryptocurrency token using Solidity. It includes the ability to create (mint) and destroy (burn) tokens, while keeping track of the total supply and individual balances of token holders.

Features-

Public Variables:

myTokenName: The name of the token.
myTokenAbbr: The abbreviation of the token.
totalSupply: The total number of tokens in circulation.

Mapping:

balance: It basically maps addresses to their respective token balances.

Functions:

mint: Creates new tokens and adds them to a specified address.
burn: Destroys tokens from a specified address, reducing the total supply, with a check to ensure the address has enough tokens to burn.
