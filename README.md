# react-native-view-scaleable

### The one of the missing piece of react-native.
### Highly performant view transformation with gestures ✋.
### This library makes ANY views editable using gestures like pinch, double tap or pull. You can scale/rotate/move any view

### Getting Started
```sh
$ npm install react-native-view-scaleable --save
```
or
```sh
$ yarn add react-native-view-scaleable
```

### Usage
```javascript
/**
 * @flow
 */

import React, { Component } from 'react';
import {
  AppRegistry,
  StyleSheet,
  Text,
  View
} from 'react-native';

import { ViewEditor } from 'react-native-view-scaleable';

export default class App extends Component {
  render() {
    return (
        <ViewEditor
          style={styles.container}
          scaleBounds={{ min: 1, max: 10 }}
          onMove={() => console.log('move')}
          onMoveEnd={() => console.log('move end')}
        >
            <View>
                <Text style={styles.welcome}>
                    Welcome to React Native!
                </Text>
                <Text style={styles.instructions}>
	            To get started, edit index.ios.js
	            </Text>
	            <Text style={styles.instructions}>
	            Press Cmd+R to reload,{'\n'}
	            Cmd+D or shake for dev menu
	            </Text>
            </View>
        </ViewEditor>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  welcome: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
  instructions: {
    textAlign: 'center',
    color: '#333333',
    marginBottom: 5,
  },
});

AppRegistry.registerComponent('App', () => App);
```
