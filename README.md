# Ton Radar dot Org
TonRadar.org API for Token and Project Prices

# TonRadar.org Crypto Price API FAQ

* What is the TonRadar Crypto Price API?

The TonRadar Crypto Price API provides developers with real-time and historical cryptocurrency price data, including for assets on the TON blockchain. It offers access to prices, market capitalization, trading volume, and more, sourced from multiple exchanges for accuracy.

* How do I access the API?
  
To use the TonRadar Crypto Price API, you need to sign up for an API key on the TonRadar developer portal (https://tonradar.org/developer). Once registered, you can generate your API key and start making requests.

# What data can I retrieve?
  
## The API provides:

* Real-time Prices: Current prices for cryptocurrencies, including TON-based assets.
* Historical Data: OHLCV (Open, High, Low, Close, Volume) data for specified time intervals.
* Market Data: Market capitalization, 24-hour trading volume, and circulating supply.
* Exchange Data: Trading pairs and exchange-specific price data.
* Supported Assets: Data for thousands of cryptocurrencies, including major assets like Bitcoin, Ethereum, and TON-native tokens.

# What are the API endpoints?

Key endpoints include:

/price: Fetch real-time prices for specified cryptocurrencies.
/historical: Retrieve OHLCV data for a given time range.
/markets: Get market data like volume and market cap.
/exchanges: Access trading pair data across supported exchanges.

For a full list, refer to the API documentation at https://tonradar.org/

* What is the rate limit?

Free Plan: 30 calls/minute, 10,000 calls/month.
Paid Plans: Up to 1,000 calls/minute, with higher quotas based on subscription tier. Check https://tonradar.org/developer/pricing for details.

How do I authenticate requests?
Include your API key in the request header:
X-API-Key: your_api_key_here

* What formats are supported?

The API returns data in JSON format via RESTful endpoints. GraphQL support is planned for future releases.

* Can I access historical data?

Yes, the /historical endpoint allows you to retrieve OHLCV data for specific cryptocurrencies, with customizable time intervals (e.g., 1-minute, hourly, daily). Historical data availability depends on the subscription plan.

* How do I handle CORS issues?

Direct client-side requests are not supported to protect your API key. Proxy requests through your backend server to avoid CORS errors and secure your key.

* What programming languages are supported?

The API is language-agnostic and works with any language that supports HTTP requests (e.g., Python, JavaScript, Java). Sample code is available in the documentation for Python, Node.js, and cURL.

# Example Request (Python)

import requests

url = "https://api.tonradar.org/v1/price?symbols=TON,BTC"
headers = {"X-API-Key": "your_api_key_here"}

response = requests.get(url, headers=headers)
print(response.json())

Is there a free tier?

Yes, the free tier includes limited access with 30 calls/minute and 10,000 calls/month, ideal for prototyping and small projects.
How accurate is the data?

TonRadar aggregates data from over 50 centralized and decentralized exchanges, including TON-based DEXs, to ensure high accuracy. Data is updated every 60-120 seconds.
Can I access DEX data?

Yes, paid subscribers can access on-chain DEX data for TON and other blockchains, including liquidity pool data and token-specific trading metrics.
How do I upgrade my plan?

Visit the TonRadar developer portal (https://tonradar.org/tokens) to view and upgrade your subscription plan. 

* What happens if I exceed my rate limit?

Requests exceeding the rate limit return a 429 Too Many Requests error. Paid plans offer higher limits, and you can monitor usage in the developer portal.

* Is there support for WebSocket streaming?

Currently, the API uses RESTful endpoints. WebSocket support for real-time streaming is under development and expected in Q3 2025.

* How do I report issues or get support?

Join the TonRadar Discord community (https://t.me/tonradarr) or email support@tonradar.org for assistance. Include your API key and request details for faster resolution.

*Are there SDKs or libraries available?

Official SDKs for Python and Node.js are available on GitHub (https://github.com/tonradar). Community-contributed libraries may also be found in the developer portal.

* Can I use the API for commercial projects?

Yes, commercial use is permitted under paid plans. Review the terms of service at https://tonradar.org/developer/terms for details.

## Where can I find more information?

* Documentation: https://tonradar.org
* Pricing: https://www.tonradar.org/tokens
* Community: https://x.com/ton_radar
* GitHub: https://github.com/tonradar-api/
* Telegram: https://t.me/tonradarr

