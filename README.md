# Frontend

## Architechture

### Goals

1. Comprehensible - Understanding the codebase should be easy
1. Flexible - Easy to iterate
1. Stable - Fail as soon as possible (compile time, boot)
1. Testable - UI and Behaviors
1. Extendable - Adding new features should be simple

### Diagram

![architechture](https://raw.githubusercontent.com/jaune/frontend/main/architechture.png)

- [components](./components.md)

## Principles

1. [KISS](https://en.wikipedia.org/wiki/KISS_principle)
1. [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
1. [SOLID](https://en.wikipedia.org/wiki/SOLID)
1. [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)

## Tech

### Build system
- [TypeScript](https://www.typescriptlang.org/)
- [Webpack](https://webpack.js.org/)
  - [code-splitting](https://webpack.js.org/guides/code-splitting/)
  - [svgr](https://react-svgr.com/docs/webpack/)

### UI
- [React](https://reactjs.org/)
  - [SSR](https://fr.reactjs.org/docs/react-dom-server.html)
- [CSS Modules](https://github.com/css-modules/css-modules)
- [SCSS](https://sass-lang.com/)

### Linter / Format
- [prettier](https://prettier.io/)
- [eslint](https://eslint.org/)
- [stylelint](https://stylelint.io/)

### Advenced web
- [PWA](https://fr.wikipedia.org/wiki/Progressive_web_app)

### Observability
- [OpenTelemetry](https://opentelemetry.io/docs/concepts/data-sources/)
- [analytics](https://getanalytics.io/)
- [Perfume.js](https://zizzamia.github.io/perfume/)

## Resources

1. [ISO/IEC 9126](https://en.wikipedia.org/wiki/ISO/IEC_9126)
