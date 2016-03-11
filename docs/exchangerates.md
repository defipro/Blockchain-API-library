##`info.blockchain.api.exchangerates` package

The `exchangerates` package contains the `ExchangeRates` class that reflects the functionality documented at https://blockchain.info/api/exchange_rates_api. It allows users to get price tickers for most major currencies and directly convert fiat amounts to BTC.

Example usage:

```java

package test;
import info.blockchain.api.exchangerates.*;

public class App 
{
    public static void main(String[] args) throws Exception
    {	
		// get the ticker map
        Map<String, Currency> ticker = ExchangeRates.getTicker();
        BigDecimal BTCUSDsell = ticker.get("USD").getSell();

        // convert 5362 EUR to BTC
        BigDecimal EURToBTC = ExchangeRates.toBTC("EUR", new BigDecimal(53620));
    }
}

```