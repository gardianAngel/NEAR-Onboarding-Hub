
# 3. Deploy Your First Smart Contract

Deploy a simple "Hello World" smart contract to understand the deployment process.

## What You'll Learn
- Create a basic smart contract
- Deploy to NEAR testnet
- Call contract functions
- Understand gas and transaction costs

## Prerequisites
- ✅ [Development environment set up](../getting-started/setup-environment.md)
- ✅ [NEAR account created](../getting-started/create-account.md)

## Time Required
⏱️ **30 minutes**

## The 1-2-3 Launch Process

### Step 1: Create Your Contract

Create a new directory and file:
```bash
mkdir my-first-contract
cd my-first-contract
```

Create `contract.js`:
```javascript
import { NearBindgen, near, call, view } from 'near-sdk-js';

@NearBindgen({})
class HelloContract {
  message = "Hello, NEAR!";

  @view({})
  get_greeting() {
    return this.message;
  }

  @call({})
  set_greeting({ message }) {
    this.message = message;
  }
}
```

### Step 2: Build and Deploy

Build the contract:
```bash
npm run build
```

Deploy to your testnet account:
```bash
near deploy --wasmFile build/contract.wasm --accountId yourname.testnet
```

**What this does**: Uploads your contract code to the NEAR blockchain and associates it with your account.

### Step 3: Test Your Contract

Call the view function (free):
```bash
near view yourname.testnet get_greeting
```

Call the change function (costs gas):
```bash
near call yourname.testnet set_greeting '{"message": "Hello from my contract!"}' --accountId yourname.testnet
```

## Success Indicator 🎯
You should see these responses:
1. **First call**: `"Hello, NEAR!"`
2. **After setting new message**: `"Hello from my contract!"`

## Understanding Gas Costs

**Coffee Shop Analogy**: Gas fees are like tips at a coffee shop:
- **View functions** = Looking at the menu (free)
- **Change functions** = Ordering coffee (costs gas/tip)
- **Gas limit** = Maximum tip you're willing to pay

## Troubleshooting

### Common Errors

**❌ "Account not found"**
- **Solution**: Check your account name spelling
- **Or**: Ensure you're using `.testnet` suffix

**❌ "Insufficient funds"**
- **Solution**: Get testnet tokens from [NEAR Faucet](https://near-faucet.io)

**❌ "Contract deployment failed"**
- **Solution**: Check that your contract compiles without errors
- **Or**: Verify you have enough gas for deployment

## What Just Happened?

1. **You created** a smart contract with persistent storage
2. **You deployed** it to NEAR's blockchain
3. **You interacted** with it using function calls
4. **You paid gas** for state-changing operations

## Next Steps
- [Learn to interact with contracts from JavaScript](interact-with-contracts.md)
- [Handle payments in your contracts](handle-payments.md)
- [Build a frontend for your contract](../dapp-development/build-frontend.md)

## Related Resources
- [NEAR SDK Documentation](https://docs.near.org/sdk/js/)
- [Smart Contract Examples](https://github.com/near-examples)
- [Gas and Storage Guide](https://docs.near.org/concepts/gas)
```

