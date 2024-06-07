# Smart Contract
This Solidity smart contract simulates checking the weather and managing the need for a raincoat. It tracks the number of times the weather has been checked and the number of times it has rained.

# Overview
The contract includes:

Boolean variables to indicate if it is rainy and if a raincoat is needed.
Counters to track how many times the weather has been checked and how many times it has rained.
Functions to interact with these variables and counters.
Events to log significant actions and state changes.
# Variables
bool public rainy: Indicates if it is currently rainy. Initially set to true.
bool public raincoat: Indicates if a raincoat is needed. Initially set to true.
uint256 public finalCall: Counter for how many times the weather has been checked. Initially set to 1.
uint256 public rainCount: Counter for how many times it has rained. Initially set to 1.
# Events
event WeatherChecked(bool rainy): Logs the weather status when checked.
event RaincoatStatus(bool raincoat): Logs the raincoat status.
event WeatherChanged(bool newStatus): Logs when the weather changes.
event RainCountUpdated(uint256 rainCount): Logs the updated rain count when it rains.

# Functions
weather()
Checks the weather condition and updates counters accordingly.

Requires rainy to be true. If not, it stops and shows the message "IT IS NOT RAINY TODAY!!".
Increments the finalCall counter.
Uses assert to ensure finalCall is not zero.
Increments the rainCount counter.
Emits RainCountUpdated and WeatherChecked events.

weatherChanger()
Toggles the rainy state.

Changes rainy from true to false or vice versa.
Emits WeatherChanged event.
getFinalCall()
Returns the value of finalCall.

wearRaincoat()
Determines if a raincoat is needed based on the weather.

If rainy is true, sets raincoat to true and emits RaincoatStatus event.
If rainy is false, stops and shows the message "No raincoat needed" using revert.

getRainCount()
Returns the value of rainCount.

# Deployment
Deployment
To deploy this contract, use Remix IDE or any Ethereum development environment (like Hardhat or Truffle). Make sure the Solidity compiler version is set to 0.8.18.

# Example Usage
Deploy the Contract: Use Remix IDE or any compatible Ethereum development environment.
Initial State:
rainy: true
raincoat: true
finalCall: 1
rainCount: 1
Check the Weather:
Call weather(). This will work since rainy is true.
Change the Weather:
Call weatherChanger(). This will toggle rainy to false.
Check Final Call:
Call getFinalCall() to get the current value of finalCall.
Wear Raincoat:
Call wearRaincoat(). This will fail if rainy is false.
License
This project is licensed under the MIT License.
This README should provide a comprehensive guide for understanding, deploying, and using the Aastha smart contract.
