# react-native

* Author's repo: https://github.com/StephenGrider/redux-code
* https://app.diagrams.net/#Hnuthanc%2Frn-casts%2Fmaster%2Fdiagrams%2F07%2Fdiagrams.xml
### Overview

* Write code
  * Test on a physical device: Easiest to setup
  * Test on a fake device: Changes to code show up faster

### App Setup

```sh
cd rn-starter
npm install
npm start
```
* Install **expo** on your phone from Google Play Store
* Scan the QR code from the React Native Bundler on your phone
* If **LAN connection doesn't work, switch to Tunnel** and scan again 
* Add ComponentsScreen file
* 4 things to do in a Component
  * Import libraries required to create a Component
  * Create a Component: a function that returns some JSX
  * Create a Stylesheet to style our component
  * Export the Component

### Showing a Custom Component

* In App.js, import and provide ComponentsScreen as an option to createStackNavigator

### Common Question and Answers

![qa](img/qa.png)
* Primitive elements
  * Text
  * View: Element for grouping other elements or stylings
  * Image
  * Button
* StyleSheet.create is not required to create styles, but it is used for additional validation it provides
```js
<Text style={{fontSize: 30}}>Hi There!</Text>

// The below gives a warning instead of big Error as seen from StyleSheet.create
<Text style={{fontsize: 30}}>Hi There!</Text>
```

### Rules of JSX

* We can assemble different JSX elements like normal HTML
  * Use View element to position or group multiple elements within it
* We configure different JSX elements using props
* We can refer to JS variables inside of a JSX block by using curly braces
  * Cannot show JS object inside of Text element
* We can assing JSX elements to a variable, then show that variable inside of a JSX block

### One Common Error

* After return immediately ( or the JSX element not in the next line
* If it's in the next line, it is considered as return; and we get an Error

### JSX Exercise Overview

![ex](img/ex.png)

### Building Lists

* Add ListScreen Component

### The FlatList Element

* Arrays to show as Lists in Mobile
* FlatList Element
* 2 props:
  * data: array of data
  * renderItem: function that will turn each individual item into an element

### Rendering a List

* Use of FlatList component
* It takes 2 props: data and renderItem
* data will take the array as value 
* renderItem will be each element in the Array
  * element will have item and index property
  * So destructure item

### Why a Key Property

* key provides a way for React Native to track lists 
* Without key, if a list item is deleted, React Native will delete every Item on Screen and render again
* With key, it knows which item is deleted and will remove only that element and move certain items if necessay
* This enhances the performance of React Native