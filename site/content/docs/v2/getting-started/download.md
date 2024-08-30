---
layout: docs
title: Download
description: Download Modus Bootstrap to get the compiled CSS and JavaScript, source code, or include it with your favorite package managers like npm, RubyGems, and more.
group: getting-started
toc: true
---

## Compiled CSS and JS

Download ready-to-use compiled code for **Modus Bootstrap v{{< param current_version >}}** to easily drop into your project, which includes compiled and minified CSS bundles (see [CSS files comparison]({{< docsref "/getting-started/contents#css-files" >}}))

This doesn't include documentation, source files, or any optional JavaScript dependencies like Popper.

<a href="https://github.com/trimble-oss/modus-bootstrap/releases" class="btn btn-primary">Download</a>

## Source files (Recommended)

Compile Modus Bootstrap with your own asset pipeline by downloading our source Sass, JavaScript, and documentation files. This option requires some additional tooling:

- [Sass compiler]({{< docsref "/getting-started/contribute#sass" >}}) for compiling Sass source files into CSS files
- [Autoprefixer](https://github.com/postcss/autoprefixer) for CSS vendor prefixing

Should you require our full set of [build tools]({{< docsref "/getting-started/contribute#tooling-setup" >}}), they are included for developing Bootstrap and its docs, but they're likely unsuitable for your own purposes.

<a href="https://github.com/trimble-oss/modus-bootstrap/" class="btn btn-primary">Download source</a>

## CDN via jsDelivr

Skip the download with [jsDelivr](https://www.jsdelivr.com) to deliver cached version of Modus Bootstrap's compiled CSS and JS to your project.

```html
<link href="{{< param "cdn.css" >}}" rel="stylesheet" crossorigin="anonymous">
<script src="{{< param "cdn.js_bundle" >}}" crossorigin="anonymous"></script>
```

## Package managers

Pull in Modus Bootstrap's **source files** into nearly any project with some of the most popular package managers. No matter the package manager, Bootstrap will **require a [Sass compiler]({{< docsref "/getting-started/contribute#sass" >}}) and [Autoprefixer](https://github.com/postcss/autoprefixer)** for a setup that matches our official compiled versions.

### npm

Install Modus Bootstrap in your Node.js powered apps with [the npm package](https://www.npmjs.com/package/@trimble-oss/modus-bootstrap):

```sh
npm install @trimble-oss/modus-bootstrap
```

Bootstrap's `package.json` contains some additional metadata under the following keys:

- `sass` - path to Modus Bootstrap's main [Sass](https://sass-lang.com/) source file
- `style` - path to Modus Bootstrap's non-minified CSS that's been precompiled using the default settings (no customization)

### yarn

Install Modus Bootstrap in your Node.js powered apps with [the yarn package](https://yarnpkg.com/en/package/@trimble-inc/modus-bootstrap):

```sh
yarn add @trimble-oss/modus-bootstrap
```
