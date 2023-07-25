# METACRAFTERS ASSESSMENT

# MyToken Contract

This is a basic ERC-20 token smart contract implemented in Solidity. It includes functionalities to mint and burn tokens, as well as store details about the token, such as name, abbreviation, and total supply.

## Requirements

1. The contract has public variables that store the details about the coin (Token Name, Token Abbrv., Total Supply).
2. It uses a mapping of addresses to balances to keep track of the token balances of each address.
3. The contract includes a `mint` function that takes two parameters: an address and a value. This function increases the total supply by the specified value and increases the balance of the "sender" address by that amount.
4. It also has a `burn` function, which works in the opposite way of the mint function, as it destroys tokens. It takes an address and a value just like the mint function and deducts the value from the total supply and from the balance of the "sender" address.
5. The `burn` function includes conditionals to make sure the balance of the "sender" is greater than or equal to the amount that is supposed to be burned.


## Contract Details

### Token Details

- Token Name: (Value specified during deployment)
- Token Abbreviation: (Value specified during deployment)
- Total Supply: (Value specified during deployment)

### Public Functions

1. `mint(address _to, uint256 _value)`: This function allows minting new tokens and increasing the total supply. It takes two parameters: `_to` (the address to mint tokens to) and `_value` (the number of tokens to mint). The function is accessible to everyone on the Ethereum network.

2. `burn(uint256 _value)`: This function allows burning tokens and reducing the total supply. It takes one parameter: `_value` (the number of tokens to burn). Before burning the tokens, the function checks if the balance of the sender (`msg.sender`) is greater than or equal to `_value`. This prevents burning more tokens than the sender owns. The function is accessible to everyone on the Ethereum network.

## How to Deploy and Use

To deploy and interact with this contract, you can use Remix IDE (https://remix.ethereum.org/) or other Ethereum development tools.

1. Deploy the contract on an Ethereum network of your choice. During deployment, provide the Token Name, Token Abbreviation, and the initial Total Supply.

2. After deployment, you can call the `mint` function to create new tokens and increase the total supply. You need to specify the recipient's address and the number of tokens to mint.

3. Similarly, you can use the `burn` function to destroy tokens and reduce the total supply. Make sure that the balance of the "sender" address is greater than or equal to the amount to be burned.
   
4. The token details and balances can be queried using the respective public variables and the `balances` mapping.

Please note that this contract is basic and may not include advanced functionalities like transfer, approve, and other standard ERC-20 functions. Consider extending this contract to meet specific requirements or using it as a starting point for more complex token contracts.

## License

This contract is released under the MIT License. Feel free to use, modify, and distribute it as per the terms of the license.

