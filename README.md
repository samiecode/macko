# **Macko \- The Decentralized Marketplace**

Macko is a web3 e-commerce platform designed to function as a decentralized marketplace, similar to Jumia or Jiji. It empowers buyers and sellers to transact directly in a secure, transparent, and peer-to-peer environment powered by smart contracts.

## **🌟 Core Features**

### **🛒 For Buyers**

* **Discover & Browse**: Explore a wide range of products across various categories in a decentralized ecosystem.  
* **Secure Payments**: Purchase goods using cryptocurrency with funds held in a transparent smart contract escrow until the transaction is complete.  
* **Order Tracking**: Monitor your purchase status from payment to delivery confirmation.  
* **Dispute Resolution**: Access a built-in mechanism to handle disputes fairly and on-chain.  
* **ENS Profiles**: View seller profiles using human-readable ENS names for better trust.

### **💼 For Sellers**

* **Decentralized Storefronts**: Set up a personalized storefront tied directly to your wallet address.  
* **Easy Product Listing**: List physical or digital products for sale, with support for image hosting on IPFS.  
* **Inventory Management**: Track and update product availability in real-time.  
* **Order Dashboard**: View and process incoming orders through a dedicated seller interface.  
* **Direct & Secure Payouts**: Receive funds automatically to your wallet via the escrow system upon successful order completion.

### **🤖 Platform & Smart Contracts**

* **Marketplace Core**: A central smart contract governs listings, sales, and user interactions.  
* **Automated Escrow**: Manages transaction funds, releasing them only when both parties are satisfied.  
* **Wallet Integration**: Seamless connectivity with popular Web3 wallets (e.g., MetaMask) via Wagmi.  
* **Multi-chain Ready**: Designed with an architecture that can be deployed on various EVM-compatible blockchains.

## **🚀 Tech Stack**

* **Frontend**: Next.js 14 \+ React 18 \+ TypeScript  
* **Styling**: Tailwind CSS with shadcn/ui & Radix UI  
* **Web3 Interaction**: Wagmi \+ Viem  
* **Decentralized Storage**: IPFS with Pinata for product assets  
* **Smart Contracts**: Solidity  
* **Contract Development**: Hardhat / Foundry  
* **State Management**: TanStack React Query  
* **UI Animation**: Framer Motion

## **🛠️ Getting Started with Development**

### **Prerequisites**

* Node.js 18+  
* npm or yarn  
* A Web3 wallet browser extension (e.g., MetaMask)  
* A Pinata account for IPFS hosting (optional)

### **Installation & Setup**

1. **Clone the repository:**  
   git clone \[https://github.com/samieazubike/macko.git\](https://github.com/samieazubike/macko.git)  
   cd macko

2. **Install dependencies:**  
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   # or
   bun install
   ```

3. Configure your environment:  
   Copy the example environment file to create your local configuration.  
   cp .env.example .env.local

   Now, open .env.local and add your configuration details:  
   \# Add your Alchemy or Infura API key for connecting to the blockchain  
   NEXT\_PUBLIC\_ALCHEMY\_ID="YOUR\_ALCHEMY\_API\_KEY"

   \# Add your wallet's private key for deploying/testing contracts  
   PRIVATE\_KEY="YOUR\_WALLET\_PRIVATE\_KEY\_FOR\_DEPLOYMENT"

   \# Set the network configuration for the frontend  
   \# Use 'true' for a testnet like Polygon Amoy  
   NEXT\_PUBLIC\_USE\_TESTNET=true

   \# Use 'false' for Polygon Mainnet (production)  
   NEXT\_PUBLIC\_USE\_TESTNET=false

4. **Run the development server:**  
   npm run dev

   The application will be available at http://localhost:3000.

### **Available Scripts**

* npm run dev: Starts the Next.js development server.  
* npm run build: Builds the application for production.  
* npm run start: Starts a production server.  
* npm run lint: Lints the codebase for errors.  
* npx hardhat compile: Compiles the smart contracts.  
* npx hardhat test: Runs smart contract tests.  
* npx hardhat deploy \--network amoy: Deploys contracts to the Amoy testnet.

## **🏗️ Architecture & Network Details**

This project is configured to run on Polygon Mainnet and its Amoy testnet. The network is controlled by the NEXT\_PUBLIC\_USE\_TESTNET environment variable.

<!-- #### **Polygon Mainnet (Production)**

* **Chain ID**: 137  
* **RPC**: https://polygon-mainnet.g.alchemy.com/v2/YOUR\_ALCHEMY\_API\_KEY  
* **USDC Address**: 0x3c499c542cEF5E3811e1192ce70d8cC03d5c3359 (6 decimals)  
* **Macko Marketplace Contract**: TBD (to be deployed)

#### **Polygon Amoy (Testnet)**

* **Chain ID**: 80002  
* **RPC**: https://polygon-amoy.g.alchemy.com/v2/YOUR\_ALCHEMY\_API\_KEY  
* **USDC Address**: 0x41e94Eb019C0762f9BFC4545e372899135362409 (6 decimals)  
* **Macko Marketplace Contract**: TBD (to be deployed) -->

## **🔐 Security & Deployment**

### **Security Features**

* **Smart Contract Auditing**: It is highly recommended that all contracts are audited by a reputable third party before mainnet deployment.  
* **Reentrancy Protection**: Follows the Checks-Effects-Interactions pattern.  
* **Secure Escrow**: Protects both buyers and sellers by ensuring funds are released only upon mutual agreement.  
* **Non-Custodial**: Users always maintain control of their funds and private keys via their own wallets.

### **Deployment Checklist**

* \[ \] Run a full security audit on all smart contracts.  
* \[ \] Deploy contracts to the Polygon Mainnet.  
* \[ \] Update mainnet contract addresses in the frontend configuration.  
* \[ \] Set NEXT\_PUBLIC\_USE\_TESTNET=false in your production environment variables.  
* \[ \] Ensure all RPC endpoints and API keys are set for mainnet.  
* \[ \] Thoroughly test all user flows (listing, buying, dispute resolution) on a public testnet.  
* \[ \] Set up a custom domain and configure your hosting provider (Vercel is recommended).