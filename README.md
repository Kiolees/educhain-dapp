# 🎓 EduChain - Blockchain Certificate DApp

A decentralized application for issuing and verifying educational certificates on the Ethereum blockchain.

## 🚀 Features
- Issue digital certificates with student name, course name, and unique ID
- Verify certificate authenticity directly on blockchain
- Immutable and tamper-proof record keeping
- Multi-account support for institutions

## 🛠️ Tech Stack
- **Blockchain:** Ethereum (Hardhat local development network)
- **Smart Contract:** Solidity
- **Frontend:** Streamlit (Python)
- **Web3 Library:** Web3.py

## 📦 Installation & Setup

### Prerequisites
- Node.js v16+
- Python 3.8+
- npm or yarn

### Installation Steps

1. **Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/educhain-dapp.git
cd educhain-dapp
```

2. **Install Node.js dependencies**
```bash
npm install
```

3. **Set up Python environment**
```bash
python -m venv .venv
.venv\Scripts\activate  # Windows
source .venv/bin/activate  # macOS/Linux
pip install streamlit web3
```

4. **Start Hardhat local blockchain**
```bash
npx hardhat node
```
Keep this terminal running.

5. **Deploy smart contract** (in a new terminal)
```bash
npx hardhat run scripts/deploy.cjs --network localhost
```
Copy the deployed contract address.

6. **Update contract address**
Edit `educhain_app.py` line 9 with your deployed contract address:
```python
CONTRACT_ADDRESS = "0xYourContractAddressHere"
```

7. **Run the Streamlit app**
```bash
streamlit run educhain_app.py
```

## 📖 Usage

### Issue a Certificate
1. Navigate to the "📝 Issue Certificate" tab
2. Enter Certificate ID, Student Name, and Course Name
3. Click "Issue Certificate"
4. Wait for blockchain confirmation

### Verify a Certificate
1. Navigate to the "🔍 Verify Certificate" tab
2. Enter the Certificate ID
3. Click "Verify Certificate"
4. View the certificate details if it exists

## 🏗️ Project Structure
```
educhain-dapp/
├── contracts/          # Solidity smart contracts
├── scripts/            # Deployment scripts
├── educhain_app.py     # Streamlit frontend
├── hardhat.config.cjs  # Hardhat configuration
└── package.json        # Node.js dependencies
```

## 🤝 Contributing
Contributions, issues, and feature requests are welcome!

## 📄 License
MIT License

## 👨‍💻 Author
Created as a blockchain learning project

---

**Note:** This project is for educational purposes and uses a local Hardhat network. For production use, additional security measures and proper testing are required.
