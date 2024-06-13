REMIX DEFAULT WORKSPACE

Remix default workspace is present when:
i. Remix loads for the very first time 
ii. A new workspace is created with 'Default' template
iii. There are no files existing in the File Explorer

This workspace contains 3 directories:

1. 'contracts': Holds three contracts with increasing levels of complexity.
2. 'scripts': Contains four typescript files to deploy a contract. It is explained below.
3. 'tests': Contains one Solidity test file for 'Ballot' contract & one JS test file for 'Storage' contract.

SCRIPTS

The 'scripts' folder has four typescript files which help to deploy the 'Storage' contract using 'web3.js' and 'ethers.js' libraries.

For the deployment of any other contract, just update the contract's name from 'Storage' to the desired contract and provide constructor arguments accordingly 
in the file `deploy_with_ethers.ts` or  `deploy_with_web3.ts`

In the 'tests' folder there is a script containing Mocha-Chai unit tests for 'Storage' contract.

To run a script, right click on file name in the file explorer and click 'Run'. Remember, Solidity file must already be compiled.
Output from script will appear in remix terminal.

Please note, require/import is supported in a limited manner for Remix supported modules.
For now, modules supported by Remix are ethers, web3, swarmgw, chai, multihashes, remix and hardhat only for hardhat.ethers object/plugin.
For unsupported modules, an error like this will be thrown: '<module_name> module require is not supported by Remix IDE' will be shown.
This Solidity contract defines a simple token named "MyToken" with basic minting and burning functionality.

This contract represents a token system named "Ritesh" with the abbreviation "RT". It allows for the minting and burning of tokens while maintaining records of the total token supply and individual token balances.

Public Variables:

Tk_Name: Stores the name of the token, set to "Ritesh".
Tk_Abbrv: Stores the abbreviation of the token, set to "RT".
Total_Supply: Tracks the total supply of the token, initialized to 0.

Mapping:

Token_balance: Maps addresses to their respective token balances.

Mint Function:

Mint(address _address, uint _number): Increases the total supply of tokens by the specified amount (_number) and adds the same amount to the balance of the specified address (_address).

Burn Function:

Burn(address _address, uint _number): Checks if the specified address (_address) has a token balance greater than or equal to the specified amount (_number). If the condition is met, it decreases the total token supply and the balance of the specified address by the specified amount.

This contract serves as a basic framework for managing token minting and burning on the Ethereum blockchain.
