# VENOM-STABLE

FunC smart contracts for Stable token on TVM/TON (for instance equivalent of US Dollar) issued by central entity.

## Contract audit
Contract was [audited by Certik](https://www.certik.com/projects/the-open-network?utm_source=CoinGecko&utm_campaign=AuditByCertiKLink) and all findings have been addressed.

# Targets and goals

This project was created to allow users to exchange and buy assets in the VENOM DeFi ecosystem for a token (token or currency) that is not subject to volatile fluctuations. To meet regulatory requirements, the issuer of the tokens must have additional control over the tokens.

Thus this token represents a [standard TVM token smart contracts](https://github.
com/ton-blockchain/token-contract/tree/369ae089255edbd807eb499792a0a838c2e1b272/ft) with additional functionality:

- Admin of token can make transfers from user's token wallet.

- Admin of token can burn user's tokens.

- Admin of token can lock/unlock user's token wallet (`set_status`). If the status is not set to zero, then the user's wallet is locked, the user cannot make transfers; Admin can make transfer even if wallet locked.

- Admin of token can change token-minter code and it's full data.

__It is critically important for issuer to carefully manage the admin's account private key to avoid any potential risks of being hacked. It is highly recommend to use multi-signature wallet as admin account with private keys stored on different air-gapped hosts / hardware wallets.__

# Local Development

The following assumes the use of `node@>=16` and requires `func` and `fift` executable installed and in path.

## Install Dependencies

`npm install`

## Compile Contracts

`npm run build`

## Run Tests

`npm run test`

## Credits

Author @dariotarantini.
