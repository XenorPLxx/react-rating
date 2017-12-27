# React Rating

React Rating is a [react](https://github.com/facebook/react) rating component which supports custom symbols both with [inline styles](https://facebook.github.io/react/tips/inline-styles.html) and glyphicons found in popular CSS Toolkits like [Fontawesome](http://fortawesome.github.io/Font-Awesome/icons/) or [Bootstrap](http://getbootstrap.com/components/).

I intend to port the jQuery [bootstrap-rating](https://github.com/dreyescat/bootstrap-rating) to a React component.

## Demo

See [react-rating](http://dreyescat.github.io/react-rating/) in action.

## Installation

You can install `react-rating` component using the *npm* package manager:

```bash
npm install --save react-rating
```

### Dependencies

The `react-rating` component [peer depends](https://docs.npmjs.com/files/package.json#peerdependencies) on the [React](http://facebook.github.io/react/) library.

You can install React using *npm* too:

```bash
npm install --save react
```

## Usage

1. Require the Rating Component

    ```javascript
    var Rating = require('react-rating');
    ```

2. Start using it

    With raw javascript:

    ```javascript
    React.createElement(Rating)
    ```

    Or with JSX:

    ```jsx
    <Rating />
    ```

## Properties

Property          | Type                                           | Default              | Description
---               | ---                                            | ---                  | ---
`start`           | *number*                                       | 0                    | Range starting value (exclusive).
`stop`            | *number*                                       | 5                    | Range stop value (inclusive).
`step`            | *number*                                       | 1                    | Describes how many values each Symbol represents. For example, for a `start` value of 0, a `stop` value of 10 and a `step` of 2, we will end up with 5 Symbols, with each Symbol representing value increments of 2.
`fractions`       | *number*                                       | 1                    | Number of equal subdivisions that can be selected as a rating in each Symbol. For example, for a `fractions` value of 2, you will be able to select a rating with a precision of down to half a Symbol.
`initialRating`   | *number*                                   | 0                    | The value that will be used as an initial rating.
`placeholderRating`   | *number*                                   | 0                    | If you do not define an `initialRating` value, you can use a placeholder rating. Visually, this will have the same result as if you had defined an `initialRating` value. If `initialRating` is set `placeholderRating` is not taken into account 
`readonly`        | *bool*                                         | false                | Whether the rating can be modified or not.
`quiet`           | *bool*                                         | false                | Whether to animate rate hovering or not.
`direction`       | *ltr* or *rtl*                                 | ltr                  | The direction of the rating element contents
`emptySymbol`     | *element* or *object* or *string* or *array*   | Style.empty          | React element, inline style object, or classes applied to the rating symbols when empty. Can also be an array of such symbols that will be applied in a circular manner (round-robin).
`fullSymbol`      | *element* or *object* or *string* or *array*   | Style.full           | React element, inline style object, or classes applied to the rating symbols when full. Can also be an array of such symbols that will be applied in a circular manner (round-robin).
`placeholderSymbol`      | *element* or *object* or *string* or *array*   | Style.placeholder           | React element, inline style object, or classes applied to the placeholder rating symbols. Can also be an array of such symbols that will be applied in a circular manner (round-robin).

## Callbacks

Callback      | Type                           | Description
---           | ---                            | ---
`onChange`    | function (value) {}            | Gets called with the `value` when you click on a different value than the currently set one.
`onHover`     | function (value) {}            | Gets called with the `value` when you hover over a symbol. The value is equal to the value that corresponds to that part of the symbol. Gets called in `quiet` mode too.

## License

[MIT License](https://github.com/dreyescat/react-rating/blob/master/LICENSE.md)
