# Responsive Webpack Plugin

Generates scss files with responsive mixins based on provided configuration.

It also generates a file that helps syncs media queries with JS

You can easily disable any unneeded breakpoints by setting them to false in wee.json or add more by adding a breakpoint value to this same array.

1. Portrait Mobile (320px)
2. Landscape Mobile (480px)
3. Portrait Tablet (768px)
4. Desktop 1 (1024px)
5. Desktop 2 (1280px)
6. Desktop 3 (1440px)

The mixins use the font family of the HTML element to reference the current breakpoint. For example, the Portrait Mobile breakpoint is triggered when the font family is '2'. When you add/remove default breakpoints, the corresponding font family values will update automatically when the build process is run.

## Usage

```js
new ResponsiveWebpackPlugin({
    breakpoints: {
        mobileLandscape: 480,
        tablet: 768,
        desktop: 1024,
        desktop2: 1280,
        desktop3: 1440,
    },
    offset: 25,

    // Breakpoint offset file generation path
    // relative to the styles source directory
    output: 'temp',
}),
```