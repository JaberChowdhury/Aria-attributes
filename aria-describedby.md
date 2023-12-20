Let's explore the `aria-describedby` attribute.

### `aria-describedby`

The `aria-describedby` attribute is used to associate an element with descriptive content. This content provides additional information about the element's purpose or usage.

#### Example:

```html
<button aria-describedby="tooltip">Hover for more info</button>
<div id="tooltip">Additional information about the button</div>
```

In this example, the `button` element is associated with the `div` containing additional information. When a screen reader encounters the button, it will announce the content of the associated `div`.

#### Best Practices:

1. Use `aria-describedby` when you want to provide additional information about an element, especially when that information is not suitable for inclusion directly within the element.

2. The value of `aria-describedby` should be the ID of the element containing the descriptive information.

3. Ensure that the descriptive content is meaningful and relevant to the user.

4. This attribute is particularly useful for tooltips or additional context that is not visually presented on the page but is important for users of assistive technologies.

Keep in mind that if the additional information can be presented visually, consider incorporating it directly into the page's layout or using appropriate HTML elements for semantic structure. `aria-describedby` is most beneficial when providing information that is not suitable for visual presentation but is important for accessibility.