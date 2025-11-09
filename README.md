Blockchain-Based Document Verification System
A secure decentralized application (DApp) that verifies document authenticity using Blockchain, IPFS, MetaMask, and Web3.js.
The system stores document hashes on the blockchain and uploads actual files to IPFS, enabling tamper-proof document verification.

Features
1. Blockchain-Based Document Verification
Computes Keccak256/SHA3 hash from uploaded documents
Stores the hash on a Solidity smart contract
Prevents document tampering or duplication

2. IPFS Integration (Local Kubo Node)
Files are uploaded to a local IPFS Kubo daemon
Generates a decentralized CID for each file
Files can be accessed through any public IPFS gateway

3. Exporter Management
Smart contract includes modules to:
Add Exporter
Edit Exporter
Delete Exporter

Verify Exporter Information

 4. Document Verification

Users can:

Upload a document to check if it matches the blockchain hash

Verify via QR code link

Fetch timestamp, block number, and IPFS CID

🔗 5. Web3 + MetaMask Integration

Connect wallet

Send transactions

View transaction info

Works on Ganache local blockchain

🖥 6. Simple & Clean Frontend

HTML, CSS, JavaScript

Fully responsive

Real-time feedback for transactions

🛠️ Tech Stack
Component	Technology
Smart Contract	Solidity
Blockchain	Ganache (Local Ethereum Testnet)
Wallet	MetaMask
Storage	IPFS (Local Kubo Node)
Frontend	HTML, CSS, JavaScript
Libraries	Web3.js, QRCode.js, FileReader API
📐 System Architecture

1. User uploads a file → Frontend
2. Frontend generates SHA3 hash → Web3.js
3. File uploaded to IPFS → CID generated
4. Hash + CID stored on Blockchain → Smart Contract
5. User verifies later by SHA3 hashing again
6. If hashes match → Document is authentic ✅

📦 Folder Structure
📁 project-folder  
│── 📁 contracts/        → Solidity smart contract  
│── 📁 src/              → Frontend HTML, CSS, JS files  
│── 📁 build/            → Compiled ABI + contract JSON  
│── README.md            → Project Documentation  
│── package.json         → Dependencies  

✅ Smart Contract Functionalities
🗂 Document Functions

addDocHash(bytes32 hash, string memory ipfsCID)

findDocHash(bytes32 hash)

deleteHash(bytes32 hash)

👨‍💼 Exporter Functions

add_Exporter(address, info)

alter_Exporter(address, info)

delete_Exporter(address)

getExporterInfo(address)

⚙ How to Run Locally
✅ 1. Start Ganache

Create a new workspace

Import RPC URL: http://127.0.0.1:7545

✅ 2. Start IPFS Local Node
ipfs daemon

✅ 3. Deploy Smart Contract

Use Remix or Truffle to deploy on Ganache.
Copy the contract address into your config.js.

✅ 4. Start the Frontend

Simply open:

index.html


in your browser.

Connect MetaMask → Choose Ganache Network → Done ✅

✅ How Verification Works

1️⃣ User uploads a file
2️⃣ Frontend generates Keccak256 hash
3️⃣ Smart contract checks if hash exists
4️⃣ If found → Shows

Block number

Timestamp

Exporter

IPFS File

QR Code for sharing

🎯 Use Cases

Academic Certificate Verification

Export/Import Document Authentication

Legal Contract Validation

NGO & Government Records

Medical Report Verification

📸 Screenshots

(Add screenshots of your UI here once uploaded)

🔮 Future Scope

File-level encryption

UI/UX improvements

Multi-file upload

Global IPFS pinning

Deploy contract on Polygon Testnet

✅ Conclusion

This project provides a secure, decentralized, and tamper-proof method for document verification using the power of Blockchain + IPFS.
It is fast, efficient, transparent, and eliminates trust issues between exporters, institutions, and authorities.
