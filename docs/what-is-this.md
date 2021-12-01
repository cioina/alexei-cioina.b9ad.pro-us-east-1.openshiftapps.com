---
order: 0
title: What Is This?
---

This is an unofficial `ng-zorro-antd` demo website. The main goal is to explore and learn `ng-zorro-antd` components and Angular `^13.0.0`.

> Currently, we use some `ng-zorro-antd` documentation pages for demonstration purpose.

<div class="pic-plus">
  <img alt="Ant Design" width="150" height="150" src="https://img.alicdn.com/tfs/TB1g.mWZAL0gK0jSZFtXXXQCXXa-200-200.svg">
  <span>+</span>
  <img alt="Angular" width="140" height="150" src="https://img.alicdn.com/tfs/TB1Z0PywTtYBeNjy1XdXXXXyVXa-186-200.svg">
</div>

## Static vs Dynamic

The main difference between this website and the [official](https://ng.ant.design/docs/introduce/en) `ng-zorro-antd` is that we don't use Server-side Rendering (SSR). If you are interested in SSR, you may choose:

- [Angular Universal](https://github.com/angular/universal) - a static site generator for Angular
- [Scully](https://github.com/scullyio/scully) - a static site generator for Angular

## Compare Different Tools for Static Content Generation

[Here](https://docs.astro.build/comparing-astro-vs-other-tools/) is a compact comparation bettwen [Astro](https://github.com/snowpackjs/astro) and diffrent tools for static content generation.

## Client-side

The client-side code is written in TypeScript and is compiled with `@angular/cli`.

- Written in TypeScript with complete defined types
- 60+ high-quality`ng-zorro-antd` components out of the box
- Default and dark themes out of the box
- Few dependencens
- Lazy-loading Angular modules
- [Reactive libraries](https://github.com/ngrx/platform) for Angular
- "Headless" website architecture (decoupled architecture)

## Package Dependences

We compile `ng-zorro-antd`and `@ant-design/icons-angular` direct from sources, so folowing are all the additional dependences that our client-site needs

```json
  "dependencies": {
    "@angular/cdk": "^12.2.12",
    "@ctrl/tinycolor": "^3.4.0",
    "@ngrx/effects": "^12.5.1",
    "@ngrx/router-store": "^12.5.1",
    "@ngrx/store": "^12.5.1",
    "date-fns": "^2.25.0",
    "@juggle/resize-observer": "^3.3.1"
  }
```

## Server-side

The server-side code is written in PHP and uses Laravel 8 framework.

- Written in PHP on top of [Laravel framework](https://github.com/laravel/framework)
- JSON Web Token Authentication (JWT) for Laravel
- Cross-Origin Resource Sharing (CORS) for Laravel
- The content for the site is accessible via a RESTful web-service API
- Hosted by [Red Hat OpenShift Online](https://www.openshift.com/products/online/)
- [Source-to-Image](https://docs.openshift.com/container-platform/3.11/architecture/core_concepts/builds_and_image_streams.html#source-build) (S2I) build
- MySQL 8.0 SQL database server

We use following PHP packages via Composer install:

```bash
Lock file operations: 54 installs, 0 updates, 0 removals
  - Locking brick/math (0.9.3)
  - Locking doctrine/inflector (2.0.4)
  - Locking doctrine/lexer (1.2.1)
  - Locking dragonmantank/cron-expression (v3.1.0)
  - Locking egulias/email-validator (2.1.25)
  - Locking graham-campbell/result-type (v1.0.4)
  - Locking laravel/framework (v8.74.0)
  - Locking laravel/serializable-closure (v1.0.5)
  - Locking laravelcollective/html (v6.2.1)
  - Locking league/commonmark (1.6.6)
  - Locking league/flysystem (1.1.8)
  - Locking league/mime-type-detection (1.9.0)
  - Locking monolog/monolog (2.3.5)
  - Locking nesbot/carbon (2.54.0)
  - Locking opis/closure (3.6.2)
  - Locking phpoption/phpoption (1.8.0)
  - Locking psr/container (1.1.1)
  - Locking psr/event-dispatcher (1.0.0)
  - Locking psr/log (1.1.4)
  - Locking psr/simple-cache (1.0.1)
  - Locking ramsey/collection (1.2.2)
  - Locking ramsey/uuid (4.2.3)
  - Locking swiftmailer/swiftmailer (v6.3.0)
  - Locking symfony/console (v5.4.0)
  - Locking symfony/css-selector (v5.4.0)
  - Locking symfony/deprecation-contracts (v2.5.0)
  - Locking symfony/error-handler (v5.4.0)
  - Locking symfony/event-dispatcher (v5.4.0)
  - Locking symfony/event-dispatcher-contracts (v2.5.0)
  - Locking symfony/finder (v5.4.0)
  - Locking symfony/http-foundation (v5.4.0)
  - Locking symfony/http-kernel (v5.4.0)
  - Locking symfony/mime (v5.4.0)
  - Locking symfony/polyfill-ctype (v1.23.0)
  - Locking symfony/polyfill-iconv (v1.23.0)
  - Locking symfony/polyfill-intl-grapheme (v1.23.1)
  - Locking symfony/polyfill-intl-idn (v1.23.0)
  - Locking symfony/polyfill-intl-normalizer (v1.23.0)
  - Locking symfony/polyfill-mbstring (v1.23.1)
  - Locking symfony/polyfill-php72 (v1.23.0)
  - Locking symfony/polyfill-php73 (v1.23.0)
  - Locking symfony/polyfill-php80 (v1.23.1)
  - Locking symfony/polyfill-php81 (v1.23.0)
  - Locking symfony/process (v5.4.0)
  - Locking symfony/routing (v5.4.0)
  - Locking symfony/service-contracts (v2.5.0)
  - Locking symfony/string (v5.4.0)
  - Locking symfony/translation (v5.4.0)
  - Locking symfony/translation-contracts (v2.5.0)
  - Locking symfony/var-dumper (v5.4.0)
  - Locking tijsverkoyen/css-to-inline-styles (2.2.3)
  - Locking vlucas/phpdotenv (v5.4.0)
  - Locking voku/portable-ascii (1.5.6)
  - Locking webmozart/assert (1.10.0)
```

## Version

The latest version of `ng-zorro-antd` is [![npm package](https://img.shields.io/npm/v/ng-zorro-antd.svg?style=flat-square)](https://www.npmjs.org/package/ng-zorro-antd). Check the bottom of the footer for `NG-ZORRO version` to see what version this website was compiled with.
