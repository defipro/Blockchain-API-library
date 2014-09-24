##`info.blockchain.api.createwallet` package

The `createwallet` package contains the `CreateWallet` class that reflects the functionality documented at https://blockchain.info/api/create_walleti. It allows users to create new wallets as long as their API code has the 'generate wallet' permission. 

Example usage:

```java

package test;
import info.blockchain.api.createwallet.*;

public class App 
{
    public static void main(String[] args) throws Exception
    {	
    	CreateWalletResponse wallet = CreateWallet.create("someComplicated123Password", "8fd2335e-720c-442b-9694-83bdd2983cc9");
    	
    	System.out.println(wallet.getIdentifier());
    }
}

```