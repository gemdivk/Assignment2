# AI Model Marketplace

## Objective
We create a decentralized application (dApp) that allows users to list, purchase, and rate AI models. The core functionality is managed by a smart contract, while the frontend provides an intuitive interface for users to interact with the blockchain.

---

## Overview
The AI Model Marketplace is a decentralized platform where users can securely:
- **List AI Models**: Creators can upload details about their AI models, set prices, and make them available for purchase.
- **Purchase AI Models**: Users can buy AI models using Ethereum, with payments going directly to the creators.
- **Rate AI Models**: Users who purchase models can rate them, contributing to their overall reputation.
- **View Model Details**: Users can access comprehensive details about each listed model.
- **Withdraw Funds**: Model creators can withdraw accumulated earnings securely.

---

## Features
### Blockchain Features
- **Smart Contract**: Built in Solidity, the contract manages listing, purchasing, rating, and fund withdrawals.
- **Web3.js Integration**: Facilitates secure blockchain interactions.
- **MetaMask Support**: Ensures safe transaction handling.

### Frontend Features
- **Dynamic Interface**: User-friendly design with a clean UI/UX.
- **Interactive Forms**:
  - Add Model: Submit model details.
  - Rate Model: Provide feedback for purchased models.
- **Grid/List Views**:
  - Browse available models.
  - Access model-specific details.
- **Secure Transactions**: Purchase AI models via MetaMask.
- **Live Updates**: Dynamic rendering of model details and ratings.

---

## Smart Contract Functions
### `listModel(string memory name, string memory description, uint256 price)`
- **Purpose**: Allows users to add a new AI model to the marketplace.
- **Parameters**:
  - `name`: Name of the model.
  - `description`: Detailed description of the model.
  - `price`: Price in Wei.
- **Flow**: Stores model details on the blockchain.

### `purchaseModel(uint256 modelId)`
- **Purpose**: Enables users to buy a specific AI model by its ID.
- **Flow**:
  - Transfers the payment to the model's creator.
  - Records the purchase.

### `rateModel(uint256 modelId, uint8 rating)`
- **Purpose**: Lets users rate a purchased AI model.
- **Flow**:
  - Updates the model's average rating.
  - Increases the rating count.

### `withdrawFunds()`
- **Purpose**: Allows the contract owner to withdraw accumulated funds from model sales.
- **Flow**: Sends the balance to the owner’s Ethereum wallet.

### `getModelDetails(uint256 modelId)`
- **Purpose**: Retrieves details of a specific AI model.
- **Returns**:
  - `name`: Model name.
  - `description`: Model description.
  - `price`: Model price.
  - `creator`: Creator's Ethereum address.
  - `averageRating`: Current rating score.

---

## Frontend Components
### Homepage
- **Purpose**: Introduces users to the marketplace.
- **Includes**:
  - Call-to-action for browsing or adding models.
  - Dynamic design with floating cubes and animations.

### Add Model Page
- **Purpose**: Allows creators to list their AI models.
- **Includes**:
  - Input fields for model name, description, and price.
  - Connection to the `listModel` function.

### Available Models Page
- **Purpose**: Displays all listed models.
- **Includes**:
  - Grid view of models.
  - Buttons to purchase or view details.
  - Connection to `getModelDetails` and `purchaseModel` functions.

### Purchase and Rate Page
- **Purpose**: Lets users buy and rate models.
- **Includes**:
  - Model details.
  - Star-based rating system.
  - Connection to `purchaseModel` and `rateModel` functions.

### Withdraw Funds Page
- **Purpose**: Enables model creators to withdraw earnings.
- **Includes**:
  - Balance display.
  - Button to withdraw funds.
  - Connection to `withdrawFunds` function.

---

## Screenshots
Here are some screenshots showcasing the core features of the AI Model Marketplace:

### Homepage
![Homepage](/screenshots/screen1.png)

### Add Your Own Model
![Add Model](/screenshots/screen3.jpg)

### Available Models
![Available Models](/screenshots/screen3.jpg)

### Purchase Model
![Purchase Model](/screenshots/screen5.jpg)

### Withdraw Funds
![Withdraw Funds](/screenshots/screen6.jpg)

---

## Usage Instructions
### Prerequisites
1. Install [MetaMask](https://metamask.io/) and create a wallet.
2. Deploy the smart contract (`Assignment2.sol`) using Remix or Truffle.
3. Update the contract address in `.html` files.
4. Have test ETH (for testnets) or ETH for mainnet.

### Quick Start
1. Clone the repository:
   ```bash
   git clone https://github.com/gemdivk/Assignment2.git
   cd Assignment2
   ```
2. Open `index.html` in a browser.
3. Interact with the platform using MetaMask.

### Example Workflows
#### Adding a Model
1. Navigate to the "Add Your Own Model" page.
2. Enter model details (name, description, price).
3. Confirm the transaction in MetaMask.

#### Purchasing a Model
1. Select a model from "Available Models."
2. Click "Buy" and approve the transaction.
3. Access purchased models for rating.

#### Withdrawing Funds
1. Go to "Withdraw Funds."
2. View the balance.
3. Click "Withdraw Funds" and confirm.

---

## File Structure
```
AI-Model-Marketplace/
├── index.html              # Homepage
├── AddYourOwnModel.html    # Add models
├── AvailableModels.html    # Browse models
├── PurchaseAModel.html     # Purchase and rate models
├── WithdrawFunds.html      # Withdraw creator earnings
├── contractABI.json        # ABI for smart contract
├── Assignment2.sol         # Solidity smart contract
├── screenshots/            # Screenshots for documentation
```

---

## Technical Details
### Smart Contract Workflow
1. **List Models**: Data stored on-chain for transparency.
2. **Purchase Models**: Payment processed securely via Ethereum.
3. **Rate Models**: Ratings influence model credibility.
4. **Withdraw Funds**: Ensures creators get paid for their work.

### Web3.js Integration
Facilitates:
- Connection to Ethereum via MetaMask.
- Secure transaction handling.
- Real-time updates for users.

---


