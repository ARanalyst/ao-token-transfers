# AO Wallet Explorer

A web-based tool for exploring AO token transactions and checking wallet balances on the Arweave ecosystem.

> **💡 Looking for more comprehensive AO ecosystem information?** Check out [ao.link](https://www.ao.link/) - an amazing explorer with detailed insights into the AO network, processes, and much more!

## Features

### 🔍 Transaction Explorer
- **Transaction History**: View detailed transaction history for any wallet address
- **Token Filtering**: Filter transactions by specific tokens (AO, ARIO, wUSDC, PI, wAR, qAR, USDA, wETH, PIXL, SMONEY, and more)
- **Transaction Types**: Filter by incoming (Credit-Notice) or outgoing (Debit-Notice) transactions
- **Date Range**: Filter transactions by start and end dates
- **Preview Mode**: Quick preview of the latest 20 transactions
- **CSV Export**: Download complete transaction history as CSV file

### 💰 Balance Checker
- **Real-time Balances**: Check current token balances for any wallet
- **Multi-token Support**: View balances for all supported tokens or specific ones
- **Automatic Conversion**: Properly converts raw token amounts using correct decimal factors
- **Clean Display**: Zero balances and errors are handled gracefully

### 📊 Data Display
- **Responsive Tables**: Clean, scrollable tables with proper formatting
- **Token Information**: Shows token tickers, process IDs, and formatted quantities
- **Transaction Details**: Complete transaction information including timestamps, addresses, and amounts

## Supported Tokens

| Token | Ticker | Process ID |
|-------|--------|------------|
| AO | AO | 0syT13r0s0tgPmIed95bJnuSqaD29HQNN8D3ElLSrsc |
| ARIO | ARIO | qNvAoz0TgcH7DMg8BCVn8jF32QH5L6T29VjHxhHqqGE |
| Wrapped USDC | wUSDC | 7zH9dlMNoxprab9loshv3Y7WG45DOny_Vrq9KrXObdQ |
| Permaweb Index | PI | 4hXj_E-5fAKmo4E8KjgQvuDJKAFk9P2grhycVmISDLs |
| Wrapped AR | wAR | xU9zFkq3X2ZQ6olwNVvr1vUWIjc3kXTWr7xKQD6dh10 |
| Quantum AR | qAR | NG-0lVX882MG5nhARrSzyprEK6ejonHpdUmaaMPsHE8 |
| Astro USD  | USDA | FBt9A5GA_KXMMSxA2DJ0xZbAq8sLLU2ak-YJe9zDvg8 |
| Wrapped ETH | wETH | cBgS-V_yGhOe9P1wCIuNSgDA_JS8l4sE5iFcPTr0TD0 |
| PIXL | PIXL | DM3FoZUq_yebASPhgd8pEIRIzDW6muXEhxz5-JwbZwo |
| Space Money | SMONEY | K59Wi9uKXBQfTn3zw7L_t-lwHAoq3Fx-V9sCyOY3dFE |

## Usage

### Getting Started
1. Open the HTML file in any modern web browser
2. Enter a wallet address in the "Wallet-Address" field
3. Choose your desired filters and options
4. Use one of the action buttons

### Transaction History
1. **Show Preview**: View the latest 20 transactions matching your filters
2. **Download CSV**: Export all matching transactions to a CSV file
3. Use the token dropdown to filter by specific tokens
4. Select transaction type (All/Incoming/Outgoing)
5. Set date ranges to limit results to specific time periods

### Balance Checking
1. Enter a wallet address
2. Optionally select a specific token (leave as "All" to check all tokens)
3. Click "Check Balance"
4. View results in a clean table format

## Technical Details

### APIs Used
- **Arweave GraphQL**: For transaction history via Goldsky's indexing service
- **AO Testnet**: For real-time balance queries via compute units

### Data Processing
- Automatic quantity conversion using token-specific decimal factors
- Parallel API requests for faster balance checking
- Proper error handling with timeouts
- CSV export functionality with proper escaping

### Performance Features
- **Parallel Processing**: Balance checks run simultaneously for multiple tokens
- **Timeout Protection**: 10-second timeout prevents hanging requests
- **Efficient Pagination**: Handles large transaction histories automatically
- **Responsive UI**: Tables with scrolling and text overflow handling

## Browser Compatibility

Works with all modern browsers that support:
- ES6+ JavaScript features
- Fetch API
- Promise.all()
- AbortController

## Installation

No installation required! Simply:
1. Download the HTML file
2. Open it in your web browser
3. Start exploring AO transactions

## Contributing

To add support for new tokens:
1. Add the token information to the `tokenMap` object
2. Include the token in the dropdown options
3. Ensure the correct decimal factor is specified

## Related Resources

- **[ao.link](https://www.ao.link/)** - Comprehensive AO ecosystem explorer with detailed network insights, process information, and advanced analytics
- **[AO Documentation](https://cookbook_ao.arweave.net/)** - Official AO computer documentation
- **[Arweave](https://arweave.org/)** - The underlying decentralized storage network

## License

This project is open source and available under the MIT License.

## Disclaimer

This tool is provided as-is for educational and informational purposes. Always verify transaction data through official sources before making financial decisions.
