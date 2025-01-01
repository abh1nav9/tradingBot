# Trading Bot

## Project Overview
The Trading Bot is a simple automated trading application designed to fetch real-time stock prices and perform trading operations based on predefined logic. The bot utilizes the Alpaca API for market data and trading functionalities, allowing users to monitor stock prices and execute trades seamlessly.

## Tech Stack
- **Node.js**: JavaScript runtime for building the server-side application.
- **Axios**: Promise-based HTTP client for making requests to the Alpaca API.
- **File System (fs)**: Node.js built-in module for logging and storing information.
- **Alpaca API**: API used for fetching stock prices and executing trades.

## Features
- Fetches real-time stock prices for specified stocks (e.g., AAPL).
- Logs stock price data to a local file for future reference.
- Executes buy/sell orders based on specified trading logic.
- Handles API requests and responses with error management.

## How to Run the Application
1. **Clone the repository**:
   ```bash
   git clone https://github.com/abh1nav9/tradingBot.git
   cd tradingBot
2. **Install dependencies:**:
   ```bash
   npm install
3. **Set up your Alpaca API credentials:** Create a `.env` file in the root directory of the project and add your Alpaca API Key and Secret:
   ```bash
   API_KEY=your_api_key
   SECRET_KEY=your_api_secret
4. **Run the application:**
   ```bash
   node index.js

## Trading Logic
The trading logic is defined to determine when to buy or sell stocks based on the fetched prices. The criteria for trading can be customized and currently involves checking the stock price against a threshold. If the price meets the conditions, the bot will execute a trade through the Alpaca API.

## API Usage
The application makes use of the following endpoint from the Alpaca API:

Get Latest Quote:

**Endpoint**: `GET https://data.alpaca.markets/v2/stocks/{symbol}/quotes/latest`

**Headers:**

`APCA_API_KEY_ID:` Your Alpaca API Key

`APCA_API_SECRET_KEY:` Your Alpaca API Secret

## Example Request
  ```bash
 const response = await axios.get(`${ALPACA_API_URL}/v2/stocks/AAPL/quotes/latest`, {
    headers: {
        'APCA_API_KEY_ID': API_KEY,
        'APCA_API_SECRET_KEY': API_SECRET,
    },
  });
```
## Critical Decisions
**Choice of Technology:** Node.js was selected for its asynchronous capabilities and extensive package ecosystem, allowing for efficient API calls and logging mechanisms.

**Trading Strategy:** A simple price threshold strategy was implemented for ease of use and clarity. This can be expanded with more complex algorithms as needed.

## Problems Tackled While Building
**Handling API Errors:** Implemented robust error handling to manage various API response statuses, such as 403 Forbidden errors.
**Asynchronous Programming:** Managed asynchronous calls to ensure that price fetching and trading logic execution do not block each other.
**Logging Mechanism:** Developed a simple logging mechanism to track stock prices and trade actions for analysis and debugging.

## Credits
**Linkedin:** `https://www.linkedin.com/in/iabhinavgautam`

**Twitter:** `https://www.x.com/abh1av`

**Github:** `https://www.github.com/abh1nav9`

**Leetcode:** `https://www.leetcode.com/u/abhinavgautam9`
