
# Unstoppable contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Arbitrum
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
any. More context below
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
none
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
Any. More context below
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

Margin: no
Spot: possibly

___

### Q: Are there any REBASING tokens interacting with the smart contracts?

Margin: no
Spot: possibly
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
RESTRICTED
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
TRUSTED
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
no
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
no
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
n.a
___

### Q: Please provide links to previous audits (if any).
n.a
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
Keepers monitoring positions and executing orders and liquidations.
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
Yes.
___

### Additional Information on tokens used
The Spot contracts need to be able to interact with any pool/token, we don’t want to have a centralized whitelist, we want it to work with any Uniswap v3 pool (and later others but this is probably out of scope).

The Margin DEX has whitelisted tokens/markets anyways, so lets assume WETH, wBTC, ARB, USDC, USDT + default OZ ERC20 implementations as scope. We’ll have to keep that in mind then before considering other markets.


# Audit scope


[unstoppable-dex-audit @ 4153c3e67ccc080032ba0bbaffd9a0c56a573070](https://github.com/Unstoppable-DeFi/unstoppable-dex-audit/tree/4153c3e67ccc080032ba0bbaffd9a0c56a573070)
- [unstoppable-dex-audit/contracts/margin-dex/MarginDex.vy](unstoppable-dex-audit/contracts/margin-dex/MarginDex.vy)
- [unstoppable-dex-audit/contracts/margin-dex/SwapRouter.vy](unstoppable-dex-audit/contracts/margin-dex/SwapRouter.vy)
- [unstoppable-dex-audit/contracts/margin-dex/Vault.vy](unstoppable-dex-audit/contracts/margin-dex/Vault.vy)
- [unstoppable-dex-audit/contracts/spot-dex/Dca.vy](unstoppable-dex-audit/contracts/spot-dex/Dca.vy)
- [unstoppable-dex-audit/contracts/spot-dex/LimitOrders.vy](unstoppable-dex-audit/contracts/spot-dex/LimitOrders.vy)
- [unstoppable-dex-audit/contracts/utils/Univ3Twap.sol](unstoppable-dex-audit/contracts/utils/Univ3Twap.sol)


