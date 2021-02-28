# Components

### Simplest component

```
src/components/
  - MyComponent.tsx
```

```tsx
// MyComponent.tsx
import React from 'react'

const MyComponent = () => (
  // ...
)
```

### Component with Style

```
src/components/MyComponent/
  - index.tsx
  - style.scss
```

```tsx
// index.tsx
import React from 'react'

import scss from './style.scss'

const MyComponent = () => <buton className={scss.button} />
```

### Component using images

```
src/components/MyComponent/
  - index.tsx
  - images/
    - logo.png
```

```tsx
// index.tsx
import React from 'react'

import logoImage from './images/logo.png'

const MyComponent = () => <img src={logoImage} />
```

### Component using global hooks

```
src/
  - hooks/
    - useMyHook.ts
  - components/
    - MyComponent.tsx
```

```tsx
// index.tsx
import React from 'react'

import useMyHook from 'src/hooks/useMyHook'

const MyComponent = () => {
  useMyHook()

  // ...
}
```

### Component using local hooks

`useMyHook` can only used by `MyComponent`

```
src/components/MyComponent/
  - index.tsx
  - hooks/
    - useMyHook.ts
```

```tsx
// index.tsx
import React from 'react'

import useMyHook from './hooks/useMyHook'

const MyComponent = () => {
  useMyHook()

  // ...
}
```

### Sub-Component

`MySubComponent` can only used by `MyComponent`

```
src/components/MyComponent/
  - index.tsx
  - components/
    - Button.tsx
```

```tsx
// index.tsx
import React from 'react'

import MySubComponent from './components/MySubComponent'

const MyComponent = () => <MySubComponent />
```

```tsx
// components/MySubComponent.tsx
import React from 'react'

const MySubComponent = () => (
  // ...
)
```

### Controlled Component

Like form's components (`<input />`, `<select />`, etc.), custom components can use the [Controlled Component](https://reactjs.org/docs/forms.html#controlled-components) pattern.

```
src/components/MyComponent/
  - index.tsx
```

```tsx
// index.tsx
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

### Component decoupling

`MyValue` must be define by `MyComponentView`, to avoid coupling between `MyComponentView` and `MyComponent`. Testing `MyComponentView` become super easy.

```
src/components/MyComponent/
  - index.tsx
  - view.tsx
```

```tsx
// index.tsx
import React from 'react'

const MyComponent = () => (
  // ...
)
```

```tsx
// view.tsx
import React from 'react'

interface MyValue {
  // ...
}

interface Props {
  value: MyValue
}

const MyComponentView = ({ value }: Props) => (
  // ...
)
```
