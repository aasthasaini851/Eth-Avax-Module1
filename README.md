# Water Supply Management Contract
This Solidity contract, named Aastha, is designed for managing water supply. It provides functionality to check if the water tank is full, stop the water supply, and retrieve the number of times certain functions are called.

# Contract Details
# State Variables:

tankFull: Indicates whether the water tank is full or not.
waterSupply: Indicates whether the water supply is active or not.
finalCall: Tracks the number of times the ifAlreadyFull function is called.
# Events:

WaterSupplyStatus(bool waterSupply): Notifies the status of the water supply.
# Functions:

ifAlreadyFull(): Checks if the water tank is already full.
getFinalCall(): Retrieves the number of times the ifAlreadyFull function is called.
stopWaterSupply(): Stops the water supply if the tank is full.
# Usage
Deploy the Contract: Deploy the Aastha contract to your preferred Ethereum network.

# Interacting with the Contract:

Call the ifAlreadyFull function to check if the water tank is full.
Call the stopWaterSupply function to stop the water supply if the tank is full.
Call the getFinalCall function to retrieve the number of times the ifAlreadyFull function is called.


# License
This contract is released under the MIT License.
