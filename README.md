
# Using Filters and Color Adjustments with CSS

This guide will show you how to use CSS filters to adjust colors of elements, and how to apply direct RGB color changes using CSS.

## 1. Using CSS Filters

The `filter` property in CSS can manipulate colors and visuals of an element. It works well for images or icons and provides a way to adjust colors dynamically using different functions such as:

- **invert()**: Inverts the colors of the element.
- **sepia()**: Adds a brownish tone to the element.
- **saturate()**: Increases or decreases the saturation of the colors.
- **hue-rotate()**: Rotates the color spectrum of the element.
- **brightness()**: Adjusts the brightness of the element.
- **contrast()**: Adjusts the contrast of the element.

### Example CSS Filter:
```css
.icon {
  filter: invert(28%) sepia(98%) saturate(745%) hue-rotate(82deg) brightness(95%) contrast(87%);
}
```
This example uses a combination of filter functions to adjust the colors of the `.icon` element. You can modify the percentages or values to achieve different color effects.

## 2. Changing SVG Icon Colors with Hover

If you're working with SVG icons, you can directly manipulate their color with the `fill` property. Here's an example that changes the color of an SVG icon when hovered:

```css
.icon {
  fill: red; /* Initial color */
  transition: fill 0.3s ease;
}

.icon:hover {
  fill: green; /* Color on hover */
}
```

This CSS will make the icon red initially, and when you hover over it, it will turn green.

## 3. Limitations of Filters with RGB Colors

Although `filter` provides useful functionality for color manipulation, it is not directly compatible with RGB color values. You can't specify a precise RGB value like `rgb(255, 0, 0)` using `filter`. The filter methods are more abstract and manipulate the color range.

### Workaround: Using Filters and Experimentation

You can experiment with filter properties like `hue-rotate()` and `saturate()` to approximate a color shift, but it will not be as exact as using RGB values. You would need to adjust filter values to visually match the color you're aiming for.

## Conclusion

If you need precise control over colors, using SVG icons or directly applying background colors or `fill` properties will give you better results. Filters are useful for visual effects but are limited in terms of exact color control.

For detailed and precise color manipulation, it's best to work with vector-based images like SVGs or standard HTML elements where you can directly specify colors.
