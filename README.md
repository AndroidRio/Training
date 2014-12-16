# Android Device Info
ADI aims to provide a powerful tool to retrieve information about the android device being used.

**Upcoming changes**
* Battery information.

## Features
 **Retrieve the following information about the device's network**
 * Network information.
 * Call, SMS and MMS history.
 * Device information.
 
## Usage
``` java
AndroidInfoFacade.getNetworkInfo(context, listener); //This returns a bean with network info.
AndroidInfoFacade.getSentSmsHistory(context).getJson(); //This will return a String with history info about the sent SMS messages in a json format.
```
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

## Observations

This library is a working in progress. The main objective is to help the developer to retrieve different informations about the user's device.

License
-------

    Copyright 2014 Mobicare

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

<sub>Android Device Info © 2014, Mobicare.</sub>
