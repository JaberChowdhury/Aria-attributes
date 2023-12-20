Let's explore the `aria-disabled` attribute.

### `aria-disabled`

The `aria-disabled` attribute is used to indicate whether an element is currently disabled or not interactive. It communicates to assistive technologies that the element cannot be activated or selected.

#### Example:

```html
<button aria-disabled="true">
  Submit (Disabled)
</button>
```

In this example, the button is disabled (`aria-disabled="true"`), indicating that it cannot be interacted with or activated.

#### Values:

- **`"true"`:** Indicates that the element is disabled.

- **`"false"` or not present:** Indicates that the element is enabled.

#### Best Practices:

1. Use `aria-disabled` to inform users of assistive technologies when an element is not interactive or is temporarily unavailable.

2. When an element is disabled, its associated functionality (e.g., click events) should also be disabled.

### Use Case:

Consider a form with a submit button that should be disabled until all required fields are filled:

```html
<button aria-disabled="true" id="submit-button" disabled>
  Submit
</button>
```

In this case, the button is initially disabled, and JavaScript can dynamically enable it when all required form fields are filled, while updating `aria-disabled` accordingly. This provides an accessible indication of the button's current state.