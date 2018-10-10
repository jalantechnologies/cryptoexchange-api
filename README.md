# cryptoexchange-api
Cryptexchange API built on Kony Fabric

### To initialize
```
                
/**
* Kony Fabric is auto initialized, only if the Kony Fabric app is linked in the Kony Visualizer.
* In all other cases the Kony Fabric initialization code should be written by User.
*/
KNYMobileFabric = new kony.sdk();
KNYMobileFabric.init("518da4cef0e3183ce8c9d707ffd4b3a7","******","/appconfig",successCallback, errorCallback);
function successCallback(res){
//code for success call back
}
function errorCallback(res){
//code for failure call back
}
```

### To get all coins
```
/**
 * NOTE: All the placeholders are represented as <place-holder>, so just that part must be replaced
 * with the actual value, rest of the things must remain same.
 * Kony Fabric is auto initialized, only if the Kony Fabric app is linked in the Kony Visualizer.
 * In all other cases the Kony Fabric initialization code should be written by User if not done
 * already, for below sample to work.
 */
//Code to invoke parent integration service should be present to use below code.
operationName =  "getcoins";
data= {};
headers= {};
integrationObj.invokeOperation(operationName, headers, data, operationSuccess, operationFailure);
function operationSuccess(res){
	//code for success call back
}
function operationFailure(res){
	//code for failure call back
}
```

### To get exchange information between two coins
```
/**
 * NOTE: All the placeholders are represented as <place-holder>, so just that part must be replaced
 * with the actual value, rest of the things must remain same.
 * Kony Fabric is auto initialized, only if the Kony Fabric app is linked in the Kony Visualizer.
 * In all other cases the Kony Fabric initialization code should be written by User if not done
 * already, for below sample to work.
 */
//Code to invoke parent integration service should be present to use below code.
operationName =  "marketinfo";
data= {"pair": "<place-holder>"};
headers= {};
integrationObj.invokeOperation(operationName, headers, data, operationSuccess, operationFailure);
function operationSuccess(res){
	//code for success call back
}
function operationFailure(res){
	//code for failure call back
}
```
For example, in order to get exchange rate between bitcoin and ethereum, `pair` will be `btc_eth`
