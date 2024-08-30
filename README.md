# pymoonshotlib
python moonshot trade sdk



### Install

```
pip install  pymoonshotlib-1.0.0-py3-none-any.whl
```



### Usage

```
from pymoonshotlib.api import MoonShot

if __name__ == '__main__':
    _private_key = '67rpwLCuS5DGA8KGZXKsVPuheKEb183tzoZ8WFUAFJnqEvsKKrePqksDCCc1qvkkRzHxD5tEhSkUUfjW2aQzMJGE'
    _rpc_endpoints = "https://mainnet.helius-rpc.com/?api-key=6dcb92e3-5222-4d11-9dc4-dbee6df8f373"
    client = MoonShot(private_key=_private_key, rpc_endpoints=_rpc_endpoints)

    # buy
    mint_str = "token_to_buy"
    client.buy(mint_str=mint_str, sol_in=0.01, slippage_bps=500)

    # sell
    mint_str = "token_to_sell"
    token_balance = client.get_token_balance(mint_str)
    client.sell(mint_str=mint_str, token_balance=token_balance, slippage_bps=500)

```



### Tips

Slippage is in bps format. 500bps equals 5% slippage.

