# Frontend

Jaune's Book.

## Articles

- [Why dependencies matter?](articles/dependencies/readme.md)


## Ideas

- [configuration](ideas/configuration.md)
- [logger](ideas/logger.md)


## Principles

- [KISS](https://en.wikipedia.org/wiki/KISS_principle) - Keep It Simple, Stupid!
- [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) - Don't Repeat Yourself
- [SOLID](https://en.wikipedia.org/wiki/SOLID)
- [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it) - You aren't gonna need it
- best practices should be the easiest way
- [The Early Days of Id Software: Programming Principles](./videos.md)
- [Agile Principles](https://agilemanifesto.org/iso/en/principles.html)
- [Fail-fast](https://en.wikipedia.org/wiki/Fail-fast), [Fail-safe](https://en.wikipedia.org/wiki/Fail-safe) and [Fail Gracefully](https://en.wikipedia.org/wiki/Fault_tolerance#Terminology)

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
- [npm](https://www.npmjs.com/) - install recursively packages using dependencies discribe in the `package.json`
- [TypeScript](https://www.typescriptlang.org/) - JavaScript but typed
- [Webpack](https://webpack.js.org/) - bundle your application, using modules' dependencies, everything is be a module
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

#### Code Testing
- [tap](https://node-tap.org/)
- [ava](https://github.com/avajs/ava)

#### Visual Testing
- [cosmos](https://github.com/react-cosmos)
- [playwright](https://github.com/microsoft/playwright)
- [percy](https://percy.io/)

### Analysis
- [lighthouse](https://developers.google.com/web/tools/lighthouse)

### Linter / Format
- [prettier](https://prettier.io/)
- [eslint](https://eslint.org/)
- [stylelint](https://stylelint.io/)
- [.editorconfig](https://editorconfig.org/)

### Advanced Features
- Offline
  - [Offline Event](https://developer.mozilla.org/en-US/docs/Web/API/Window/offline_event)
  - [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)
  - [IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API/Using_IndexedDB)

- [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
- [PWA](https://fr.wikipedia.org/wiki/Progressive_web_app)
  - [Notifications](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API/Using_the_Notifications_API)
  - [Payment](https://developer.mozilla.org/en-US/docs/Web/API/Payment_Request_API)
  - [Authentication](https://developer.mozilla.org/en-US/docs/Web/API/Web_Authentication_API)

### i18n & l10n

ICU, extract strings

 - [globalize](https://github.com/globalizejs/globalize)
 - [messageformat](https://messageformat.github.io/messageformat/)
 - [i18next](https://react.i18next.com/misc/using-with-icu-format)

### Observability
- [OpenTelemetry](https://opentelemetry.io/docs/concepts/data-sources/)
- [analytics](https://getanalytics.io/)
- [Perfume.js](https://zizzamia.github.io/perfume/)

### Time / Date
- [Temporal](https://github.com/tc39/proposal-temporal)
- [Luxon](https://moment.github.io/luxon/)

## Resources

1. [ISO/IEC 9126](https://en.wikipedia.org/wiki/ISO/IEC_9126)
