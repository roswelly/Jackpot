# Liquid Staking Program

A sophisticated liquid staking program for the Solana blockchain built using the Anchor framework. This project allows users to stake SOL tokens and receive liquid staking derivatives (mSOL) in return, providing immediate liquidity while earning staking rewards.

## Contact

-[telegram](https://t.me/roswellecho)
-[twitter](https://x.com/roswellecho)

## Features

- **Liquid Staking**: Convert SOL to mSOL for immediate liquidity
- **Validator Management**: Dynamic validator list with scoring system
- **Liquidity Pool**: Automated market making for mSOL/SOL pairs
- **Delayed Unstaking**: Option for delayed SOL withdrawal
- **Fee Management**: Configurable fee structure for sustainability
- **Automated Operations**: Crank system for automated processing

## Project Structure

```
├── programs/marinade-finance/    # Main Solana program
│   ├── src/
│   │   ├── lib.rs               # Program entry point and instructions
│   │   ├── state/               # Program state structures
│   │   ├── instructions/        # Instruction implementations
│   │   ├── events/              # Event definitions
│   │   ├── error.rs             # Custom error types
│   │   ├── checks.rs            # Security validations
│   │   └── calc.rs              # Mathematical calculations
│   └── Cargo.toml               # Program dependencies
├── scripts/                      # Build and deployment scripts
├── Cargo.toml                    # Workspace configuration
└── Anchor.toml                   # Anchor framework configuration
```

## Prerequisites

- [Rust](https://rustup.rs/) (v1.75.0 or later)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools) (v1.17.0 or later)
- [Anchor CLI](https://book.anchor-lang.com/getting_started/installation.html) (v0.29.0 or later)

## Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```

2. **Install dependencies**
   ```bash
   cargo build
   ```

3. **Build the program**
   ```bash
   anchor build
   ```

4. **Run tests** (when available)
   ```bash
   anchor test
   ```

## Development

### Building
```bash
# Build the program
anchor build

# Build with specific features
cargo build --release
```

### Testing
```bash
# Run tests (when integration tests are available)
anchor test

# Run specific test
anchor test <test-name>
```

### Deployment
```bash
# Deploy to localnet
anchor deploy

# Deploy to devnet
anchor deploy --provider.cluster devnet

# Deploy to mainnet
anchor deploy --provider.cluster mainnet
```

## Configuration

### Anchor.toml
- **Toolchain**: Anchor v0.29.0, Solana v1.17.0
- **Features**: Seeds and linting enabled
- **Provider**: Mainnet cluster configuration

### Cargo.toml
- **Workspace**: Multi-crate project structure
- **Release Profile**: Optimized for production with overflow checks
- **Dependencies**: Anchor v0.29.0, Solana SPL token programs

## Security

- **Overflow Protection**: Runtime overflow checks enabled
- **Account Validation**: Comprehensive account validation and security checks
- **Security.txt**: Transparent security contact information
- **Audits**: Multiple security audits from reputable firms

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the terms specified in the [LICENSE.md](LICENSE.md) file.

## Support

- **Documentation**: [Project Index](PROJECT_INDEX.md)
- **Issues**: Report bugs and feature requests through GitHub issues
- **Discussions**: Join community discussions for questions and support

## Integration Testing

**Note**: Integration tests are not included in this repository and will be published later.

---

