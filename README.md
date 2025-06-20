# sn77-Phrase2Hex: Mnemonic to Hex Converter

A secure, client-side tool to convert a 12 or 24-word BIP39 mnemonic phrase into a Substrate-compatible 32-byte hex seed and its corresponding SS58 address. This tool is specifically designed to streamline development and operations for Bittensor's Subnet 77.

It runs entirely in your browser. **Your mnemonic is never stored, processed on a server, or sent over the network.**

---

## ✨ Features

- **Client-Side Security**: All cryptographic operations are performed locally in your browser using the battle-tested `polkadot.js` library.
- **Dual Output**: Generates both the SS58 public address (for verification) and the 32-byte hex seed.
- **Role-Specific Commands**: Provides ready-to-use, one-click terminal commands to update your `.env` file for both:
  - `HOLDER_COLDKEY` (for voters)
  - `MINER_HOTKEY` (for miners)
- **Intuitive UI**: A clean, retro-hacker terminal interface for a straightforward user experience.
- **Command-Line Fallback**: Includes a simple Python script (`phrase2Hex.py`) for command-line users.

---

## 🚀 How to Use the Web Interface

1.  **Open `index.html`**: Open the `index.html` file in any modern web browser.
2.  **Enter Mnemonic**: Type or paste your 12 or 24-word mnemonic phrase into the input area.
3.  **Convert**: Click the `Convert >_` button.
4.  **Verify & Use**:
    - The tool will display your public SS58 address (verify this matches your wallet).
    - It will also display the 32-byte hex seed.
    - Choose the appropriate terminal command (`HOLDER_COLDKEY` or `MINER_HOTKEY`) and click the copy button.
    - Paste and run the command in your terminal to automatically update your `sn77/.env` file.

---

## 🐍 Command-Line Script (Python)

For users who prefer the terminal.

### Requirements
- Python 3
- `substrate-interface` library

### Installation
1.  Clone this repository.
2.  Install the required package:
    ```bash
    pip install substrate-interface
    ```

### Usage
Run the script from your terminal:
```bash
python3 phrase2Hex.py
```
You will be prompted to enter your mnemonic phrase. The script will output your SS58 address and the 32-byte hex seed.

---

## 🔒 Security First

The security of your keys is paramount.
- **No Network Activity**: The conversion logic uses JavaScript modules that run directly in your browser. Open your browser's developer tools and check the "Network" tab to verify that no requests are made when you convert your phrase.
- **Trusted Libraries**: It relies on the official and widely-used `polkadot.js` cryptographic libraries.
- **Best Practice**: After use, it is recommended to clear the page or close the browser tab to ensure your mnemonic is not left visible.