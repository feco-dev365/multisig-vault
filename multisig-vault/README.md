# multisig Vault Smart Contract

## Overview

The Multisig Vault is a Clarity smart contract designed for the Stacks blockchain. It implements a simple multi-signature vault that allows designated members to vote on who should receive the STX (Stacks tokens) contents of the vault. This contract provides a secure way to manage shared funds, requiring consensus among members before any withdrawal can occur.

## Features

1. **Member Management**: The contract owner can set up a list of members who have voting rights.
2. **Configurable Voting Threshold**: The number of votes required for a successful withdrawal can be set during initialization.
3. **Voting Mechanism**: Members can vote on potential recipients of the vault's contents.
4. **Secure Withdrawals**: Funds can only be withdrawn when the required number of votes is met.
5. **Deposit Functionality**: Anyone can deposit STX into the vault.
6. **Vote Tallying**: The contract provides a function to tally votes for a specific recipient.

## Smart Contract Functions

### Public Functions

1. `start`: Initializes the vault with a list of members and the required number of votes.
2. `vote`: Allows a member to cast a vote for a recipient.
3. `withdraw`: Attempts to withdraw the vault's contents to the caller if enough votes are met.
4. `deposit`: Allows anyone to deposit STX into the vault.

### Read-Only Functions

1. `get-vote`: Retrieves the vote of a specific member for a specific recipient.
2. `tally-votes`: Counts the total number of votes for the transaction sender.

## Setup

1. Ensure you have the Clarity CLI installed.
2. Deploy the contract to the Stacks blockchain: