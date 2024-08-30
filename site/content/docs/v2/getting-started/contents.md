---
layout: docs
title: Contents
description: Discover what's included in Modus Bootstrap, including our compiled and source code flavors.
group: getting-started
toc: true
---

## Compiled Modus Bootstrap

Once downloaded, unzip the compressed folder and you'll see something like this:

<!-- NOTE: This info is intentionally duplicated in the README. Copy any changes made here over to the README too, but be sure to keep in mind to add the `dist` folder. -->

```text
bootstrap/
├── css/
│   ├── modus-bootstrap-grid.css
│   ├── modus-bootstrap-grid.css.map
│   ├── modus-bootstrap-grid.min.css
│   ├── modus-bootstrap-grid.min.css.map
│   ├── modus-bootstrap-grid.rtl.css
│   ├── modus-bootstrap-grid.rtl.css.map
│   ├── modus-bootstrap-grid.rtl.min.css
│   ├── modus-bootstrap-grid.rtl.min.css.map
│   ├── modus-bootstrap-reboot.css
│   ├── modus-bootstrap-reboot.css.map
│   ├── modus-bootstrap-reboot.min.css
│   ├── modus-bootstrap-reboot.min.css.map
│   ├── modus-bootstrap-reboot.rtl.css
│   ├── modus-bootstrap-reboot.rtl.css.map
│   ├── modus-bootstrap-reboot.rtl.min.css
│   ├── modus-bootstrap-reboot.rtl.min.css.map
│   ├── modus-bootstrap-utilities.css
│   ├── modus-bootstrap-utilities.css.map
│   ├── modus-bootstrap-utilities.min.css
│   ├── modus-bootstrap-utilities.min.css.map
│   ├── modus-bootstrap-utilities.rtl.css
│   ├── modus-bootstrap-utilities.rtl.css.map
│   ├── modus-bootstrap-utilities.rtl.min.css
│   ├── modus-bootstrap-utilities.rtl.min.css.map
│   ├── modus-bootstrap.css
│   ├── modus-bootstrap.css.map
│   ├── modus-bootstrap.min.css
│   ├── modus-bootstrap.min.css.map
│   ├── modus-bootstrap.rtl.css
│   ├── modus-bootstrap.rtl.css.map
│   ├── modus-bootstrap.rtl.min.css
│   └── modus-bootstrap.rtl.min.css.map
```

This is the most basic form of Modus Bootstrap: precompiled files for quick drop-in usage in nearly any web project.

### CSS files

Bootstrap includes a handful of options for including some or all of our compiled CSS.

{{< bs-table "table" >}}
| CSS files | Layout | Content | Components | Utilities |
| --- | --- | --- | --- | --- |
| `bootstrap.css`<br> `bootstrap.min.css`<br> `bootstrap.rtl.css`<br> `bootstrap.rtl.min.css` | Included | Included | Included | Included |
| `bootstrap-grid.css`<br> `bootstrap-grid.rtl.css`<br> `bootstrap-grid.min.css`<br> `bootstrap-grid.rtl.min.css` | [Only grid system]({{< docsref "/layout/grid" >}}) | — | — | [Only flex utilities]({{< docsref "/utilities/flex" >}}) |
| `bootstrap-utilities.css`<br> `bootstrap-utilities.rtl.css`<br> `bootstrap-utilities.min.css`<br> `bootstrap-utilities.rtl.min.css` | — | — | — | Included |
| `bootstrap-reboot.css`<br> `bootstrap-reboot.rtl.css`<br> `bootstrap-reboot.min.css`<br> `bootstrap-reboot.rtl.min.css` | — | [Only Reboot]({{< docsref "/content/reboot" >}}) | — | — |
{{< /bs-table >}}

### JS files

Similarly, we have options for including some or all of our compiled JavaScript.

{{< bs-table "table" >}}
| JS Files | Popper |
| --- | --- |
| `bootstrap.bundle.js`<br> `bootstrap.bundle.min.js`<br> | Included |
| `bootstrap.js`<br> `bootstrap.min.js`<br> | – |
{{< /bs-table >}}

## Bootstrap source code

The Bootstrap source code download includes the compiled CSS and JavaScript assets, along with source Sass, JavaScript, and documentation. More specifically, it includes the following and more:

```text
bootstrap/
├── dist/
│   ├── css/
│   └── js/
├── site/
│   └──content/
│      └── docs/
│          └── {{< param docs_version >}}/
│              └── examples/
├── js/
└── scss/
```

The `scss/` and `js/` are the source code for our CSS and JavaScript. The `dist/` folder includes everything listed in the compiled download section above. The `site/docs/` folder includes the source code for our documentation, and `examples/` of Bootstrap usage. Beyond that, any other included file provides support for packages, license information, and development.
