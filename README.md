# Chart Pie:
- Referência: [react-native-pie](https://github.com/nihgwu/react-native-pie#readme)

- Instalar dependencia:

```bash
yarn add react-native-pie
```

- Instalar essa outra também:

```bash
yarn add @react-native-community/art
```

- Na pasta `ios/` executar o comando:

```bash
pod install
```

- Criar o arquivo `src/App.js`:

```js
import React from 'react';
import {StyleSheet, View, Text} from 'react-native';
import Pie from 'react-native-pie';

const styles = StyleSheet.create({
  container: {
    backgroundColor: '#00ffff',
    alignItems: 'center',
    justifyContent: 'center',
    height: 300,
  },
  v: {
    backgroundColor: '#00ffff',
    height: 100,
    width: 100,
    position: 'absolute',
    alignItems: 'center',
    justifyContent: 'center',
  },
});

export default () => {
  return (
    <View style={styles.container}>
      <Pie
        backgroundColor="#00ffff"
        radius={90}
        innerRadius={70}
        sections={[
          {
            percentage: 10,
            color: '#C70039',
          },
          {
            percentage: 20,
            color: '#44CD40',
          },
          {
            percentage: 30,
            color: '#404FCD',
          },
          {
            percentage: 40,
            color: '#EBD22F',
          },
        ]}
        dividerSize={0}
        strokeCap={'round'}
      />
      <View style={styles.v}>
        <Text>A</Text>
      </View>
    </View>
  );
};

```

- No arquivo `./index.js` alterar:

```js
import App from './src/App';
```