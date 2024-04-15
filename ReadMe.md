# Gamification for android & ios platform

This package provide integration with gamification provided by The Logical Banya.

## Installation

You can install this package using npm:

```bash
npm install gamification-react-native
```
if getting any error install this package using npm:

```bash
npm install gamification-react-native react-native-webview react-native-orientation-locker --force
```

## install pod for ios

```bash
pod install
```

## Usage

1.create new page and import Gamification package & pass props.<br>

```react-native
import GamificationReactNative from "gamification-react-native";
import {useState} from "react";
import {Button} from "react-native";

export default (() => {
    const [open, setOpen] = useState(false);
    const baseUrl = "";
    const clientID = "";
    const clientKey = "";
    const userID = "";
    const username = "";
    const keyString = "";
    return (<>
        {open ?
            <GamificationReactNative
                baseUrl={baseUrl}
                clientID={clientID}
                clientKey={clientKey}
                userID={userID}
                username={username}
                keyString={keyString}
                onClose={() => setOpen(false)}/> :
            <Button title={'open'}
                    onPress={() => setOpen(true)}/>
        }

    </>);
})
```

```bash
Required parameters

baseUrl: "",
clientID: "",
key: "",
userID: "",
username: "",
keyString: "",

Take above parameters from provider.
```
*Note: for ios  <GamificationReactNative/> wrap in SafeAreaView for rendering.

also you can pass another optional props <br>
    1.utm_param1 <br>
    2.utm_param2 <br>
    3.utm_param3 <br>
    4.utm_param4 <br>
