# MyContract

MyContract is a simple Solidity smart contract that allows users to set, get, increment, and decrement a value.

## Features

- **Set Value**: Allows setting a value.
- **Get Value**: Allows retrieving the current value.
- **Increment Value**: Allows incrementing the current value by 1.
- **Decrement Value**: Allows decrementing the current value by 1, ensuring it doesn't go below zero.

## Contract Functions

## setValue

function setValue(uint256 _value) public
Sets the value to _value.

## getValue

function getValue() public view returns (uint256)
Returns the current value.

## incrementValue

function incrementValue() public
Increments the current value by 1.


## decrementValue

function decrementValue() public
Decrements the current value by 1. Ensures the value does not go below zero.

Usage
Deploying the Contract
Use a development environment like Remix or a local Ethereum development setup.
Copy the contract code into a new Solidity file (e.g., MyContract.sol).
Compile the contract.
Deploy the contract to your desired network.
Interacting with the Contract
Set Value: Call the setValue function with a desired value.
Get Value: Call the getValue function to retrieve the current value.
Increment Value: Call the incrementValue function to increase the value by 1.
Decrement Value: Call the decrementValue function to decrease the value by 1. Note that the value will not decrement below zero.

Example

    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.0;

    contract MyContract {
    uint256 private value;

    // Function to set the value
    function setValue(uint256 _value) public {
        value = _value;
    }

    // Function to get the value
    function getValue() public view returns (uint256) {
        return value;
    }

    // Function to increment the value
    function incrementValue() public {
        value += 1;
    }

    // Function to decrement the value
    function decrementValue() public {
        require(value > 0, "Value cannot be less than zero");
        value -= 1;
    }
    }

##License
This project is licensed under the MIT License.
