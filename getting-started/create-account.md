# 2. Create Your First NEAR Account

Create and fund a NEAR account for development and testing.

## What You'll Learn
- Understand NEAR account structure
- Create a testnet account
- Fund your account with test tokens
- Verify account creation

## Prerequisites
- ✅ [Development environment set up](setup-environment.md)

## Time Required
⏱️ **10 minutes** | 🟢 **Beginner**

---

## The 1-2-3 Launch Process

### Step 1: Choose Your Account Name

NEAR accounts follow specific naming rules:
- Must be lowercase
- Letters and numbers only
- For testnet: `yourname.testnet`
- For mainnet: `yourname.near`

{% hint style="info" %}
**Example**: `alice.testnet`, `bob123.testnet`, `myproject.testnet`
{% endhint %}

### Step 2: Create the Account

```bash
near create-account yourname.testnet --masterAccount yourname.testnet
```

**What this does**: Creates a new account on NEAR testnet with your chosen name.

### Step 3: Fund Your Account

Visit the [NEAR Testnet Faucet](https://near-faucet.io/) to get test tokens:

1. Enter your account name: `yourname.testnet`
2. Complete the captcha
3. Click "Request tokens"
4. Wait for confirmation

---

## Success Indicator 🎯

Your account shows a positive balance when you run:
```bash
near state yourname.testnet
```

**Expected output**:
```json
{
  "amount": "200000000000000000000000000",
  "code_hash": "11111111111111111111111111111111",
  "storage_usage": 182,
  "block_height": 12345678,
  "block_hash": "ABC123..."
}
```

---

## Understanding Your NEAR Account

When you create a NEAR account, these are the key details to understand:

{% tabs %}
{% tab title="Account ID" %}
**yourname.testnet**

- Unique identifier on NEAR  
- Cannot be changed once created  
- Used for all transactions  
{% endtab %}

{% tab title="Balance" %}
**NEAR Tokens**

- Amount shown in yoctoNEAR (smallest unit)  
- 1 NEAR = 10^24 yoctoNEAR  
- Used for gas fees and storage  
{% endtab %}

{% tab title="Storage" %}
**Storage Usage**

- Measured in bytes  
- Costs NEAR tokens to maintain  
- Includes account data and contracts  
{% endtab %}
{% endtabs %}

---

## Coffee Shop Analogy ☕

Think of your NEAR account like a coffee shop loyalty card:
- **Account ID** = Your name on the card
- **Balance** = Credit amount on the card
- **Storage** = Personal preferences stored on the card
- **Testnet** = Practice coffee shop where drinks are free

---

## Troubleshooting

### Common Issues

**❌ "Account already exists"**
- **Solution**: Choose a different account name
- **Or**: Use an existing account you created before

**❌ "Invalid account ID"**
- **Solution**: Check naming rules (lowercase, alphanumeric only)
- **Example**: `my-account.testnet` ❌ → `myaccount.testnet` ✅

**❌ "Faucet not working"**
- **Solution**: Try again after a few minutes
- **Or**: Ask for tokens in [NEAR Discord](https://discord.gg/near)

---

## What You Just Accomplished

✅ **Created a NEAR account** - Your identity on the blockchain  
✅ **Funded with test tokens** - Ready for transactions  
✅ **Verified account status** - Everything is working  

---

## Next Steps

Now that you have a funded account:
- [Deploy your first smart contract](../smart-contracts/deploy-first-contract.md)
- [Learn about interacting with contracts](../smart-contracts/interact-with-contracts.md)
- [Check the quick reference guide](quick-reference.md)

## Related Resources

- [NEAR Account Model](https://docs.near.org/concepts/account-model)
- [NEAR Testnet Explorer](https://testnet.nearblocks.io/)
- [Account Management Guide](https://docs.near.org/concepts/account-model)

---

{% hint style="warning" %}
**Important**: Testnet accounts and tokens have no real value. They're only for development and testing!
{% endhint %}
```

---
