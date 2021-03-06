Adds [`svg-react-loader`][loader] to gatsby webpack config (and removes `svg`s from the built-in `url-loader` config).

The `rule` plugin option can be used to pass [rule options](https://webpack.js.org/configuration/module/#rule). If either `include` or `exclude` options are present, `svg-react-loader` will use them and `url-loader` will be reenabled with the inverse.

The following uses `svg-react-loader` to process svgs from a path matching `/assets/`, and `url-loader` to process svgs from everywhere else.

```js
{
    resolve: 'gatsby-plugin-react-svg',
    options: {
        rule: {
          include: /assets/
        }
    }
}
```

[loader]: https://github.com/jhamlet/svg-react-loader

From now on you can import SVGs and add them as Components:


```js
import Icon from './path/icon.svg';

// ...

<Icon />
```
