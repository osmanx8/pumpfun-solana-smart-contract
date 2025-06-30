💊 PumpX: A Solana Smart Contract Framework
PumpX is a robust and extensible smart contract framework that empowers developers to launch tokens, create custom trading markets, and manage liquidity pools on Raydium and Meteora. Inspired by pump.fun, PumpX adds more flexibility with enhanced token authority management, user permissions, Discord notifications, and advanced features like spam filtering and CPI-powered migrations.

✨ Key Capabilities
🔖 Custom Token Creation: Launch tokens with personalized metadata including name, symbol, and image.

🔐 Authority Controls: Revoke or delegate token authorities for added security.

📈 Market Infrastructure: Seamlessly deploy token markets with integrated liquidity logic.

💧 Liquidity Pool Management: Add/remove liquidity from Raydium pools and efficiently handle SPL token burns.

📊 Live Dashboard: Monitor token stats and activity on a custom dashboard (similar to pump.fun).

🔗 Discord Alerts: Real-time trade and event notifications through Discord webhooks.

💸 Fee Collection System: Collect usage fees programmatically from contract interactions.

🚀 CPI Migration Support: Interact with Meteora and Raydium via cross-program invocation (CPI).

🧾 User Whitelisting: Grant elevated permissions to specific addresses through whitelisting.

🛡️ Anti-Spam Detection: Filter and block suspicious transactions to protect OpenBook markets.

🔬 Transaction Examples
You can review real transactions executed via this contract, including:

🔹 Global PDA Initialization

🔹 Bonding Curve Deployment

🔹 Whitelist Insertion

🔹 CPI-based Migration to Meteora

(Feel free to contact me for specific transaction hashes or deep dives.)

📞 Contact
Telegram: @BACAW

Have questions or feedback? I’m happy to chat.

☕ Support & Star
If this project helped or inspired you, please consider ⭐️ starring or forking it to show support!

🛠 Project Setup Guide
Welcome! Follow the steps below to configure your development environment and get started.

📦 Requirements
Install the following tools:

🦀 Rust

⚙️ Solana CLI

⚓ Anchor Framework

📌 Recommended Anchor version: 0.30.1

🧪 Check Tooling
Run these commands to verify your setup:

bash
Copy
Edit
rustc --version
solana --version
anchor --version

solana config get
solana config set --url devnet
🔐 Wallet Initialization
Create and fund a Solana wallet for development:

bash
Copy
Edit
solana-keygen new -o ./keys/admin.json
solana-keygen pubkey ./keys/admin.json
solana balance ./keys/admin.json
solana airdrop 5 <YOUR_PUBLIC_KEY> -u devnet
🚀 Clone & Install
bash
Copy
Edit
git clone https://github.com/your-repo/project-name.git
cd project-name
yarn install
⚙️ Build the Program
Build the smart contract with a specific Rust toolchain:

bash
Copy
Edit
RUSTUP_TOOLCHAIN=nightly-2024-11-19 anchor build
anchor keys sync
🧪 Deploy to Devnet
Ensure your Anchor.toml is set to Devnet:

toml
Copy
Edit
[provider]
cluster = "https://api.devnet.solana.com"
Deploy the contract:

bash
Copy
Edit
anchor deploy
🔧 Command-Line Scripts
You can interact with the program using predefined Yarn scripts:

🏁 Initialize Config
bash
Copy
Edit
yarn script config
🚀 Launch a Token
bash
Copy
Edit
yarn script curve
🔄 Swap Token / SOL
bash
Copy
Edit
yarn script swap -t <TOKEN_MINT> -a <AMOUNT> -s <DIRECTION>
Flag	Description
-t	Token Mint Address
-a	Amount to swap
-s	Swap direction: 0 (Buy), 1 (Sell)

📦 Migrate Token to Raydium
bash
Copy
Edit
yarn script migrate -m <TOKEN_MINT>
📚 Final Notes
This project provides a production-ready toolkit for token creation, liquidity management, and DeFi interoperability on Solana. With built-in features like Discord alerts and whitelist logic, it’s ideal for developers building next-gen dApps, token communities, or launching novel memecoins with better tooling than pump.fun.
