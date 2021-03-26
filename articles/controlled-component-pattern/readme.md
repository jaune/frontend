---
  title: Controlled component pattern
  tags: [react, frontend]
---


### Controlled Component

Like input components (`<input />`, `<select />`, etc.), custom components can use the [Controlled Component](https://reactjs.org/docs/forms.html#controlled-components) pattern.

```tsx
import React from 'react'

interface MyValue {
  // ...
}

interface Props {
  value: MyValue
  onChange: (value: MyValue) => void
}

const MyComponent = ({ value, onChange }: Props) => (
  // ...
)
```

`MyValue` must be define by the module `MyComponent` to reduce coupling.

# Resources
- https://reactjs.org/docs/forms.html#controlled-components
- https://reactpatterns.com/#controlled-input
- https://itnext.io/controlled-and-uncontrolled-component-design-pattern-in-react-21e8d40e46e
