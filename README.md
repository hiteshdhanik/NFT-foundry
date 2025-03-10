# 🖼️ NFT Foundry 🛠️  

A Solidity-based NFT minting smart contract leveraging **ERC-721** with **Foundry** for testing and deployment. 🚀  

## ✨ Features  

✅ **Mint NFTs** – Create unique, ownable digital assets  
✅ **ERC-721 Standard** – Fully compatible with NFT marketplaces  
✅ **Secure & Efficient** – Gas-optimized smart contract design  
✅ **Tested with Foundry** – Ensuring reliability and robustness  

## 📜 Smart Contract  

The contract implements ERC-721 functionality, allowing users to mint NFTs.  

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract NFTFoundry is ERC721 {
    uint256 private _nextTokenId;
    
    constructor() ERC721("NFTFoundry", "NFTF") {}

    function mint() external {
        _safeMint(msg.sender, _nextTokenId);
        _nextTokenId++;
    }
}
```

## 🛠 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/hiteshdhanik/NFT-foundry.git
cd NFT-foundry
```

### 2️⃣ Install Foundry (if not installed)

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### 3️⃣ Build the project

```bash
forge build
```

### 4️⃣ Run tests

```bash
forge test
```

## 🚀 Deployment
Deploy the contract to a testnet or local blockchain:

```bash
forge script script/Deploy.s.sol --rpc-url <RPC_URL> --private-key <PRIVATE_KEY>
```

## 🧪 Testing
All smart contract functions are tested using Foundry’s forge. Run:

```bash
forge test
```

## 📜 License
This project is licensed under the MIT License.

## 🤝 Contributing
Feel free to open issues and PRs to improve this project! 💡
