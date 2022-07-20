## Comono React Native SDK
Comono is a quick and secure way to carry out digital address verification.

## Installation
```
npm install react-native-com-address 
```
Also, install react-native-webview because it's a dependency for this package. Here's a link to their docs.

## Usage
```import React, { useState } from 'react';

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
        workitemId=""     //string
        customerName="r"     //string
        customerEmail=""     //string
        branchCode=""     //string
        segmentId=""     //string
        houseNumber=""     //string
        streetName=""     //string
        areaName=""     //string
        landmark=""     //string
        state=""     //string
        lga=""     //string
        createdBy=""     //string
        customerImage=""     //base64string
        Latitude=""     //string
        Longitude=""     //string
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
