
## FORK OF 'react-native-navigation'
This package is a fork of wix's 'react-native-navigation' and adds 2 main features missing on the main package on both iOS and Android and 1 Fix on Android :

- Fixes some bugs with the top TitleBar positioning on Android
- Waits for the react component of a screen to mount before pushing the screen on the native side, effectively removing the white flash effect that might e experienced sometimes when pushing a screen.
- Adds the ability to provide a custom react bottom Tab Bar component to the startTabBasedApp(params) method like the following :

```Javascript

Navigation.startTabBasedApp({
  tabs: [
    ...
  ],
  overlay: {
    screen: 'SCREENID',
    passProps: {},
    position: {
      top: 0,
      left: 0,
      width: WIDTH,
      height: HEIGHT,
    }
  }
});
```

If you want to compare the changes to the main wix master repository just use [github's compare tool](https://github.com/wix/react-native-navigation/compare/Odinvt:master) and look through my commits.

For the rest just follow the wix documentation except for android's installation take care of using 'react-native-odinvt-navigation' instead of 'react-native-navigation'

<h1 align="center">
  <img src="./logo.png"/><br>
  React Native Navigation
</h1>

[![NPM Version](https://img.shields.io/npm/v/react-native-navigation.svg?style=flat)](https://www.npmjs.com/package/react-native-navigation)
[![NPM Downloads](https://img.shields.io/npm/dm/react-native-navigation.svg?style=flat)](https://www.npmjs.com/package/react-native-navigation)
[![Build Status](https://travis-ci.org/wix/react-native-navigation.svg?branch=master)](https://travis-ci.org/wix/react-native-navigation)
[![Join us on Discord](https://img.shields.io/badge/discord-react--native--navigation-738bd7.svg?style=flat)](https://discord.gg/DhkZjq2)

## Important
Latest stable version is `1.1.x` and is published to npm under tag `latest`. It supports react-native 0.43 and above.
<br><br>We are currently redesigning and rewriting this project under branch `v2`.
<br>As a result, new features and pull requests on the current stable version will take more time to process.

### tldr;

React Native Navigation provides 100% native platform navigation on both iOS and Android for React Native apps. The JavaScript API is simple and cross-platform - just install it in your app and give your users the native feel they deserve. Using redux? No problem: React Native Navigation comes with optional redux support out of the box. Ready to get started? Check out the [docs](https://wix.github.io/react-native-navigation/).

### Real world examples

<img src="https://github.com/wix/react-native/blob/master/src/videos/demo.gif?raw=true" width="240">&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://github.com/wix/react-native/blob/master/src/videos/rnn-example-demo.gif?raw=true" width="240">

On the left - The Wix app.

On the right - The example app.


## Quick Links
* [Documentation](https://wix.github.io/react-native-navigation/#/)
* [Stack Overflow](http://stackoverflow.com/questions/tagged/react-native-navigation)
* [Chat with us](https://discord.gg/DhkZjq2)
* Bootstrap - If you prefer to learn more about the library and the APIs through code, head over to [the bootstrap example app](https://github.com/wix/react-native-navigation-bootstrap) or the more feature rich [JuneDomingo/movieapp](https://github.com/JuneDomingo/movieapp)
* [v2 - Under Development](https://github.com/wix/react-native-navigation/tree/v2#react-native-navigation-v2-wip)

----

One of the major things missing from React Native core is fully featured native navigation. Navigation includes the entire skeleton of your app with critical components like nav bars, tab bars and side menu drawers.

If you're trying to deliver a user experience that's on par with the best native apps out there, you simply can't compromise on JS-based components trying to fake the real thing.

For example, this package replaces the native [NavigatorIOS](https://facebook.github.io/react-native/docs/navigatorios.html) that has been [abandoned](https://facebook.github.io/react-native/docs/navigator-comparison.html) in favor of JS-based solutions that are easier to maintain. For more details see in-depth discussion [here](https://github.com/wix/react-native-controllers#why-do-we-need-this-package).


## License

The MIT License.

See [LICENSE](LICENSE)
