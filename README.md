# CrypToken(Crypto Token)

The CrypToken is a token contract that uses the Solidity programming language to display account balance and transactions. All of the coded variables' functions will be explained in this program. The cryptocurrency and blockchain communities will benefit from the Cryptoken.

## Description

On the Ethereum Blockchain, the CrypToken is a smart contract created using the solidity program. With the help of this program, the user can add and subtract transactions from accounts, and the balance of amounts input and output will be displayed. 

### Procedures

a) To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

b) Click the "Create new file" (paper logo) then type the any name you want for your file and add .sol (e.g. MyToken.sol).

c) Copy the code and paste to your workplace.

```// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract CrypToken {

   // public variables here
    string public TokenName = "CrypToken";
    string public TokenAcro = "CT";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _amount) public {
        totalSupply += _amount;
        balances[_address] += _amount;
    }

    // burn function
    function burn(address _address, uint _amount) public {
        if(balances[_address] >= _amount){
            totalSupply -= _amount;
            balances[_address] -= _amount;
        }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile"+ (the name of your file) button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the (name of your file) contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, scroll down and look for the "Deployed Contracts" after that go to you file to see all. Kindly copy the transaction account then paste in the mint section and enter the desired amount, after clicking see all in the mint area. Click the "transact"

After the "transact" button, paste the transaction account again in the "balances section" and then click all the buttons (balances, TokenAcro, TokenName, and totalSupply) to view the outcome.

Repeat the procedure for the "mint" part for the "burn" section, where the quantity you enter will be subtracted to the total balance.



## Authors

Junel Symon Closa Dela Cruz

BSIT 2.5

[@symondlcrz](https://www.instagram.com/symondlcrz/)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
