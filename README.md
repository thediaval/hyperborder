# hyperborder-elevated
Customized version of [hyperborder](https://github.com/webmatze/hyperborder) extension

![](hyperborder.png?raw=true)

## Installation
Add it to plugins in your `~/.hyper.js` configuration

````
module.exports = {
  ...
  plugins: ['hyperborder-elevated']
  ...
}
````
then just restart `Hyper` app or go to the menu View > Full Reload

## Configuration
The following settings can be configured by adding a `hyperBorder` section in your `.hyper.js` `config` section:

| Setting              | Type                 | Description                                            | Default Value |
|----------------------|----------------------|--------------------------------------------------------|---------------|
| `borderWidth`        | `string`             | CSS string for how thick the borders should be         | 0px           |
| `adminBorderWidth`   | `string`             | CSS string for how thick the borders for an admin/elevated window.         | 2px           |
| `borderRadiusInner`  | `string`             | CSS string for round inner corners                     | 0px           |
| `borderRadiusOuter`  | `string`             | CSS string for round outer corners                     | 0px           |
| `borderColors`       | `string`, `string[]` | The color(s) for the border                            | ['#fc1da7', '#fba506']          |
| `adminBorderColors`  | `string`, `string[]` | The color(s) for the border for an admin/elevated window. This follows the precedence  of `adminBorderColors` > `borderColors` > defaultColors                                    | Same as `borderColors`           |
| `blurredColors`      | `string`, `string[]` | The color(s) of the borders when the window isn't active | Same as `borderColors`           |
| `blurredAdminColors` | `string`, `string[]` | The color(s) of the borders when the admin/elevated window isn't active. This follows the precedence of `blurredAdminColors` > `blurredColors` > `adminBorderColors` > `borderColors` > defaultColors | Same as `borderColors`           |

### EXAMPLE: Set Border Colors And Width

```javascript
module.exports = {
  config: {
    ...
      hyperBorder: {
        borderColors: ['#fc1da7', '#fba506'],
        borderWidth: '2px',
        adminBorderWidth: '8px'
      }
    ...
  }
}
```

### EXAMPLE: Set Border Colors To Random Colors

In addition, you can set any color value to `'random'` (string value):

```javascript
module.exports = {
  config: {
    ...
      hyperBorder: {
        borderColors: ['random','random'],
        borderWidth: '8px'
      }
    ...
  }
}
```

Then every newly opened `Hyper` terminal window will have a different colored border.

### EXAMPLE: Animate Border Colors

```javascript
module.exports = {
  config: {
    ...
    hyperBorder: {
      animate: true,
      ...
    }
    ...
  }
}
```

To change the speed of animation, specify an object with a `duration` property:

```javascript
module.exports = {
  config: {
    ...
    hyperBorder: {
      animate: {
        duration: '1s',  // default is 16s
      },
      ...
    }
    ...
  }
}
```

### EXAMPLE: Angled Gradients
Because we use CSS3's `linear-gradient`, we're able to specify angles at which to create the radius. Set your own angle like this:

```javascript
module.exports = {
  config: {
    ...
    hyperBorder: {
      borderAngle: '180deg',
      ...
    }
    ...
  }
}
```

## Download Hyper here
https://hyper.is/
