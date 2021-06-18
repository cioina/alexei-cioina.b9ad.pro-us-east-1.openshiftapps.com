---
order: 0
title: What Is This?
---

This is an unofficial `ng-zorro-antd` demo website. The main goal is to explore and learn `ng-zorro-antd` components and Angular `^11.0.0`.

> At this time, we use some `ng-zorro-antd` documentation pages for demonstration purpose.

<div class="pic-plus">
  <img alt="Ant Design" width="150" height="150" src="https://img.alicdn.com/tfs/TB1g.mWZAL0gK0jSZFtXXXQCXXa-200-200.svg">
  <span>+</span>
  <img alt="Angular" width="140" height="150" src="https://img.alicdn.com/tfs/TB1Z0PywTtYBeNjy1XdXXXXyVXa-186-200.svg">
</div>

## Static vs Dynamic

The main difference between this website and the official `ng-zorro-antd` [website](https://ng.ant.design/docs/introduce/en) is that we don't use Server-side Rendering (SSR). If you are interested in SSR, you may choose:

- **Angular Universal:** can control server-rendered page and transfer state before client-side web app loads to the client-side-app ([website](https://github.com/angular/universal))
- **Scully:** is a static site generator for Angular ([website](https://github.com/scullyio/scully))

## Client-side

The client-side code is written in TypeScript and is compiled with `@angular/cli`.

- Written in TypeScript with complete defined types
- 60+ high-quality`ng-zorro-antd` components out of the box
- Default and dark themes out of the box
- Lazy-loading Angular modules
- Reactive libraries for Angular ([website](https://github.com/ngrx/platform))
- Differential loading for legacy browser support
- "Headless" website architecture (decoupled architecture)

## Server-side

The server-side code is written in PHP and uses Laravel 8 framework.

- Written in PHP on top of Laravel framework
- JSON Web Token Authentication (JWT) for Laravel
- Cross-Origin Resource Sharing (CORS) for Laravel
- The content for the site is accessible via a RESTful web-service API
- Hosted by Red Hat OpenShift Online ([website](https://www.openshift.com/products/online/))
- Source-to-Image (S2I) Build ([website](https://docs.openshift.com/container-platform/3.11/architecture/core_concepts/builds_and_image_streams.html#source-build))
- MySQL 8.0 SQL database server

We use following PHP packages via Composer install:

```bash
Package operations: 52 installs, 0 updates, 0 removals
  - Installing doctrine/inflector (2.0.3): Extracting archive
  - Installing doctrine/lexer (1.2.1): Extracting archive
  - Installing symfony/polyfill-ctype (v1.23.0): Extracting archive
  - Installing webmozart/assert (1.10.0): Extracting archive
  - Installing dragonmantank/cron-expression (v3.1.0): Extracting archive
  - Installing voku/portable-ascii (1.5.6): Extracting archive
  - Installing symfony/polyfill-php80 (v1.23.0): Extracting archive
  - Installing symfony/polyfill-mbstring (v1.23.0): Extracting archive
  - Installing phpoption/phpoption (1.7.5): Extracting archive
  - Installing graham-campbell/result-type (v1.0.1): Extracting archive
  - Installing vlucas/phpdotenv (v5.3.0): Extracting archive
  - Installing symfony/css-selector (v5.3.0): Extracting archive
  - Installing tijsverkoyen/css-to-inline-styles (2.2.3): Extracting archive
  - Installing symfony/var-dumper (v5.3.2): Extracting archive
  - Installing symfony/deprecation-contracts (v2.4.0): Extracting archive
  - Installing symfony/routing (v5.3.0): Extracting archive
  - Installing symfony/process (v5.3.2): Extracting archive
  - Installing symfony/polyfill-php72 (v1.23.0): Extracting archive
  - Installing symfony/polyfill-intl-normalizer (v1.23.0): Extracting archive
  - Installing symfony/polyfill-intl-idn (v1.23.0): Extracting archive
  - Installing symfony/mime (v5.3.2): Extracting archive
  - Installing symfony/polyfill-php73 (v1.23.0): Extracting archive
  - Installing symfony/http-foundation (v5.3.2): Extracting archive
  - Installing symfony/http-client-contracts (v2.4.0): Extracting archive
  - Installing psr/event-dispatcher (1.0.0): Extracting archive
  - Installing symfony/event-dispatcher-contracts (v2.4.0): Extracting archive
  - Installing symfony/event-dispatcher (v5.3.0): Extracting archive
  - Installing psr/log (1.1.4): Extracting archive
  - Installing symfony/error-handler (v5.3.0): Extracting archive
  - Installing symfony/http-kernel (v5.3.2): Extracting archive
  - Installing symfony/finder (v5.3.0): Extracting archive
  - Installing symfony/polyfill-intl-grapheme (v1.23.0): Extracting archive
  - Installing symfony/string (v5.3.2): Extracting archive
  - Installing psr/container (1.1.1): Extracting archive
  - Installing symfony/service-contracts (v2.4.0): Extracting archive
  - Installing symfony/console (v5.3.2): Extracting archive
  - Installing symfony/polyfill-iconv (v1.23.0): Extracting archive
  - Installing egulias/email-validator (2.1.25): Extracting archive
  - Installing swiftmailer/swiftmailer (v6.2.7): Extracting archive
  - Installing ramsey/collection (1.1.3): Extracting archive
  - Installing brick/math (0.9.2): Extracting archive
  - Installing ramsey/uuid (4.1.1): Extracting archive
  - Installing psr/simple-cache (1.0.1): Extracting archive
  - Installing opis/closure (3.6.2): Extracting archive
  - Installing symfony/translation-contracts (v2.4.0): Extracting archive
  - Installing symfony/translation (v5.3.2): Extracting archive
  - Installing nesbot/carbon (2.49.0): Extracting archive
  - Installing monolog/monolog (2.2.0): Extracting archive
  - Installing league/mime-type-detection (1.7.0): Extracting archive
  - Installing league/flysystem (1.1.3): Extracting archive
  - Installing league/commonmark (1.6.2): Extracting archive
  - Installing laravel/framework (v8.47.0): Extracting archive
  ```

## Version

The latest version of `ng-zorro-antd` is [![npm package](https://img.shields.io/npm/v/ng-zorro-antd.svg?style=flat-square)](https://www.npmjs.org/package/ng-zorro-antd). Check the bottom of the footer for `NG-ZORRO version` to see what version this website was compiled with.
