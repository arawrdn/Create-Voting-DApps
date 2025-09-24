# Base Voting dApp

This repository contains a **simple voting smart contract** that can be deployed on the **Base Network** using Remix IDE. Users can vote for candidates, and each wallet is allowed to vote once.  

---

## 1. Open Remix IDE

- Go to [https://remix.ethereum.org](https://remix.ethereum.org)  
- Connect your wallet (e.g., MetaMask) to the Base network (Testnet or Mainnet).

---

## 2. Create Contract File

- In Remix, create a new file:  
  `contracts/Voting.sol`  
- Paste the smart contract code from `Voting.sol` into the file.

---

## 3. Compile Contract

- Select Solidity compiler version: **0.8.20**  
- Enable optimization (optional)  
- Click **Compile Voting.sol**  

> Ensure there are no compilation errors.

---

## 4. Deploy Contract

- Environment: **Injected Web3**  
- Network: Base Testnet/Mainnet  
- Constructor parameter: Array of candidate names, e.g.:  
  ```solidity
  ["Alice", "Bob", "Charlie"]
  ```  
- Click **Deploy** and confirm the transaction in your wallet.

---

## 5. Interact with Contract

- Open the **Deployed Contracts** section in Remix:  

### Voting
- `vote(candidateId)` → Cast your vote for a candidate.  
  - `candidateId` starts from 0.  
  - Example: `0` for Alice, `1` for Bob, etc.  

### View Results
- `getCandidate(candidateId)` → Check the candidate's name and vote count.  

---

## Notes

- Each wallet can vote **only once**.  
- This is a **simple educational example** for testing and learning.  
- For production usage, consider:  
  - Adding voting periods  
  - Token-weighted voting  
  - Security audits  
