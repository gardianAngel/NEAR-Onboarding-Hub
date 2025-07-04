## 📄 getting-started/setup-environment.md
```markdown
# 1. Set Up Your Development Environment

Set up everything you need to start building on NEAR Protocol in under 15 minutes.

## What You'll Learn
- Install NEAR CLI
- Configure your development environment
- Verify everything works correctly

## Prerequisites
- Basic familiarity with command line
- Node.js installed on your computer

## Time Required
⏱️ **15 minutes**

## The 1-2-3 Launch Process

### Step 1: Install NEAR CLI
```

```bash
npm install -g near-cli
```

**What this does**: Installs the NEAR command-line interface globally on your system.

### Step 2: Verify Installation
```bash
near --version
```

**Expected output**: You should see a version number like `4.0.13`

### Step 3: Set Up Your Development Network
```bash
near login
```

**What happens**: This opens your web browser to connect NEAR CLI to your wallet.

## Success Indicator 🎯
Run this command to verify everything is working:
```bash
near state
```

If you see network information, you're ready to go!

## Troubleshooting

### Common Issues

**❌ "Permission denied" error**
- **Solution**: Use `sudo npm install -g near-cli` on Mac/Linux
- **Or**: Run Command Prompt as Administrator on Windows

**❌ "near: command not found"**
- **Solution**: Restart your terminal after installation
- **Or**: Check if Node.js is properly installed

**❌ Browser doesn't open for login**
- **Solution**: Copy the URL from terminal and paste in browser manually

## Coffee Shop Analogy ☕
Think of NEAR CLI like a loyalty card app for your favorite coffee shop. Once you install it (download the app) and log in (register your card), you can interact with the coffee shop (NEAR network) from anywhere.

## Next Steps
- [Create your first NEAR account](create-account.md)
- [Quick reference guide](quick-reference.md)

## Related Resources
- [NEAR CLI Documentation](https://docs.near.org/tools/near-cli)
- [Node.js Installation Guide](https://nodejs.org/)
```

