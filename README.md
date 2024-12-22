# Governance DAO Smart Contract

A decentralized autonomous organization (DAO) smart contract built on Stacks blockchain for transparent and decentralized governance.

## Overview

This smart contract implements a comprehensive DAO system that enables:

- Decentralized decision-making through proposals and voting
- Member management with reputation and staking mechanisms
- Treasury management with secure fund handling
- Cross-DAO collaboration capabilities
- Reputation system with activity-based adjustments

## Features

- **Membership Management**

  - Join/leave DAO functionality
  - Token staking and unstaking
  - Reputation-based system
  - Activity tracking

- **Proposal System**

  - Create and vote on proposals
  - Automatic proposal expiration
  - Weighted voting based on reputation and stake
  - Transparent execution of approved proposals

- **Treasury Management**

  - Secure fund handling
  - Donation capabilities
  - Balance tracking
  - Controlled fund distribution

- **Reputation System**

  - Dynamic reputation scoring
  - Activity-based reputation gains
  - Inactivity decay mechanism
  - Weighted voting power

- **Cross-DAO Collaboration**
  - Propose collaborations with other DAOs
  - Accept/reject collaboration proposals
  - Track collaboration status

## Getting Started

### Prerequisites

- Stacks blockchain environment
- Clarity smart contract development tools
- STX tokens for testing and deployment

### Installation

1. Clone the repository
2. Deploy the contract to the Stacks blockchain
3. Initialize the contract

### Usage

#### Joining the DAO

```clarity
(contract-call? .governance-dao join-dao)
```

#### Creating a Proposal

```clarity
(contract-call? .governance-dao create-proposal
  "Proposal Title"
  "Proposal Description"
  u1000)
```

#### Voting on a Proposal

```clarity
(contract-call? .governance-dao vote-on-proposal u1 true)
```

#### Staking Tokens

```clarity
(contract-call? .governance-dao stake-tokens u1000)
```

## Contract Functions

### Member Management

- `join-dao`: Join the DAO as a new member
- `leave-dao`: Leave the DAO
- `stake-tokens`: Stake STX tokens
- `unstake-tokens`: Unstake previously staked tokens

### Proposal Management

- `create-proposal`: Create a new proposal
- `vote-on-proposal`: Vote on an active proposal
- `execute-proposal`: Execute an approved proposal

### Treasury Management

- `get-treasury-balance`: Get current treasury balance
- `donate-to-treasury`: Make a donation to the treasury

### Reputation System

- `get-member-reputation`: Get a member's reputation
- `decay-inactive-members`: Apply reputation decay to inactive members

### Cross-DAO Collaboration

- `propose-collaboration`: Propose collaboration with another DAO
- `accept-collaboration`: Accept a collaboration proposal

## Error Codes

- `ERR-NOT-AUTHORIZED (u100)`: Unauthorized access
- `ERR-ALREADY-MEMBER (u101)`: User is already a member
- `ERR-NOT-MEMBER (u102)`: User is not a member
- `ERR-INVALID-PROPOSAL (u103)`: Invalid proposal
- `ERR-PROPOSAL-EXPIRED (u104)`: Proposal has expired
- `ERR-ALREADY-VOTED (u105)`: Member has already voted
- `ERR-INSUFFICIENT-FUNDS (u106)`: Insufficient funds
- `ERR-INVALID-AMOUNT (u107)`: Invalid amount specified

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## Security

For security concerns, please refer to our [SECURITY.md](SECURITY.md) file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support and questions, please open an issue in the repository.
