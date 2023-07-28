# SOLIDITY TOKEN PROJECT

This Solidity program is a simple "CREATE A TOKEN" program that developing smart contracts in Solidity programming language. 

## Description

This program is a smart contract name as "MY TOKEN" written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract have public variables that store the details about our coin (Token Name, Token Abbrv., Total Supply), contract has a mapping of addresses to balances (address => uint),The contract has two function that are "mint" and "burn" function, a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount,a burn function, which works the opposite of the mint function,  burn function has conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned. . This program serves as a simple and straightforward introduction to Solidity programming.

### Executing program

To run MY TOKEN program, we use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once we are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., PROJECT.sol). 

```javascript
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tname = "tn";
    string public tAbbrv = "ta";
    uint public tsupply = 0;

    // mapping variable here
    mapping (address=> uint) public balances;

    // mint function
    function mint(address _add, uint _val) public {
        tsupply += _val;
        balances[_add] += _val;

    }

    // burn function
    function burn(address _add, uint _val) public {
        if(balances[_add] >= _val){
            tsupply -= _val;
            balances[_add]-= _val;
        }
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" , and then click on the "PROJECT.sol" button.

Once the code is compiled, we deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar."MYTOKEN-PROJECT.SOL " contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, after that we copy the address of my token and past it in the MINT function and BURN function and in Balance after that we can interact with it by calling the MINT function. Click on the "MYTOKEN" contract in the left-hand sidebar, and then click on the "BURN" function. Finally, click on the "tsupply" 

## Video Walkthrough
https://www.loom.com/share/02a182c98b0e43c4ada24f459464c39a

## License

This project is licensed under the MIT License.
