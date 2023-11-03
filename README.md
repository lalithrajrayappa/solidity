# Solidity

This is my third module final submission of solidity beginner course where I have created a token and deployed the smart contract in remix IDE.

## Description

In my project submission, I have created a token in which you can mint , burn and check the balance of an account by deploying the contract and interacting with it. The total supply has been set to 0 and the token name is named after a cartoon show - 'Tom&Jerry'

## Getting Started

### Installing the project

You can download the code and run it locally on your local code editor or follow the below step to deploy it on remix(online IDE)

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., solidity.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenname="Tom&Jerry";
    string public tokenabbrv="TJ";
    uint public totalsupply=0;
    // mapping variable here
    mapping(address => uint)public balance;
    // mint function
    function mint(address wallet_address, uint  inpvalue)public {
      totalsupply += inpvalue;
      balance[wallet_address] += inpvalue;
   }
    // burn function
   function burn(address wallet_address, uint inpvalue)public {
      if(balance[wallet_address]>= inpvalue){
        totalsupply -= inpvalue;
        balance[wallet_address] -= inpvalue;
      }
     }
  }

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile solidity.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "solidity" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it . You will be able to successfully mint , burn Tom&Jerry tokens which is pretty cool! You will also be able to check the balance of each address to check how many Tom&Jerry tokens you have .
## Authors

Lalith Raj 

[@lalithrajrayappa@gmail.com]

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
