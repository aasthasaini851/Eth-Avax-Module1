# Smart Contract
This Solidity smart contract facilitates weather checking and manages the need for a raincoat. It tracks the number of times the weather has been checked and provides the option to wear a raincoat when it's rainy.

# Overview
The contract includes:

Boolean variables to indicate if it is currently rainy and if a raincoat is needed.
A counter to track how many times the weather has been checked.
Functions to check the weather, wear a raincoat, and retrieve the number of weather checks.
An event to log the status of the raincoat.
# Variables
bool public rainy: Indicates if it is currently rainy. Initially set to true.
bool public raincoat: Indicates if a raincoat is needed. Initially set to true.
uint256 public finalCall: Counter for how many times the weather has been checked. Initially set to 1.
# Events
event RaincoatStatus(bool raincoat): Logs the status of the raincoat.
# Functions
# weather()
Checks the weather condition.

Requires rainy to be true. If not, it stops and shows the message "IT IS NOT RAINY TODAY!!".
Increments the finalCall counter.
Uses assert to ensure finalCall is not zero.

# getFinalCall()
Returns the value of finalCall.
# wearRaincoat()
Wears a raincoat if it's rainy.

If rainy is true, sets raincoat to true and emits the RaincoatStatus event.
If rainy is false, stops and shows the message "No Raincoat needed" using revert.
# Deployment
To deploy this contract, use Remix IDE or any Ethereum development environment. Make sure the Solidity compiler version is set to 0.8.18.

# Example Usage
Initial State:
rainy: true
raincoat: true
finalCall: 1
Check the Weather:
Call weather(). This will work since rainy is true.
Check Final Call:
Call getFinalCall() to get the current value of finalCall.
Wear Raincoat:
Call wearRaincoat(). This will emit the RaincoatStatus event if rainy is true.
# License
This project is licensed under the MIT License.
