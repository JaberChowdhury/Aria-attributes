### `aria-labelledby`

The `aria-labelledby` attribute is used to associate an element with another element that serves as its label. This is helpful when you have an element without visible text, and you want to provide a label that is visually separate from the element.

#### Example:

```html
<h2 id="sectionTitle">Important Information</h2>
<div aria-labelledby="sectionTitle">
  <!-- Content goes here -->
</div>
```

In this example, the `div` is associated with the `h2` using `aria-labelledby`. Screen readers will announce the content of the `h2` as the label for the `div`.

#### Best Practices:

1. Use `aria-labelledby` when an element needs a label, and the label is provided by another element.

2. The value of `aria-labelledby` should be the ID of the element that serves as the label.

3. Ensure that the labeled-by element is meaningful and descriptive.

4. This is particularly useful when you want to associate a label with a non-interactive element like a `<div>`.