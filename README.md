# ERC20DividendPayingToken
 A mintable dividend-paying ERC20 token contract written in solidity.

This Smart Contract is based on the ERC 1726 dividend paying token from [Roger-Wu](https://github.com/Roger-Wu/erc1726-dividend-paying-token). 

## Key difference with DividendPayingToken 
The original DividendPayingToken was designed to send the native token as dividend (ETH in Ethereum, MATIC in Polygon, BNB in Binance Smart Chain, etc.).
This token can send any ERC20 as a dividend, which makes it very useful to send any wrapped cryptocurrency or stablecoin, instead a native token.

You must specify the ERC20 token address that you will send as a dividend, in the constructor:

```sh
  constructor(string memory _name, string memory _symbol, address erc20dividendtoken) ERC20(_name, _symbol) {
      dividendToken = IERC20(erc20dividendtoken);
  }
```

### Solidity version updated to 0.8.1
The Solidity version of the original Smart Contract was 0.5.0
This Smart Contract is written in the recent 0.8.1
For that reason, SafeMath is not required any longer for uint type.

#### Original code commented (by the moment)
In order to make it easier to compare the current code, with the original one, I let the original code commented over the current line code.
