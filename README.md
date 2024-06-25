Overview
The MyToken contract allows for the creation and management of a custom token. It includes features for initializing the token with a name, symbol, and initial supply, as well as functions to mint (create) new tokens and burn (destroy) existing tokens.

Functionality
Token Details Initialization

Public Variables: name, symbol, and totalSupply are public variables that store the token's name, symbol, and total supply, respectively. They can be accessed by anyone.
Balances Mapping: balances is a mapping that keeps track of the number of tokens each address holds.
Constructor

The constructor initializes the contract with the token's name (_name), symbol (_symbol), and initial supply (_initialSupply).
It sets the totalSupply to the initial supply value and assigns all these initial tokens to the deployer's address (msg.sender).
Mint Function

The mint function allows for the creation of new tokens.
Parameters:
_to: The address to which the new tokens will be assigned.
_value: The number of tokens to be created.
Functionality:
Increases the totalSupply by _value.
Increases the balance of the _to address by _value.
Burn Function

The burn function allows for the destruction of tokens.
Parameters:
_from: The address from which the tokens will be burned.
_value: The number of tokens to be destroyed.
Functionality:
Ensures the _from address has at least _value tokens to burn by using the require statement.
Decreases the totalSupply by _value.
Decreases the balance of the _from address by _value.
Summary
Initialization: The token is initialized with a name, symbol, and initial supply. The deployer receives all the initial tokens.
Minting Tokens: The contract allows the creation of new tokens, increasing both the total supply and the recipient's balance.
Burning Tokens: The contract allows the destruction of existing tokens, decreasing both the total supply and the owner's balance, with a check to ensure sufficient balance for burning.
