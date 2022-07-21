## Comono React Native SDK
Comono is a quick and secure way to carry out digital address verification.

## Installation
```
npm install react-native-com-address 
```
Also, install react-native-webview because it's a dependency for this package. Here's a [link](https://github.com/react-native-webview/react-native-webview) to their docs.

## Usage
``` Typescript
import React, { useState } from 'react';

import { StyleSheet, View, Text, TouchableOpacity } from 'react-native';
import { Verifyaddress } from 'react-native-com-address';

export default function App() {
  const [openSDK, setOpenSDK] = useState(false);

  const handleOpen = () => {
    setOpenSDK(true);
  };

  const handleClose = () => {
    setOpenSDK(false);
  };

  return (
    <>
      <View style={styles.container}>
        <Text>hello world!</Text>
        <TouchableOpacity
          onPress={handleOpen}
          style={{
            backgroundColor: '#007BFF',
            paddingVertical: 10,
            paddingHorizontal: 20,
            marginTop: 20,
            borderRadius: 5,
          }}
        >
          <Text style={{ fontSize: 15, color: 'white' }}>open SDK</Text>
        </TouchableOpacity>
      </View>

      <Verifyaddress
        onClose={handleClose}
        onOpen={openSDK}
        workitemId=""     
        customerName="r"     
        customerEmail=""     
        branchCode=""     
        segmentId=""     
        houseNumber=""     
        streetName=""     
        areaName=""     
        landmark=""     
        state=""     
        lga=""     
        createdBy=""     
        customerImage=""     
        latitude=""     
        longitude=""     
      />
    </>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center',
  },
});
```

## Configuration Options
 
* [```workitemId```](#workitemid)
* [```customerName```](#customername)
* [```customerEmail```](#customeremail)
* [```branchCode```](#branchcode)
* [```segmentId```](#segmentid)
* [```houseNumber```](#housenumber)
* [```streetName```](#streetname)
* [```areaName```](#areaname)
* [```landmark```](#landmark)
* [```state```](#state)
* [```lga```](#lga)
* [```createdBy```](#createdby)
* [```customerImage```](#customerimage)
* [```latitude```](#latitude)
* [```longitude```](#longitude)


### ```workitemId```
**string: Required** The workitem Id for the customer's account

### ```customerName```
**string: Required** The customer's full name

### ```customerEmail```
**string: optional** The customer's email address

### ```branchCode```
**string: required** The branch code of the customer's account

### ```segmentId```
**string: required** The segment of the customer's account

### ```houseNumber```
**string: required** The customer's house/block/apartment number

### ```streetName```
**string: required** The customer's street 

### ```areaName```
**string: required** The area of the customer's house address

### ```landmark```
**string: required** The major landmark closest to the customer's house

### ```state```
**string: required** The state of the customer's residence

### ```lga```
**string: required** The lga of the customer's residence

### ```createdBy```
**string: optional** The customer's account officer

### ```customerImage```
**string: optional** The customer's picture

### ```latitude```
**string: optional** The customer's current location

### ```longitude```
**string: optional** The customer's current location


## Support
If you're having trouble with Comono React or your integration, please reach out to us at support@comono.io. We're more than happy to help you out.
