# Project Planning

## Project Goal
To provide a secure and easy-to-use tool for converting Bittensor/Substrate mnemonic phrases into their corresponding 32-byte hex seeds. This is primarily for users of Subnet 77 who need the hex seed for voting scripts.

## Architecture
The project consists of two main parts:
1.  **CLI Tool (`phrase2Hex.py`):** A Python script for users who prefer a command-line interface. It uses the `substrate-interface` library.
2.  **Web Front-end (`index.html`):** A static, client-side HTML page for a user-friendly graphical interface. It will be hosted on GitHub Pages. All conversion logic is handled in the browser using Polkadot.js libraries, ensuring mnemonics are never transmitted over the internet.

## Style Guide
-   **Python:** PEP8 compliant, `black` formatted, Google-style docstrings.
-   **Front-end:** A single, self-contained `index.html` file. The visual theme is a clean, modern take on a retro computer terminal (dark background, green text, monospace font).

## Constraints
-   The web front-end must be fully static and work without a server backend.
-   Security is paramount. The mnemonic phrase must never leave the user's browser.
-   The conversion logic must be accurate and match the output of the `substrate-interface` library used in the Python script. 