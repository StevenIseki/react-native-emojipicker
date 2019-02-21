# react-native-emojipicker

[![npm version](https://badge.fury.io/js/react-native-emojipicker.svg)](https://badge.fury.io/js/react-native-emojipicker)

![](https://raw.githubusercontent.com/StevenIseki/react-native-emojipicker/master/screenshot.gif)

react-native-emojipicker is a simple emoji picker component

## Install

`yarn add react-native-emojipicker`

## Usage

```jsx
import React from 'react'
import { ScrollView, View, Text, TouchableOpacity } from 'react-native'
import EmojiPicker from '../components/Picker'

export default class extends React.Component {
  constructor (props) {
    super(props)
    this.state = { visible: true }
  }

  logEmoji (emoji) {
    console.log(emoji)
  }

  render() {
    return (
      <ScrollView>
        <EmojiPicker
          onEmojiSelected={this.logEmoji.bind(this)}
          visible={this.state.visible}
          />
          <TouchableOpacity
            onPress={() => {this.setState({visible: !this.state.visible})}}>
            <Text>show / hide</Text>
          </TouchableOpacity>
      </ScrollView>
    )
  }
}
```

## Props

#### `onEmojiSelected` (required)
Handler returns the unicode emoji character ⚽️ selected from the emoji picker.

#### `visible`
Opacity to show or hide the picker. Defaults to `true`.

## Styles
Uses styled-components 💅 for the base styling.

## Development
    yarn
    npm run dev

## Build
    yarn
    npm run build
    npm login
    npm version patch
    git add -A
    git push origin master
    npm publish

## License

[MIT](http://isekivacenz.mit-license.org/)
