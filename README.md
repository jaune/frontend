# Frontend

Jaune's Book.
## Principles

- [KISS](https://en.wikipedia.org/wiki/KISS_principle) - Keep It Simple, Stupid!
- [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) - Don't Repeat Yourself
- [SOLID](https://en.wikipedia.org/wiki/SOLID)
- [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it) - You aren't gonna need it

## Goals

- Comprehensible
  - code should be easy to understand
  - naming matter
- Explicit
  - no ambiguity nor black magic
  - complexity should be visible
- Flexible
  - easy to iterate
  - adding new features should be simple
  - feature flags
- Stable
  - fail as soon as possible (compile time, boot)
  - fail gracefully
  - failing is not a execption
- Testable
  - code should be testable
  - UI should be testable
  - behaviors should be testable
- Observable
  - log should be easy

## Tech

### Core
- [TypeScript](https://www.typescriptlang.org/) - JavaScript but typed
- [Webpack](https://webpack.js.org/) - Everything is a module
  - [code-splitting](https://webpack.js.org/guides/code-splitting/)
  - [svgr](https://react-svgr.com/docs/webpack/)
- [React](https://reactjs.org/)
  - [SSR](https://fr.reactjs.org/docs/react-dom-server.html) - Server side rendering
  - [Error Boundaries](https://reactjs.org/docs/error-boundaries.html) - Fail gracefully
- [CSS Modules](https://github.com/css-modules/css-modules) - Make CSS modular
- [SCSS](https://sass-lang.com/) - CSS but 'better'

### Environment
- [lerna](https://github.com/lerna/lerna) - Multiple package in on repo
- .nvmrc - Switch node environment ([nvm](https://github.com/nvm-sh/nvm), [nvs](https://github.com/jasongin/nvs))
- [engineslist](https://github.com/muuvmuuv/engineslist) - Check node environment
- [browserslist](https://github.com/browserslist/browserslist) - Check browser environment

### Versioning
- [Semantic Versioning](https://semver.org/) - Versions have meaning
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Conventional Changelog](https://github.com/conventional-changelog/conventional-changelog/)
- [commitlint](https://commitlint.js.org/)
- [husky](https://github.com/typicode/husky)
- [lint-staged](https://github.com/okonet/lint-staged)

### Testing
`No implicit globals` testing frameworks

- [tap](https://node-tap.org/)
- [ava](https://github.com/avajs/ava)

### Linter / Format
- [prettier](https://prettier.io/)
- [eslint](https://eslint.org/)
- [stylelint](https://stylelint.io/)
- [.editorconfig](https://editorconfig.org/)

### Advenced web
- [PWA](https://fr.wikipedia.org/wiki/Progressive_web_app)

### i18n & l10n

ICU, extract strings

 - [globalize](https://github.com/globalizejs/globalize)
 - [messageformat](https://messageformat.github.io/messageformat/)
 - [i18next](https://react.i18next.com/misc/using-with-icu-format)

### Observability
- [OpenTelemetry](https://opentelemetry.io/docs/concepts/data-sources/)
- [analytics](https://getanalytics.io/)
- [Perfume.js](https://zizzamia.github.io/perfume/)

## Architechture

### Diagram

![architechture](https://raw.githubusercontent.com/jaune/frontend/main/architechture.png)

## Resources

1. [ISO/IEC 9126](https://en.wikipedia.org/wiki/ISO/IEC_9126)
