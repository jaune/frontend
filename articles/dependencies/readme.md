---
title: Why dependencies matter?
tags: [software engineering, software architecture]
---

# Why dependencies matter?

`Dependency` is one of the more intuitive concept in software engineering.


## What is a dependency?

> A dependency is a unidirectional relationship between two logical entity. A entity depend of another, when incomplete without it.

Abstact definition are the worst. Let's try to be more real: PIZZA 🍕.

![Pizza Photo](./pizza.jpg)

A pizza depends on his ingredients, like Tomato, Cheese, Dough, and, Pineapple?

![Pizza's dependencies](./pizza.svg)

Your scope have to stop somewhere, because Cheese is a really complex and delicous product.

Pizza are great, but let's see somthing less eatable. WWW is based on HTML, we can start by that.

![HTML document's dependencies](./html.svg)

The HTML document depends on images and scripts to be render properly.

Ok, but I write complexe software, not HTML pages.

```typescript
const bar = () => {
  // changing-world code...
}

const foo = () => {
  // complex but super clear code...
  bar()
  // amazing code...
}
```

The array function `foo` depends on `bar` to run properly.


```typescript
const a

open(a)
// ...
close(b)
```

Here `close` depends on `open` to run properly.


### Why dependency is a unidirectional relationship?

`A` **depends** on `B`. We represent the dependency by an solid arrow from `A` to `B`.

![A/B's dependencies](./a-b.svg)

The arrow make the relationship clear, and means:

- `A` depends on `B`
- `A` is aware of `B`
- changing `B` may impact `A`
- `B` is not aware of `A`
- changing `A` does not impact `B`

![A/B circular dependencies](./a-b-circular.svg)

In case of bidirectionnal dependency, you should prefer two arrows, instead of a two-headed arrow, it will make the circular dependency stand out.


### Explicit vs Implicit

It's not that simple, dependency explicity is a spectrum.

Importing a module using `import` in `typescript` is on the `explicity` side of the spectrum.

```typescript
import uniq from 'lodash/uniq'

const foo = () => {
  // complex but super clear code...
  uniq(variable)
  // amazing code...
}
```

The dependency between a CSS class and a button using it is more on the `implicit` side of the spectrum. Espesialy because usually you does not write directly HTML/CSS.

```html
<link href="style.css" rel="stylesheet" />
<!-- ... -->
<button class="button">
  <!-- ... -->
</button>
```

```css
.button {
  /* ... */
}
```

Globals like `Promise` or `window` are probaly on the middle of the explicity spectrum.

The more your dependcies are explicit:

- the less is knowledge based
- the less is ambiguous
- the more can be automated
- the easier errors can be found
- the more can be encapsulate


## Leveraging dependencies

Tech can help you get a lot of value out of you dependencies, here my basic stack.

- [npm](https://www.npmjs.com/) - install recursively packages using dependencies discribe in the `package.json`
- [webpack](https://webpack.js.org/) - bundle your application, using modules' dependencies, everything is be a module
- [TypeScript](https://www.typescriptlang.org/) - JavaScript but typed, with explicit imports
- [CSS Modules](https://github.com/css-modules/css-modules) - Make CSS modular, with 'explicit' imports


### Package

A `package` is a set of modules and a [package.json](https://docs.npmjs.com/cli/v7/configuring-npm/package-json) discribing it. Usually managed via `npm` and distibuted by [https://www.npmjs.com/](npmjs.com). `packages` can be libraries like [lodash](https://www.npmjs.com/package/lodash), executables like [concurrently](https://www.npmjs.com/package/concurrently), etc.
<!-- TODO: find more examples -->


### Module

Browsers use HTTP, HTML, CSS and JS as bluilding blocks of user experiences. Nowadays, frontend engineers don't write directly HTML nor JS, for lot of good reasons.
<!-- TODO: find resources about 'good reasons to not wrote HTML/JS/CSS directly' -->

`webpack` *bundle* your `modules`.

`webpack` will generate browser-friendly files from your files. Where every file is a `module`. Yes, everything, `*.ts`, `*.css`, `*.svg`, `*.png`, `*.json`, `*.yml`, etc. Because the dependencies are explicit `webpack` will only bundle the needed files.
