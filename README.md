# Android Device Info
ADI aims to provide a powerful tool to retrieve information about the android device being used.

**Upcoming changes
* Battery information.

## Features
 **Retrieve the following information about the device's network**
 * MSISDN
 * IMSI
 * Status
 * Detailed status
 * Available networks (To be implemented)
 * Current network type
 * Preferential network (Not yet possible)
 * Bit error rate
 * Carrier
 * Several other informations can be retrieved.
 
## Usage

### Android Manifest
``` xml
<manifest>
    <!-- These are the permissions that you might need depending on the methods that you might access on this library. -->
    <uses-permission android:name="android.permission.READ_PHONE_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
    <uses-permission android:name="android.permission.READ_SMS"/>
    <uses-permission android:name="android.permission.READ_CALL_LOG"/>
    <uses-permission android:name="android.permission.READ_CONTACTS"/>

    <!-- This library has a utility class called FileUtilities to help you save the the JSON locally if you want to. If you want to use this funcionality, you will need the permission below in your manifest. -->
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
	...
</manifest>
```

### Available methods
``` java
AndroidInfoFacade.getNetworkInfo(context, listener); //This returns a bean with network info.
AndroidInfoFacade.getSentSmsHistory(context).getJson(); //This will return a String with history info about the sent SMS messages in a json format.
```

## Observations

This library is a working in progress. The main objective is to help the developer to retrieve different informations about the user's device.
