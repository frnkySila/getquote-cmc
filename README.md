
This is a `getquote` script that converts cryptocurrencies into fiat according to CoinMarketCap rates. Please note that these rates are weighted averages over multiple exchanges and may not represent the actual value of your assets.

#### Requirements

Python 2.6+, `requests`.

#### Installation

Put the `getquote` script somewhere in your `$PATH`, e.g.

`cp getquote /usr/local/bin/getquote`

#### Usage

Account for cryptos and fiat using their CMC symbols, e.g. "BCH" for Bitcoin Cash, "RUB" for Russian Rouble:

```
01-06
    Assets:Exchanges:Wex  -1454.7657 RUB
    Assets:Exchanges:Wex  0.00998 BCH
    Expenses:Fees:Exchanges:Trade  0.00002 BCH
```

```
ledger -f crypto.dat bal Assets Draw Equity -X RUB -Q
```

#### Limitations

You can only get rates on top-100 cryptos as that's what CMC gives through their API.

TODO: parse the "View All" page instead of using the API.
