# Lovable.dev Ergo Blockchain Integration Prompt

This specialized prompt helps you generate a web application with Lovable.dev that integrates with the Ergo blockchain using Fleet SDK and Nautilus wallet.

```
I need to build a web application that integrates with the Ergo blockchain. The application should use Fleet SDK to interact with the blockchain and connect to Nautilus wallet for transaction signing.

## Application Overview

I want to create a [REPLACE WITH: type of application, e.g., "decentralized marketplace", "token swap interface", "NFT gallery", etc.] that allows users to:
- Connect their Nautilus wallet
- View their ERG balance and tokens
- [REPLACE WITH: main functionality, e.g., "swap tokens", "mint NFTs", "participate in auctions", etc.]
- Sign and submit transactions to the Ergo blockchain
- View transaction history and status

## UI Requirements

### Layout
- Clean, modern interface with a dark theme using deep blues and accent colors that complement Ergo's branding
- Responsive design that works well on both desktop and mobile
- Wallet connection button prominently displayed in the header
- Main dashboard showing balance information and available actions
- Transaction history section with filtering capabilities
- [REPLACE WITH: any additional UI sections needed]

### Components
- Wallet connection modal with clear instructions
- Balance display showing ERG and tokens with proper decimal formatting
- Asset display with token icons and information
- Transaction builder form with input validation
- Transaction confirmation modal showing details before signing
- Loading indicators and transaction status updates
- Error messages with user-friendly explanations
- [REPLACE WITH: any additional components needed]

## Functionality

### Wallet Integration
- Connect to Nautilus wallet using EIP-12 standard
- Request necessary permissions (connect, get address, get balance, sign tx)
- Handle wallet disconnection and reconnection
- Support multiple addresses if available in the wallet
- Display proper error handling if wallet extension is not installed

### Blockchain Interactions
- Use Fleet SDK for all blockchain interactions
- Fetch user balance and tokens from the blockchain
- Build transactions according to Ergo's extended UTXO model
- Send transactions to the wallet for signing
- Submit signed transactions to the blockchain
- Track transaction status and provide feedback to users

### Key Features
- [REPLACE WITH: detailed description of your application's unique features]
- Secure transaction building with proper change address handling
- Real-time transaction status updates
- Error handling with clear user feedback

## Data Model

### Key Entities
- User (connected wallet addresses)
- Assets (ERG and tokens owned by the user)
- Transactions (history of user's transactions)
- [REPLACE WITH: any additional entities specific to your application]

### Data Requirements
- Store connected wallet address in local storage for persistence
- Cache token information for better performance
- Keep transaction history for reference

## Backend Integration

### Supabase Setup (if needed)
- User authentication linking blockchain addresses
- Storage for application-specific data
- [REPLACE WITH: any additional Supabase requirements]

### API Integrations
- Connect to Ergo Explorer API for blockchain data
- Use Node API for transaction submission
- [REPLACE WITH: any additional APIs needed]

## Implementation Details

- Use React and Tailwind for the frontend
- Implement Fleet SDK (npm package) for Ergo blockchain interaction
- Follow best practices for blockchain integration security
- Handle edge cases like network issues and transaction failures
- Provide informative error messages for common blockchain issues
- Implement proper loading states during blockchain operations

Please integrate all these requirements and give me a fully functional Ergo blockchain application that offers a seamless user experience with proper error handling and clear feedback throughout the transaction process.
```

## How to Use This Prompt with Lovable.dev

1. **Copy the entire prompt**
2. **Replace all [REPLACE WITH: ...] sections** with your specific requirements
3. **Paste the completed prompt** into Lovable.dev's chat interface
4. **Iteratively refine** your application through follow-up messages

## Tips for Ergo Blockchain Integration

1. **Test Wallet Connection**: Ensure you have the Nautilus wallet extension installed to test the connection
2. **Start Simple**: Begin with basic functionality like balance checking before moving to complex transactions
3. **Address Error Handling**: Blockchain interactions often require comprehensive error handling
4. **Consider Testnet First**: Develop and test using Ergo's testnet before moving to mainnet
5. **Request Explicit Security Measures**: Ask for protection against common blockchain vulnerabilities
6. **Include Transaction Review**: Always implement a review step before transaction signing

This specialized prompt helps you create blockchain applications with Lovable.dev by providing the specific structure and requirements needed for Ergo blockchain integration. You can customize it further based on your specific use case and requirements.