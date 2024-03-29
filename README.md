# react-native-wido-progress-bar

An animated progress bar for React Native.

## Getting started

1. `npm install react-native-wido-progress-bar@latest --save`

## Example usage

```javascript
var React = require('react-native');
var {
  AppRegistry,
  StyleSheet,
  Text,
  View,
} = React;
var RNWidoProgressBar = require('react-native-wido-progress-bar');

var rnsandbox = React.createClass({

  getInitialState() {
    return {
      progress: 0
    };
  },

  render() {

    setTimeout((function() {
      this.setState({ progress: this.state.progress + (0.4 * Math.random())});
    }).bind(this), 1000);

    return (
      <View style={styles.container}>
        <Text style={styles.welcome}>
          Welcome to React Native!
        </Text>
        <Text style={styles.instructions}>
          To get started, edit index.ios.js
        </Text>
        <Text style={styles.instructions}>
          Press Cmd+R to reload,{'\n'}
          Cmd+Control+Z for dev menu
        </Text>
        <RNWidoProgressBar
          fillStyle={{}}
          backgroundStyle={{backgroundColor: '#cccccc', borderRadius: 2}}
          style={{marginTop: 10, width: 300}}
          progress={this.state.progress}
        />
      </View>
    );
  }
});

var styles = StyleSheet.create({
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

AppRegistry.registerComponent('rnsandbox', () => rnsandbox);

```

## Properties

| Prop | Description | Default |
|---|---|---|
|**`progress`**|The progress value for the progress bar. Ranges from `0..1`.|None|
|**`easingDuration`**|The time taken to complete the animation in milliseconds.|`500`|
|**`easing`**|Function from [`Easing`](https://github.com/facebook/react-native/blob/master/Libraries/Animation/Animated/Easing.js).|`Easing.inOut(Easing.ease)`|
|**`fillStyle`**|The style for the progress bar fill.|None|
|**`backgroundStyle `**|The style for the progress bar's background.|None|
|**`style `**|The style for the entire component. This doesn't really differ from the `backgroundStyle` property. You must set width either here or in `backgroundStyle` in order to make sure the component works properly.|See [`RNWidoProgressBar.js`]|


## Component methods
| Method | Description |
|---|---|
| **`update(progress)`** | The recommended way to update the progress of the progress bar is to use the `progress` property. If you prefer, you can use this `update` method to update the progress directly. To access this method, set the `ref` property on the `<RNWidoProgressBar>` and call `this.refs.RNWidoProgressBarName.update(0.3)` |