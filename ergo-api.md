# Ergo Blockchain API Guide for Cursor

This guide provides information about the Ergo blockchain API endpoints and recommended documentation resources to add to Cursor for your development.

## Ergo API Overview

The Ergo blockchain ecosystem provides several API endpoints for different purposes:

1. **Node API** - Core blockchain functionality
2. **Explorer API** - Blockchain data exploration
3. **Fleet SDK** - JavaScript/TypeScript SDK for Ergo transactions

## Key API Endpoints

### Explorer API v1

The primary API for blockchain data exploration is available at:
```
https://api.ergoplatform.com/api/v1/
```

This API allows you to query information about:
- Blocks
- Transactions
- Addresses
- Assets
- Network statistics

The complete API documentation can be accessed at:
```
https://api.ergoplatform.com/api/v1/docs/
```

### Node API

For direct interaction with the Ergo blockchain node:
```
https://node.ergoplatform.com/
```

## Documentation Resources for Cursor

Adding these resources to Cursor will enhance your development experience. Here's how to add them and when to use each resource:

### 1. Fleet SDK Documentation

**URL to add in Cursor:** 
```
https://fleet-sdk.github.io/docs/
```

**When to use:**
- When working with transaction building
- For wallet integration
- When implementing payment functionality
- For UTXO management

**Key subpages:**
- Getting Started: https://fleet-sdk.github.io/docs/getting-started
- Wallet Interaction: https://fleet-sdk.github.io/docs/wallet-interaction
- Transaction Building: https://fleet-sdk.github.io/docs/transaction-building

### 2. Ergo Platform Documentation

**URL to add in Cursor:**
```
https://docs.ergoplatform.com/
```

**When to use:**
- For understanding core Ergo concepts
- For API usage guides
- For integration best practices

**Key subpages:**
- API Documentation: https://docs.ergoplatform.com/dev/stack/api/
- Stack Documentation: https://docs.ergoplatform.com/dev/stack/

### 3. Ergo Explorer API Documentation

**URL to add in Cursor:**
```
https://api.ergoplatform.com/api/v1/docs/
```

**When to use:**
- When querying blockchain data
- When tracking transactions
- When retrieving address information
- When working with assets/tokens

### 4. Nautilus Wallet Documentation

**URL to add in Cursor:**
```
https://docs.ergoplatform.com/eco/nautilus/
```

**When to use:**
- When implementing wallet connections
- For dApp connector integration
- For transaction signing

## How to Add Documentation to Cursor

1. Open Cursor
2. In any AI input (Chat, Cmd+K, or Composer), type `@Docs`
3. Select `> Add new doc`
4. Enter one of the URLs listed above
5. Add a trailing slash to index all subpages (e.g., `https://fleet-sdk.github.io/docs/`)
6. Cursor will crawl and index the documentation
7. Manage your documentation in Cursor Settings > Features > Docs

## Example Integration Patterns

### 1. Querying Address Information

When implementing address balance checking:

```
@Docs Fleet SDK getting-started

Help me implement a function to check an address balance using the Fleet SDK and Explorer API.
```

### 2. Creating a Payment Transaction

When implementing payment functionality:

```
@Docs Fleet SDK wallet-interaction

Based on this documentation, help me create a transaction that sends 1 ERG to another address using Nautilus wallet.
```

### 3. Working with Smart Contracts

When implementing smart contract interactions:

```
@Docs Ergo Platform smart contracts

Help me understand how to interact with an existing smart contract on the Ergo blockchain using Fleet SDK.
```

## Common API Endpoints Reference

Here are some commonly used endpoints from the Explorer API:

### Address Information
```
GET /api/v1/addresses/{address}
```

### Address Transactions
```
GET /api/v1/addresses/{address}/transactions
```

### Address Balance
```
GET /api/v1/addresses/{address}/balance
```

### Transaction Information
```
GET /api/v1/transactions/{id}
```

### Unspent Boxes (UTXOs)
```
GET /api/v1/boxes/unspent/byAddress/{address}
```

### Submit Transaction
```
POST /api/v1/mempool/transactions/submit
```

## Best Practices

1. **Always use Fleet SDK for transaction building** rather than constructing transactions manually
2. **Keep documentation up-to-date** by periodically refreshing your Cursor documentation sources
3. **Reference specific documentation sections** when asking for help with implementation
4. **Combine multiple documentation sources** for comprehensive context when working on complex features

By adding these documentation resources to Cursor and following the provided guidelines, you'll be well-equipped to build applications that integrate with the Ergo blockchain effectively.
