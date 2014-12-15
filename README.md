Training
========

Repositório de Treinamento

# ! Android Device Info
ADI aims to provide a powerful tool to retrieve information about the android device being used.

## Features
 ** Retrieve the following information about the device's network
 * MSISDN
 * IMSI
 * Status
 * Detailed status
 * Available networks (To be implemented)
 * Current network type
 * Preferential network (Not yet possible)
 * Bit error rate
 * Carrier
 
## Usage

### Available methods
``` java
AndroidInfoFacade.getNetworkInfo(context, listener); //This returns a bean with network info.
AndroidInfoFacade.getSentSmsHistory(context).getJson(); //This will return a String with history info about the sent SMS messages in a json format.
```

## Observations

This library is a working in progress. The main objective is to help the developer to retrieve different informations about the user's device.
