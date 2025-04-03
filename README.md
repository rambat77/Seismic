# Contract Deploy & Interaction Full-Guide

# Official Docs Guide
# [Seismic DevNet Docs](https://docs.seismic.systems/appendix/devnet)

# Deploy an Encrypted Contract

## 1️⃣ Dependencies for WINDOWS & LINUX & VPS
```bash
sudo apt update && sudo apt install -y build-essential
sudo apt install cargo -y
```

## 2️⃣ Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustc --version
```

## 3️⃣ Install JQ
### Windows or VPS by WSL/Ubuntu
```bash
sudo apt install -y jq
jq --version
```

### Mac
```bash
brew install jq
```

## 4️⃣ Download Some Files
```bash
curl -L \ 
     -H "Accept: application/vnd.github.v3.raw" \ 
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```

## 5️⃣ Run sfoundryup
```bash
sfoundryup
```
### This may take some time between 5m to 60m or more

## 6️⃣ Clone Repository
```bash
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```

## 7️⃣ Deploy contract
```bash
bash script/deploy.sh
```
### A wallet is automatically created, and its details (address and faucet URL) are displayed.
### Then Get Faucet in your Address & Proceed it

🔗 [Faucet](https://faucet-2.seismicdev.net/)  
🔗 [Explorer](https://explorer-2.seismicdev.net/)

## Get your address and claim faucet tokens.

---

# Interact with an Encrypted Contract

## 1️⃣ Navigate to Home Directory
```bash
cd $HOME
```

## 2️⃣ Install Bun
```bash
curl -fsSL https://bun.sh/install | bash
```

## 3️⃣ Install Node Dependencies
```bash
cd try-devnet/packages/cli/
bun install
```

## 4️⃣ Send Transactions
```bash
bash script/transact.sh
```
### A wallet is automatically created, and its details (address and faucet URL) are displayed.
### Then Get Faucet in your Address & Proceed it

🔗 [Faucet](https://faucet-2.seismicdev.net/)  
🔗 [Explorer](https://explorer-2.seismicdev.net/)

## Get your address and claim faucet tokens.
