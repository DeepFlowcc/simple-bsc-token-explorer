# BSC Token Explorer

A lightweight, client-side tool for exploring BNB Smart Chain (BSC) tokens, prices, and transaction history without requiring backend infrastructure.

![BSC Token Explorer Screenshot](https://via.placeholder.com/800x450.png?text=BSC+Token+Explorer)

## Features

- **Token Information Lookup**: Get basic token information (name, symbol, decimals)
- **Real-time Price Data**: Fetch current token price in BNB and USD from PancakeSwap V3 pools
- **Transaction History**: View token transactions with buy/sell indicators using BSCScan API
- **Zero Backend Required**: Runs entirely in browser with direct blockchain interaction
- **Responsive Design**: Clean, modern interface that works on mobile and desktop

## How to Use

1. Open `index.html` in your web browser
2. Enter a BSC token contract address
3. (Optional) Enter a BSCScan API key to view transaction history
4. Click "Get Token Info" to display token details and transactions

## BSCScan API Key

To view transaction history, you'll need a free BSCScan API key:

1. Visit [BSCScan API Keys](https://bscscan.com/apis) and create an account if needed
2. Generate a new API key
3. Enter the API key in the designated field in the application

## Technologies

- **Web3.js**: Ethereum JavaScript API for blockchain interaction
- **PancakeSwap V3**: Price discovery through V3 pools with fallback fee tiers
- **BSCScan API**: Transaction history retrieval
- **Vanilla JavaScript**: No frameworks or dependencies needed
- **Responsive CSS**: Clean, modern design with intuitive UX

## Features in Detail

### Token Price Discovery

The application attempts to find the best price by trying different PancakeSwap V3 fee tiers in sequence:
- 0.25% (most common)
- 0.05%
- 0.01%
- 1.00% (high volatility pairs)

### Transaction Classification

Transactions are classified as:
- **Buy**: Token received from a DEX router
- **Sell**: Token sent to a DEX router
- **Transfer**: Standard wallet-to-wallet token transfers

### Failover RPC Support

The application includes multiple BSC RPC endpoints with automatic failover if the primary connection fails.

## Local Development

Simply clone the repository and open `index.html` in a browser. No build process or server setup is required.

```bash
git clone https://github.com/yourusername/bsc-token-explorer.git
cd bsc-token-explorer
# Open index.html in your browser
```

## Limitations

- Only works with BEP-20 tokens on the BNB Smart Chain
- Requires a BSCScan API key for transaction history
- Only shows tokens with active PancakeSwap V3 liquidity pools

## License

MIT

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Disclaimer

This tool is for informational purposes only. Always do your own research before trading cryptocurrencies. 