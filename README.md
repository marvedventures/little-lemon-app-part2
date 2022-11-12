# React Native (Meta) Exercise

This is a solution to the React Native Exercise by Meta.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:  

- Create a React Native App using Expo
- Use View, Text, and FlatList Components
- Create a Header Component
- Create a Footer Component  
- Create a component to display menu items and use FlatList
- Update Styles of Components to match Scenario
- Extract All Styles to StyleSheet API 
- Render Components to the App Component

### Screenshot

![image](https://user-images.githubusercontent.com/108392678/201472990-50305996-32e6-4d2d-bc82-2412ab849ebd.png)
![image](https://user-images.githubusercontent.com/108392678/201473000-4f7b1dca-a06a-4576-a361-42915a72d5f9.png)


### Links

- Solution URL: [Code](https://github.com/marvedventures/little-lemon-app-part2)

## My process

### Built with
- [React Native](https://reactnative.dev/docs/environment-setup) - React Native using Expo Go
- [StyleSheet](https://reactnative.dev/docs/stylesheet) - For styles

### What I learned

Creating React Native components, Views, Text and FlatList Components.  Using StyleSheet API to style a React Native App.

Here is a code snippet: 


```jsx
import * as React from 'react';
import { View, Text, StyleSheet, FlatList } from 'react-native';

const menuItemsToDisplay = [
  { name: 'Hummus', price: '$5.00', id: '1A' },
  { name: 'Moutabal', price: '$5.00', id: '2B' },
  ...
];

const Item = ({ name, price }) => (
  <View style={menuStyles.innerContainer}>
    <Text style={menuStyles.itemText}>{name}</Text>
    <Text style={menuStyles.itemText}>{price}</Text>
  </View>
);

const MenuItems = () => {
  const renderItem = ({ item }) => <Item name={item.name} price={item.price} />;

  return (
    <View style={menuStyles.container}>
      <FlatList
        data={menuItemsToDisplay}
        renderItem={renderItem}
        keyExtractor={(item) => item.id}></FlatList>
    </View>
  );
};

const menuStyles = StyleSheet.create({
  container: {
    flex: 1
  },
  ...
});
```

### Useful resources

- [React Native Docs](https://reactnative.dev/docs/stylesheet) - This helped me for all the neccessary React Native styles. I really liked their documentation and will use it going forward.


## Author

- Website - [Marvin Morales Pacis](https://marvin-morales-pacis.vercel.app/)
- LinkedIn - [@marvedventures](https://www.linkedin.com/in/marvedventures/)
- Twitter - [@marvedventures](https://www.twitter.com/marvedventures)
