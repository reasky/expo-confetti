
# Expo-confetti

Animated star rating component for React Native (Expo). Compatible with iOS, Android.
Written in JavaScript.

![Alt Text](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM28ydXl1a3Nub2FoZHp3N2VhMG5zc2prZGdtd2VpY2h4c3hpbDEyNiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/6JVuTslAjabsrjWSWT/giphy.gif)


# Expo-confetti

Animated star rating component for React Native (Expo). Compatible with iOS, Android.
Written in JavaScript.

## Installation

Install expo-confetti:

```bash
  yarn add expo-confetti / npm install expo-confetti
```
Your `babel.config.js` should be: 

```bash
  module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: [
        [
            'react-native-reanimated/plugin', {
                relativeSourceLocation: true,
            },
        ]
    ],
  };
};

```


## Usage

```javascript
import React, { useState } from "react";
import ConfettiCanvas, { startAnimation } from "expo-confetti";

export default function App() {
  const [confettiPieces, setConfettiPieces] = useState([]);

  const handleStartAnimation = () => {
    startAnimation(setConfettiPieces);
  };

  return (
    <View style={styles.container}>
      <ConfettiCanvas confettiPieces={confettiPieces} />
      <View style={styles.containerButton}>
        <TouchableOpacity onPress={handleStartAnimation}>
          <Text>Click for start animation</Text>
        </TouchableOpacity>
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    height: "100%",
    backgroundColor: "white",
  },
  containerButton: {
    alignItems: "center",
    marginTop: 200
  }
});

```


## Props

| Name | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `confettiPieces` | `array` | **Required**.|


## Authors

- [@reaskydev](https://www.github.com/reaskydev)


## Feedback

**Telegram:** [t.me/dev_nikita](https://t.me/dev_nikita) \
**VKontakte**: [vk.com/reasky](https://vk.com/reasky)

