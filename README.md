
# react-native-wido-progress-bar

## Getting started

`$ npm install react-native-wido-progress-bar --save`

### Mostly automatic installation

`$ react-native link react-native-wido-progress-bar`

### Manual installation


#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-wido-progress-bar` and add `RNWidoProgressBar.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNWidoProgressBar.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.reactlibrary.RNWidoProgressBarPackage;` to the imports at the top of the file
  - Add `new RNWidoProgressBarPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-wido-progress-bar'
  	project(':react-native-wido-progress-bar').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-wido-progress-bar/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-wido-progress-bar')
  	```

#### Windows
[Read it! :D](https://github.com/ReactWindows/react-native)

1. In Visual Studio add the `RNWidoProgressBar.sln` in `node_modules/react-native-wido-progress-bar/windows/RNWidoProgressBar.sln` folder to their solution, reference from their app.
2. Open up your `MainPage.cs` app
  - Add `using Wido.Progress.Bar.RNWidoProgressBar;` to the usings at the top of the file
  - Add `new RNWidoProgressBarPackage()` to the `List<IReactPackage>` returned by the `Packages` method


## Usage
```javascript
import RNWidoProgressBar from 'react-native-wido-progress-bar';

// TODO: What to do with the module?
RNWidoProgressBar;
```
  