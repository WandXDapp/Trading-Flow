# Trading Flow
This page allows users to swap between ERC20 tokens. Desktop app will search Bancor, Kyber, Uniswap and 0x Relayer to present best possible rate before user.

## Welcome Screen
Initially *Ethereum Address* of the user will be  displayed. User will have to fill following 3 fields:
1. **Input Token**: The token user want to sell.
2. **Amount**: Quantity of input token user want to sell.
3. **Output Token**: The token user want to buy.

## Step - 1
User selects *Input Token* to sell.

- Available balance of the user corresponding to that token will be displayed.

User also fills *Amount* of token to sell and selects *Output Token* to buy.

### Response
User can proceed to next step if following conditions are satisfied:
- All the 3 fields have been filled
- *Amount* is valid decimal
- *Amount* is not greater than available *Balance* of *Input Token*

***Check Rates*** button will appear to proceed to the next step.

## Step - 2
User clicks ***Check Rates*** button to check rates at different exchanges such as *Bancor*, *Kyber*, *Uniswap*, *0x Relayer*.

### Response
**Case 1**: If the selected pair of tokens are not available in any one of the above exchanges then error message will be displayed.  
**Case 2**: Otherwise desktop app will fetch **minimum** amount of *Output Token* that user will certainly receive (**or transaction will fail**) on the pre mentioned exchanges. The exchanges which does not support the swap of these tokens will not be displayed. Also ***Use the Best Exchanges*** button will appear to proceed to next step.

## Step - 3
User clicks ***Use the Best Exchanges*** button so that app can prepare trade with best exchanges.

### Response
**Case 1**: On successful preparation of trades ***Confirm Transaction*** button will appear.  
**Case 2**: If there is some error while preparing trade then error message will be displayed.

## Step - 4
User clicks ***Confirm Transaction*** button to complete the trading process.

### Response
**Transaction Hashes** (corresponding to transactions which has been submitted to blockchain to complete the trade) will be displayed sequentially. User can click the arrow beside the hash to check the status on *etherscan.io*, once the transaction is included in a block the status of the transaction will pop up in desktop app.
