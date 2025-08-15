# Liquid Staking Program - Project Index

## Project Overview
**Liquid Staking** is a liquid staking program for the Solana blockchain built using the Anchor framework. This project allows users to stake SOL tokens and receive liquid staking derivatives (mSOL) in return.

## Project Structure

### Root Directory
```
├── .git/                    # Git repository
├── scripts/                 # Build and deployment scripts
├── programs/                # Solana program source code
├── README.md               # Project documentation
├── LICENSE.md              # License information
├── Cargo.toml             # Rust workspace configuration
├── Cargo.lock             # Dependency lock file
├── Anchor.toml            # Anchor framework configuration
└── .gitignore             # Git ignore rules
```

### Core Program Structure (`programs/marinade-finance/`)
```
├── src/
│   ├── lib.rs              # Main program entry point and instruction definitions
│   ├── error.rs            # Custom error types and error handling
│   ├── checks.rs           # Validation and security checks
│   ├── calc.rs             # Mathematical calculations and formulas
│   ├── state/              # Program state structures and data models
│   ├── instructions/       # Program instruction implementations
│   └── events/             # Event definitions and logging
├── Cargo.toml              # Program-specific dependencies
└── Xargo.toml              # Cross-compilation configuration
```

## Key Components

### 1. Program Entry Point (`lib.rs`)
- **Program ID**: `MarBmsSgKXdrN1egZf5sqe1TMai9K1rChYNDJgjq7aD`
- **Security**: Implements security.txt for transparency
- **Instructions**: Defines all program instructions and their handlers

#### Core Instructions
- **Initialization**: `initialize`, `change_authority`
- **Validator Management**: `add_validator`, `remove_validator`, `set_validator_score`
- **User Operations**: Liquid staking and unstaking
- **Liquidity Pool**: Add/remove liquidity operations
- **Admin Functions**: Configuration and management operations

### 2. State Management (`state/`)
- **`mod.rs`**: Main state structures and program state
- **`validator_system.rs`**: Validator list and scoring system
- **`stake_system.rs`**: Staking mechanics and state
- **`liq_pool.rs`**: Liquidity pool management
- **`fee.rs`**: Fee calculation and management
- **`list.rs`**: Generic list data structures
- **`delayed_unstake_ticket.rs`**: Delayed unstaking ticket system

### 3. Instructions (`instructions/`)
- **`admin/`**: Administrative operations
- **`crank/`**: Automated processing operations
- **`delayed_unstake/`**: Delayed unstaking functionality
- **`liq_pool/`**: Liquidity pool operations
- **`management/`**: Program management functions
- **`user/`**: User-facing operations

### 4. Events (`events/`)
- **`user.rs`**: User operation events
- **`admin.rs`**: Administrative events
- **`crank.rs`**: Automated processing events
- **`liq_pool.rs`**: Liquidity pool events
- **`delayed_unstake.rs`**: Delayed unstaking events
- **`management.rs`**: Management operation events

### 5. Utilities
- **`error.rs`**: Comprehensive error handling with custom error types
- **`checks.rs`**: Security validations and account checks
- **`calc.rs`**: Mathematical calculations for staking rewards and fees

## Build Configuration

### Rust Configuration (`Cargo.toml`)
- **Workspace**: Multi-crate project structure
- **Release Profile**: Optimized for production with overflow checks
- **Dependencies**: Anchor v0.29.0, Solana SPL token programs

### Anchor Configuration (`Anchor.toml`)
- **Toolchain**: Anchor v0.29.0, Solana v1.17.0
- **Program ID**: Configured for localnet deployment
- **Features**: Seeds and linting enabled
- **Provider**: Mainnet cluster configuration

## Scripts (`scripts/`)
- **`verify.sh`**: Program verification script
- **`verify-buffer.sh`**: Buffer verification script
- **`prepare-upgrade.sh`**: Upgrade preparation script

## Security Features
- **Audits**: Multiple security audits from Neodyme, Sec3, Kudelski Security, and Ackee Blockchain
- **Security.txt**: Transparent security contact information
- **Overflow Protection**: Runtime overflow checks enabled
- **Account Validation**: Comprehensive account validation and security checks

## Dependencies
- **Anchor Lang**: v0.29.0 - Solana program framework
- **Anchor SPL**: v0.29.0 - SPL token program integration
- **Solana Security TXT**: v1.1.1 - Security transparency

## Development Notes
- **Integration Tests**: Not included in this repository (to be published later)


## Key Features
1. **Liquid Staking**: Convert SOL to mSOL for immediate liquidity
2. **Validator Management**: Dynamic validator list with scoring system
3. **Liquidity Pool**: Automated market making for mSOL/SOL pairs
4. **Delayed Unstaking**: Option for delayed SOL withdrawal
5. **Fee Management**: Configurable fee structure for sustainability
6. **Automated Operations**: Crank system for automated processing

Liquid Staking represents a sophisticated DeFi protocol for liquid staking on Solana, providing users with the benefits of staking while maintaining liquidity through derivative tokens.
