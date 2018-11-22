# react-native-checklist
Todo points to consider while developing react-native app

### Styles

 - #### hairlineWidth
Use [hairlineWidth](https://facebook.github.io/react-native/docs/stylesheet#hairlinewidth) instead of constant value for border or divider.

    var styles = StyleSheet.create({
      separator: {
        borderBottomColor: '#bbb',
        borderBottomWidth: StyleSheet.hairlineWidth,
      },
    });

This constant will always be a round number of pixels (so a line defined by it can look crisp) and will try to match the standard width of a thin line on the underlying platform. However, you should not rely on it being a constant size, because on different platforms and screen densities its value may be calculated differently.

A line with hairline width may not be visible if your simulator is downscaled.
