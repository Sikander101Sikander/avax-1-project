# Eth+Avax-1-project

This project demonstrate that how the solidity functions,revert(),assert(),require() are work that is related to error handling.
## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a multiple function. This program serves as a simple and straightforward introduction to error handling in Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension(for eg:-Simpledivison.sol).
```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleDivision {
    // Function to perform division with basic checks
    function divide(uint256 numerator, uint256 denominator) public pure returns (uint256) {
        // Check that the denominator is not zero using require()
        require(denominator != 0, "Denominator cannot be zero");

        // Perform the division
        uint256 result = numerator / denominator;

        // Check that the result is valid using assert()
        assert(result <= numerator);

        return result;
    }

    // Function to demonstrate the use of revert() statement
    function alwaysFail() public pure {
        // Revert with an error message
        revert("This function always fails");
    }
}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "^0.8.0" (or another compatible version), and then click on the "Compile Simpledivision.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you need to enter thr value of numerator and denominator And then transact and now we can see total supply and final output.

## Authors

Contributors names and contact info

Sikander Singh Nanglu

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
