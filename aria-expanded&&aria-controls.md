Let's explore the `aria-expanded` and `aria-controls` attributes.

### `aria-expanded`

The `aria-expanded` attribute is used to indicate the current state of a collapsible element or widget, such as a menu or tree. It informs assistive technologies whether the element is expanded or collapsed.

#### Example:

```html
<button aria-expanded="true" aria-controls="menu">
  Expand Menu
</button>
<div id="menu" aria-hidden="false">
  <!-- Menu content goes here -->
</div>
```

In this example, `aria-expanded="true"` indicates that the menu is expanded, and the associated content is visible. The `aria-controls` attribute references the ID of the controlled element.

#### Values:

- **`"true"`:** Indicates that the element is expanded or open.

- **`"false"`:** Indicates that the element is collapsed or closed.

### `aria-controls`

The `aria-controls` attribute is used to associate an element with the IDs of elements it controls. It indicates that the listed elements are the controlled elements of the current element.

#### Example:

```html
<button aria-expanded="true" aria-controls="section-content">
  Show Content
</button>
<div id="section-content" aria-hidden="false">
  <!-- Content goes here -->
</div>
```

In this example, `aria-controls="section-content"` associates the button with the content it controls, providing context to assistive technologies.

#### Best Practices:

1. Use `aria-expanded` with `aria-controls` for elements that can be expanded or collapsed.

2. Ensure that the values of `aria-expanded` accurately reflect the current state of the element.

3. Use `aria-controls` to create associations between interactive elements and the elements they control.

### Use Case:

Consider an accordion component where clicking a button expands or collapses a section:

```html
<button aria-expanded="true" aria-controls="section1">
  Section 1
</button>
<div id="section1" aria-hidden="false">
  <!-- Content for Section 1 goes here -->
</div>
```

This provides screen readers with information about the current state and controlled elements, enhancing the user experience for those relying on assistive technologies.