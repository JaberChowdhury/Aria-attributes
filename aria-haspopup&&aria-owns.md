
### `aria-haspopup`

The `aria-haspopup` attribute is used to indicate that an element has a popup context menu or sub-level menu. It signals to assistive technologies that activating the element may display additional options.

#### Example:

```html
<button aria-haspopup="true" aria-owns="submenu">
  Open Menu
</button>
<div id="submenu">
  <!-- Submenu content goes here -->
</div>
```

In this example, `aria-haspopup="true"` indicates that activating the button may reveal a submenu, and `aria-owns` associates the button with the ID of the submenu.

### `aria-owns`

The `aria-owns` attribute is used to associate an element with the IDs of elements that it owns or controls. It indicates that the listed elements are subordinate elements controlled by the current element.

#### Example:

```html
<div aria-owns="tooltip">
  Hover for more info
</div>
<div id="tooltip">
  <!-- Tooltip content goes here -->
</div>
```

In this example, the first `<div>` owns the tooltip with the ID "tooltip," conveying the relationship between the two elements.

#### Best Practices:

1. Use `aria-haspopup` to indicate elements that trigger popups or submenus.

2. Use `aria-owns` to create associations between interactive elements and the elements they own or control.

3. Ensure that the values of `aria-owns` are the IDs of elements that are indeed controlled by the current element.

### Use Case:

Imagine a navigation bar with dropdown menus. The parent menu button can use `aria-haspopup` to indicate that it has a submenu, and `aria-owns` can associate it with the actual submenu:

```html
<button aria-haspopup="true" aria-owns="dropdown-menu">
  Products
</button>
<div id="dropdown-menu">
  <!-- Submenu content for Products goes here -->
</div>
```

This provides additional information to users of assistive technologies about the presence of a submenu and its association with the parent button.