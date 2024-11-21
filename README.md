# Pump.fun Solana Trading and Sniping Bot

Welcome to the Pump.fun Solana Trading Bot! This tool, developed by [HackerChain](https://github.com/HackerChain) is designed for trading and sniping new token launches on pump.fun. It includes strategies for buying and selling tokens based on market cap changes and bonding curve progress.

## Overview

The Solana Trading Bot helps you trade tokens on the Pump.fun on Solana blockchain based on bonding curves and market cap changes. The bot scrapes data to identify new tokens with favorable bonding curves, monitors market cap changes, and makes decisions on when to sell to maximize profits.

## Trading Strategy

- **Initial Buy**: The bot scrapes pump.fun to identify new token pairs with favorable bonding curves.
- **Monitoring**: Once a token is bought, the bot monitors the market cap and bonding curve progress.
- **Profit Targets**:
  - The bot aims to take profit at a 25% increase and then again at another 25% increase.
  - It sells 50% of the tokens at the first 25% increase and 75% of the remaining tokens at the next 25% increase.
- **Stop Loss**: The bot will sell all tokens if the market cap falls by 10%.
- **Bonding Curve**: The bot will sell 75% of the tokens if the bonding curve reaches a critical level and keep 25% as a moon bag.
- **Timing**: The bot resets the timer if the price goes up and monitors the trade for a set period, adjusting its actions based on market conditions.

## Requirements

- **Node.js**: JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Solana CLI**: Command-line interface for interacting with the Solana blockchain.
- **Selenium WebDriver (Chrome)**: Automated web browser.

## Installation

1. **Clone the repository**:

   ```
   https://github.com/HackerChain/Pump-fun-sniper-bot.git
   cd Pump-fun-sniper-bot
   ```

2. **Install dependencies**:

   ```
   npm install dotenv axios @solana/web3.js @solana/spl-token selenium-webdriver fs bs58 blessed blessed-contrib
   ```

3. **Set up your environment variables**:
   Create a .env file in the root directory and add the following:

   ```
   SOLANA_WALLET_PATH=/path/to/your/solana/wallet.json
   MINIMUM_BUY_AMOUNT=0.015
   MAX_BONDING_CURVE_PROGRESS=10
   SELL_BONDING_CURVE_PROGRESS=15
   ```

4. **Configure Solana CLI**:
   ```
   solana config set --url https://api.mainnet-beta.solana.com
   solana config set --keypair /path/to/your/solana/wallet.json
   ```

## Usage

- **Run the trading bot**:

  ```
  node script.mjs
  ```

- **Sell all SPL tokens**:
  ```
  node sell.js
  ```

## Contact

For any questions or support, please contact us at [Email](jasonsmith0614.dev@gmail.com).
