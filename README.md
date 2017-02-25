# React Native Boilerplate
React Native + Redux

### 1. Install Step By Step
	
- Install React Native ([Getting Started React Native](https://facebook.github.io/react-native/docs/getting-started.html))
	```
	react-native init ReactNativeBoilerplate
	```
- Install Redux
 	```
	npm install --save react-redux redux
	```
- Create folder `\src` in root folder and create File `App.js`

	```
	/// /src/App.js

	import React, { Component } from 'react';
	import { View, Text } from 'react-native';
	import { Provider } from 'react-redux';
	import { createStore } from 'redux';
	import reducers from './reducers';

	class App extends Component {
		render () {
		    return (
				<Provider store={createStore(reducers)}>
				    <View>
					<Text>
					    Welcome to React Native + Redux ;)
					</Text>
				    </View>
				</Provider>
			);
		}
	}

	export default App;
	```

- Create folder `/src/reducers` and create `index.js`
	```
	/// /src/reducers/index.js

	import { combineReducers } from 'redux';

	export default combineReducers({
		// Reducer Here
		hello: () => []
	});
   	```
- Remove all in `index.ios.js`, `index.android.js` and add
	```
	import {
	  AppRegistry
	} from 'react-native';
	import App from './src/App';

	AppRegistry.registerComponent('ReactNativeBoilerplate', () => App);

	```
