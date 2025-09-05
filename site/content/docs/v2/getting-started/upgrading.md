---
layout: docs
title: Upgrading from Modus Bootstrap 1
description: Modus Bootstrap 2 can be upgraded from Modus Bootstrap 1
group: getting-started
aliases:
  - "/docs/v2/migrating/"
toc: true
---

## Steps

1. There is a [command-line script](https://github.com/coliff/bootstrap-5-migrate-tool#readme) designed to help you upgrade your Modus Bootstrap 1 (based on Bootstrap 4) projects to Modus Bootstrap 2 (based on Bootstrap 5). It uses gulp with gulp-replace to replace class names within your folder of HTML pages/templates and it can save a lot of time.

2. Check your JavaScript/TypeScript files don't use deprecated/renamed classes and update as necessary as the command-line script in the step above is only really for HTML-like templates.

3. Update any of the CSS imports on your project to remove any `@trimbleinc/modus-bootstrap` imports and instead just use a single import which includes light mode, dark mode, modus-layout and everything else you need.:

```sass
@import '../node_modules/@trimble-oss/modus-bootstrap/dist/css/modus-bootstrap.min.css';`
```

## Post Migration tips

- Modus Bootstrap doesn't include Print styles, though you can use [bootstrap-print-css](https://www.npmjs.com/package/bootstrap-print-css) from npm.
- If you used negative margins/padding classes (e.g, `.mt-n1` or `.pb-n2`) note that these are not included in the CDN version of the Modus Bootstrap CSS so you may want to add those.
- Remember that there is a new XXL breakpoint so be sure to make use of it and optimize layouts[ for screens larger than 1440px](https://modus-bootstrap.trimble.com/docs/v2/layout/breakpoints/).
- There is a [helpful browser extension](https://github.com/julien-deramond/bootstrap-deprecated-classes-extension) which can be used for finding any deprecated classes on your site.
