# react-native-disable-battery-optimizations

## Getting started

`$ npm install react-native-disable-battery-optimizations --save`

### Mostly automatic installation

`$ react-native link react-native-disable-battery-optimizations`

### Manual installation



#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.reactlibrary.RNDisableBatteryOptimizationsPackage;` to the imports at the top of the file
  - Add `new RNDisableBatteryOptimizationsPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-disable-battery-optimizations'
  	project(':react-native-disable-battery-optimizations').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-disable-battery-optimizations/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-disable-battery-optimizations')
  	```

## Usage
```javascript
import RNDisableBatteryOptimizations from 'react-native-disable-battery-optimizations';

RNDisableBatteryOptimizations.isBatteryOptimizationEnabled().then((isEnabled)=>{
	if(isEnabled){
		RNDisableBatteryOptimizations.openBatteryModal();
	}
});

RNDisableBatteryOptimizations;
```
  