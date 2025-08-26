# Token Information Repository

This repository is used to store detailed information about ERC20 tokens on various blockchain networks.

## Project Structure

```
tokens/
├── {chainId}/                    # Blockchain network ID directory
│   ├── {tokenAddress}.json       # JSON file named after token address
│   └── ...
└── README.md
```

## How to Add ERC20 Token Information

### 1. Determine Chain ID
First, determine the blockchain network ID where your ERC20 token is located. Common Chain IDs include:
- `1` - Ethereum Mainnet
- `56` - BSC (Binance Smart Chain)
- `137` - Polygon
- `42161` - Arbitrum One
- `10` - Optimism
- `8453` - Base
- `1301` - Example Network

### 2. Create or Find the Corresponding Chain ID Directory
If the directory for that Chain ID doesn't exist, create it:
```bash
mkdir -p {chainId}
```

### 3. Create Token JSON File
In the corresponding Chain ID directory, create a JSON file named after the ERC20 token contract address.

**File naming format:** `{tokenAddress}.json`

**Example:** `0x5bef4d0fa28542bd0e0eb996efd65785dc388a8e.json`

### 4. JSON File Format
Each ERC20 token's JSON file should contain the following fields:

```json
{
    "name": "Token Name",
    "symbol": "Token Symbol",
    "description": "Token description information",
    "decimals": 18,
    "image": "Token icon URL",
    "website": "Official website URL",
    "twitter": "Twitter link",
    "telegram": "Telegram link",
    "discord": "Discord link",
    "github": "GitHub link"
}
```

**Required fields:**
- `name`: Complete name of the ERC20 token
- `symbol`: Token symbol (usually 3-5 characters)
- `description`: Detailed description of the token
- `decimals`: Number of decimal places for the token (typically 18 for ERC20 tokens)

**Optional fields:**
- `image`: URL address of the token icon
- `website`: Project's official website
- `twitter`: Twitter social media link
- `telegram`: Telegram group link
- `discord`: Discord server link
- `github`: GitHub repository link

### 5. Example

**File path:** `1301/0x5bef4d0fa28542bd0e0eb996efd65785dc388a8e.json`

**File content:**
```json
{
    "name": "Sample Token",
    "symbol": "SMPL",
    "description": "Sample ERC20 token for demonstration purposes. This is a fungible token that follows the ERC20 standard.",
    "decimals": 18,
    "image": "https://ipfs.io/ipfs/QmUu3GsdBg2G7bZHyj8Y9aR7n7M9Ya3N76XbnkVeK4xUYd",
    "website": "https://example.com",
    "twitter": "https://twitter.com/example",
    "telegram": "https://t.me/example",
    "discord": "https://discord.gg/example",
    "github": "https://github.com/example"
}
```

## ERC20 Token Standards

This repository focuses on ERC20 tokens, which are fungible tokens that follow the Ethereum Request for Comment 20 standard. Key characteristics:

- **Fungible**: Each token is identical and interchangeable
- **Divisible**: Tokens can be divided into smaller units (specified by decimals)
- **Standard Interface**: All ERC20 tokens implement the same basic functions
- **Common Decimals**: Most ERC20 tokens use 18 decimal places

## Important Notes

1. **File names must use lowercase letters**: Token addresses should be converted to lowercase
2. **JSON format validation**: Ensure the JSON file format is correct, you can use online JSON validation tools
3. **Address accuracy**: Ensure you use the correct ERC20 token contract address
4. **Information accuracy**: Ensure the provided token information is accurate and up-to-date
5. **Decimals field**: Most ERC20 tokens use 18 decimals, but some may use different values (e.g., 6 for USDC, 8 for WBTC)

## Contributing Guidelines

1. Fork this repository
2. Add ERC20 token information according to the format above
3. Submit a Pull Request
4. Wait for review and merge

## Supported Blockchain Networks

- Ethereum Mainnet (Chain ID: 1)
- BSC (Chain ID: 56)
- Polygon (Chain ID: 137)
- Arbitrum One (Chain ID: 42161)
- Optimism (Chain ID: 10)
- Base (Chain ID: 8453)
- Other networks...

If you need to add support for new blockchain networks, please suggest it in the Issues section.
