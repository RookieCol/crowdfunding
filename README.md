# CrowdFunding Contract

This is a smart contract for crowdfunding in Ethereum blockchain.

## Requirements

* Node.js
* Hardhat
* Solidity

## Installation
### Clone the repository:
```console
git clone https://github.com/RookieCol/crowdfunding.git
```


### Install dependencies:
 ```console
 cd crowdfunding
npm install
 ```
## Usage

### Compile the contract:
```console
npx hardhat compile
```
### Deploy
```
npx hardhat run scripts/deploy.js --network <network>
```

## Contract

The contract is located in the `contracts` directory and is called `CrowdFunding.sol`. It contains the following functions:

### `createProject(string id, string name, string description, uint256 fundraisingGoal)`

Creates a new project with the given `id`, `name`, `description`, and `fundraisingGoal`. The `id` must be unique and cannot be changed after the project is created. The function emits a `ProjectCreated` event with the project details.

### `fundProject(uint256 projectIndex) payable`

Funds the project at the given `projectIndex` with the amount of Ether sent with the transaction. The function emits a `ProjectFunded` event with the project ID and the amount funded.

### `changeProjectState(FundraisingState newState, uint256 projectIndex)`

Changes the state of the project at the given `projectIndex` to the new state `newState`. The function emits a `ProjectStateChanged` event with the project ID and the new state.

### `getProjectCount() view returns (uint256)`

Returns the total number of projects.

### `getProjectById(string projectId) view returns (string, string, string, address, FundraisingState, uint256, uint256)`

Returns the details of the project with the given `projectId`.

## SPDX-License-Identifier

The license used for this project is the GNU General Public License v3.0 (GPL-3.0). 



