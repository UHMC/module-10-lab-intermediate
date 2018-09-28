Nifty Assignment---Creating an ERC20 token
=======================
# Background
Smart contracts can be implemented into blockchain technology through the Ethereum blockchain network. They allow for binding agreements between network participants that are handled by network consensus instead of a third party. 

# Meta-information
| Attribute | Explanation |
| ------------- | ------------- |
| Summary | Create a basic smart contract on an Ethereum test network while going over every method of implementation of the ERC20 specification  |
| Topics  | Solidity programming, blockchain development  |
| Audience | Appropriate for CS1 or a later course. |
| Difficulty | Completing the assignment is easy, as it is just editing a contract and deploying it. However, full understanding and extension of the contract can be difficult. |
| Strengths | The strength of this assignment is that it allows students to get exposed to technology that they hear about all the time (blockchain) and creates a seed of learning that they can research further. |
| Weaknesses | It may be difficult for students to extend their first smart contract. They might require more in-depth knowledge about how transactions work in blockchain settings. | 
| Dependencies | Requires the understanding of implementing interfaces in an object-oriented language. It also requires the understanding of blockchain transactions in order to further extend past the assignment. |
| Variants | Could be used in an introductory course of OOP languages, as means to introduce how to implement a specification. |

# Assignment instructions
1. Navigate to MyEtherWallet, a website for offline wallet access, which can be retrieved at https://www.myetherwallet.com/ 
On the top right corner of the webpage, change the network to “Rinkeby (etherscan.io)” in order to create a wallet compatible with that test network.
2. Create a wallet by entering a password that will be used to encrypt the wallet, and follow the prompts. Save your wallet’s JSON file and the private key.
3. Once a wallet that is compatible with the Rinkeby testnet is created, one can obtain Rinkeby ETH at no cost, this can be done using the faucet service on http://rinkeby,io by clicking the link on the left side called “Crypto faucet” and follow their instructions to obtain the ETH.
4. Download the following sample contract and open it using the Remix Solidity IDE: Sample contract: https://github.com/UHMC/sample-smart-contract/blob/master/contract.sol Remix Solidity IDE: https://remix.ethereum.org/ 
5. Go to line 4 and remove [insert token name here], and add your own token name.
6. Go to line 6 and remove [insert wallet address to deploy here], and add the address you created using MyEtherWallet
7. Go to line 7 and remove [insert token symbol here], and add your own symbol (similar to a stock ticker)
8. Go to line 8 and remove [insert token name here], and add your own token name
9. Go to line 9 and remove [insert total supply of tokens here], and add the supply of tokens wanted
10. Go to line 10 and remove [insert decimal denomination per token, up to 18], and add the denomination that you want to use for your tokens. 
11. Go to line 107 and remove [TokenName], and add the name of your token in CamelCase
12. Go to line 120 and remove [TokenName], and add the same name you used in line 107
13. Go to line 121 and remove [insert token symbol here], and add the symbol you wrote in line 7
14. Go to line 122 and remove [insert token name here], and add the name you used on line 8
15. Go to line 123 and remove [insert token decimal denomination here]
16. Go to line 125 and remove [insert token supply here], and add the total number of tokens to be generated and add 0s to the end of it by the number of decimals in line 10 Example: if decimal denomination is 5, and I want 100 tokens, the number to write here would be 10000000
17. Go to line 126 and remove [insert your wallet address here] and add the address from line 6
18. Go to line 127 and remove [insert your wallet address here] and add the address from line 6
19. After all the lines listed are edited, click on “Start to compile” on the top right corner of the Remix IDE.
20. Click the drop down box near the “Start to compile” button and click on the name of your token. This is referencing the name of the constructor method. 
21. Click on details and copy the text under “BYTECODE.” 
