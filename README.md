Module 7 - Intermediate Lab: Creating An ERC20 Token
=======================
# Background
Smart contracts can be implemented through the use of blockchain technology with the Ethereum network. They allow for binding agreements between network participants that are handled by network consensus instead of a third party.

This assignment goes through the process of contract creation. Students will briefly implement the ERC20 interface using Solidity programming. Implementation of interfaces is a technique taught in CS1 classroom environments.

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

## Setting up your wallet and test Ethereum
1. Navigate to [MetaMask](https://metamask.io/) and install the extension for your browser (feel free to watch the introduction video, too).
2. Click the get started button and then click the create a wallet button.
3. Agree or decline the anonymous usage data collection.
4. Create a new, secure password. You can use [How Secure Is My Password](https://howsecureismypassword.net/) to check (be careful of similar services).
5. Enter and confirm your password in MetaMask, and click to acknowledge you agree to the Terms of Use (if you do). Then click create.
6. It is advisable to read the information on the next page and store your mnemonic phrase accordingly. Remember: this is for your eyes only, forever. It is all the information someone needs to someday steal all of the future value you may have in this wallet. And if you lose it, no-one can help you recover it.
7. Confirm you have your mnemonic phrase properly stored and accessible to you by clicking the words on the next page in the correct order. Then proceed, reading along the way, until you see your account balance. You should have 0 ETH ($0.00 USD).
8. In the top right, you should see a dropdown with 'Main Ethereum Network'. Click this and select 'Rinkeby Test Network'.
9. Click on the 'DEPOSIT' button to the right of your balance and in the overlay that appears, click 'GET ETHER' by Test Faucet.
10. A new tab sould open at https://www.rinkeby.io/#stats. On the left border of this page, click the middle button labeled 'Crypto Faucet'.
11. For the next step, Twitter is recommended, but you may use any listed option which works for you. Follow the instructions on the page you are redirected to in order to get your wallet funded with test currency. (If using Twitter, be sure to use the link to the tweet itself which you pasted your wallet's public address into.)
12. Wait until your account gets funded (up to 8 hours, 1 day, or 3 days, depending on your choice \[8 hours recommended\], but it may be as little as a few seconds or minutes).

## Editing the contract.sol file
1. [Download the sample contract](contract.sol) and [open it using the Remix Solidity IDE.](https://remix.ethereum.org/)

### Editing the comment block
This section will not affect the contract code. It is written to practice documentation and maintainance of code. 

| Line | Characters to change | Explanation |
| --- | --- | --- |
| 4 | [insert token name here] | Name for your token. |
| 6 | [insert wallet address to deploy here] | Address you created earlier. The smart contract must take funds from a wallet to initialize. |
| 7 | [insert token symbol here] | Symbol to identify your token shorthand. (example: "UHMC") |
| 8 | [insert token name here] | Name for your token. |
| 9 | [insert total supply of tokens here] | Total number of tokens in existance. |
| 10 | [insert decimal denomination per token, up to 18] | How do you want to break apart your token? Ethereum allows a maximum of 18 decimals. |

### Editing the contract constructor method

| Line | Characters to change | Explanation |
| --- | --- | --- |
| 107 | [TokenName] | The name of your token in CamelCase, as per Solidity convention. |
| 121 | [insert token symbol here] | Write your token symbol here, in all CAPS. |
| 122 | [insert token name here] | Write your token name here. |
| 123 | [insert token decimal denomination here] | Write the decimal denomination. |
| 125 | [insert token supply here] | Write the token supply, read line 124 to learn how to do this. |
| 126 | [insert your wallet address here] | Paste your wallet address here, this line and line 127 create the original transfer of Ethereum to the smart contract in order to initialize it. |
| 127 | [insert your wallet address here] | Paste your wallet address here, see above. |

## Deploying your contract to the Rinkeby testnet
1. After all the lines listed are edited, click on “Start to compile” on the top right corner of the Remix IDE.
2. After successful compilation, click on the 'Run' tab.
3. The four fields should already be filled out with:
    * Environment: Injected Web3 Rinkeby
    * Account: \[your wallet address\]
    * Gas limit: 3000000
    * Value 0 wei
4. In the next box, select the name of your coin in the dropdown, then click the 'Deploy' button.
5. Click on the MetaMask plugin icon in the top right of your browser, then click 'CONFIRM' in the popup to allow the transaction.
6. If all went well, you should now see your contract in the Deployed Contracts section in Remix. You may also find it by searching your wallet address on [rinkeby.etherscan.io](https://rinkeby.etherscan.io/) or navigating through the interface in the MetaMask plugin.
7. You can now interact with your contract by clicking the arrow on the left side of your deployed contract (in Remix) and then filling out the fields and clicking the buttons corresponding to methods in the contract. For example, clicking owner should return your wallet's address.

# Credits
Dr. Debasis Bhattacharya  
Mario Canul  
Saxon Knight  
Assignment possible thanks to the work of [Moritz Neto](https://twitter.com/mrtzneto) for the original contract.  
Special thanks to [James Maupin](https://github.com/jmsMaupin1) for help with testing and feedback.  
