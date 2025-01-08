![](static/header.svg)
<p align="center">
    <a href="#">
        <img src="https://img.shields.io/github/actions/workflow/status/artcher19/CryptoBotSyncApi/pyproject.toml?style=flat-square" />
    </a>
    <a href="#">
        <img src="https://img.shields.io/github/license/artcher19/CryptoBotSyncApi?style=flat-square" />
    </a>
    <a href="https://t.me/artcher_news">
        <img src="https://img.shields.io/badge/telegram-group-blue?style=flat-square&logo=telegram" />
    </a>
    <a href="#">
        <img src="https://img.shields.io/github/stars/artcher19/CryptoBotSyncApi?style=social" />
    </a>
</p>

# Overview
This is a simple sync Python library for API [@CryptoBot](https://t.me/send?start=r-2buqm) particularly transaction service CryptoPay.

Check official API documentation: https://help.crypt.bot/crypto-pay-api
# Installation
```sh
pip install CryptoBotSyncApi
```
---
# First Steps
1. Create your application and get an API token:
Open [@CryptoBot](https://t.me/send?start=r-2buqm) or [@CryptoTestnetBot](http://t.me/CryptoTestnetBot) (for testnet).
2. Send bot a command `/pay` to create a new app and get API Token.
3. Copy 
>All queries to the Crypto Pay API must be sent over HTTPS
---
# Example
```
pay = CryptoPay("crypto_bot_api")
invoice = pay.create_invoice(amount='500', currency_type='fiat', accepted_assets='usdt,btc', fiat='RUB')
```
---
# Methods
- get_me() - Use this method to test your app's authentication token. Requires no parameters.
- create_invoice() - Use this method to test your app's authentication token. Requires no parameters.
- delete_invoice - Use this method to delete invoices created by your app.
- create_check - Use this method to create a new check.
- delete_check - Use this method to delete checks created by your app.
- transfer - Use this method to send coins from your app's balance to a user. This method must first be enabled in the security settings of your app. Open @CryptoBot (@CryptoTestnetBot for testnet), go to Crypto Pay → My Apps, choose an app, then go to Security -> Transfers... and tap Enable.
- get_invoices() - Use this method to get invoices created by your app.
- get_transfers() - Use this method to get transfers created by your app.
- get_checks() - Use this method to get checks created by your app.
- get_balance() - Use this method to get balances of your app. Requires no parameters.
- get_exchange_rates() - Use this method to get exchange rates of supported currencies. Requires no parameters.
- get_currencies() - Use this method to get a list of supported currencies. Requires no parameters.
- get_stats() - Use this method to get app statistics.
---
