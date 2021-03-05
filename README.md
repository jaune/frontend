# Frontend

## Architechture

### Goals

1. Comprehensible - Understanding the codebase should be easy
1. Explicit - Reduce ambiguity and black magic
1. Flexible - Easy to iterate
1. Stable - Fail as soon as possible (compile time, boot)
1. Testable - UI and Behaviors
1. Extendable - Adding new features should be simple

### Diagram

![architechture](https://raw.githubusercontent.com/jaune/frontend/main/architechture.png)

- [components](./components.md)

## Principles

1. [KISS](https://en.wikipedia.org/wiki/KISS_principle) - Keep It Simple, Stupid!
1. [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) - Don't Repeat Yourself
1. [SOLID](https://en.wikipedia.org/wiki/SOLID)
1. [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it) - You aren't gonna need it

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
- .nvmrc - Switch node environment [nvm](https://github.com/nvm-sh/nvm) [nvs](https://github.com/jasongin/nvs)
- [engineslist](https://github.com/muuvmuuv/engineslist) - Check node environment

### Versioning
- [Semantic Versioning](https://semver.org/)
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

### Observability
- [OpenTelemetry](https://opentelemetry.io/docs/concepts/data-sources/)
- [analytics](https://getanalytics.io/)
- [Perfume.js](https://zizzamia.github.io/perfume/)

## Resources

1. [ISO/IEC 9126](https://en.wikipedia.org/wiki/ISO/IEC_9126)
