# ETH-AVAX

LicenseManager Smart Contract
The LicenseManager smart contract is designed to manage the eligibility for a driving license based on users' ages and vehicle ownership statuses.

Prerequisites
Solidity version ^0.8.0
Ethereum development environment (Remix IDE, Truffle, Ganache, etc.)
Overview
The LicenseManager contract has the following features:

Store and update user ages.
Store and update vehicle ownership statuses.
Verify driving license eligibility based on age and vehicle ownership status.
Contract Details
Mappings
mapping(address => uint) private userAge;
Stores the age of each user. The key is the user's address, and the value is an unsigned integer representing their age.
mapping(address => bool) private hasVehicle;
Stores the vehicle ownership status of each user. The key is the user's address, and the value is a boolean indicating whether the user owns a vehicle.
Functions
function updateAge(uint _age) public

Updates the age of the sender.
Parameters: _age (uint) - The age to set for the user.
Validates that the age is within a reasonable range (greater than 0 and less than 150).
function updateVehicleOwnership(bool _hasVehicle) public

Updates the vehicle ownership status of the sender.
Parameters: _hasVehicle (bool) - The vehicle ownership status to set for the user.
function verifyEligibility() public view returns (bool)

Verifies if the sender is eligible for a driving license.
Returns true if the user is eligible, revert otherwise.
Checks that the user's age is set and is 18 or older, and the vehicle ownership status is true.
