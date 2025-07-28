# Octra-Labs
A guide to Interacting with Octra Labs Public testnet
## Dependencies
Install & Update Packages:
```
sudo apt update && sudo apt upgrade -y
sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```
Install Bun (if not installed yet):
```
curl -fsSL https://bun.sh/install | bash
```
Add Bun to your shell environment:
```
source ~/.bashrc  # or ~/.zshrc if using zsh
```
Verify it works:
```
bun --version
```
## Wallet generation
Clone the repo and navigate into it:
```
git clone https://github.com/octra-labs/wallet-gen.git
cd wallet-gen
```
Make the web wallet script executable and start it:
```
chmod +x ./start.sh
./start.sh
```
This starts a local web server at:
```
http://localhost:8888
```
Open that in your browser.

In your browser, you’ll now be able to:

-Generate a wallet

-See your mnemonic phrase and address

-Download the wallet data  (Make sure do download and keep wallet details somewhere safe)

Request faucet for transactions: https://faucet.octra.network/

## Pre-Client
Make sure you're in your root directory:
```
cd
```
Install python:
```
sudo apt install python3 python3-pip python3-venv python3-dev -y
```

Install CLI
```
git clone https://github.com/octra-labs/octra_pre_client.git
cd octra_pre_client

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

cp wallet.json.example wallet.json
```
Open and edit wallet.json to replace Private key and Octra address with previously saved details
```
nano wallet.json
```
After editing; ctrl + X then Y then Enter to save

Run
```
./run.sh       # on linux/mac
run.bat        # on windows
```

An Interface will display where you can view your balance, send and receive transactions as well as Interact with the Octra labs public testnet in other ways.

## Credits
Original project https://github.com/octra-labs




