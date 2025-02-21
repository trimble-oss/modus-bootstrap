---
layout: docs
title: "Modus Layout"
description: "Besides the aesthetics and UI elements, the Modus Framework has an
optional layout you can use for your web applications."
group: layout
toc: true
loadModusLayout: true
---

## Basic Structure

The basic structure for our Modus Layout, including the sidebar,
toolbar, and panel, is as follows:

```text
div.modus-layout
        ├── nav.modus-header
        ├── div.modus-body
        |   ├── nav.modus-sidebar
        |   └── div.modus-content-rows
        |       ├── div.modus-toolbar (optional)
        |       └── div.modus-content-columns
        |           ├── div.modus-panel (optional)
        |           └── div.modus-content
        └── div.modus-footer
```

The page should be wrapped in a `.modus-layout` to set up the
overall structure.

The top navbar is a standard Bootstrap
`nav.navbar.navbar-expand-lg` with an additional class of
`.modus-header` to apply the aesthetics. Please refer to the
<a href="/docs/v2/components/navbar/">Navbar Docs</a>
for more information.

The `.modus-header` should be followed by
`.modus-body` to set up the left nav area and main content
area.

After `.modus-body` should be
`nav.modus-sidebar` which contains a vertical nav list (more
info below).

The next sibling element after the `.modus-sidebar` should be
`.modus-content-rows` with an optional child of
`.modus-toolbar`.

After `.modus-content-rows` should be
`.modus-content-columns` with an optional child of
`.modus-panel`.

Your main content is housed within `.modus-content` inside of
`.modus-content-columns`.

After the `.modus-body`, the next element should be
`.modus-footer`.

### Interactive Example

To help illustrate how all the layout elements look when displayed
we have this interactive example. <a href="/docs/v2/examples/web-app/" target="_blank">Open in a new tab</a>

<iframe src="/docs/v2/examples/web-app/" height="500" class="w-100 border mb-3" style="max-width: 777px">
</iframe>

### Modus Sidebar

The Modus sidebar is a simple Bootstrap
<code>.nav flex-column</code> element with an additional
<code>.modus-sidebar</code> class for styling. Each
<code>.nav-link</code> should have an icon or image with a class of
<code>.left-nav-icon</code>.

The <code>.modus-body</code> should have a class of either
<code>.sidebar-open</code> or <code>.sidebar-closed</code> to open or
close the sidebar.

Toggling the sidebar is done through a menu button icon with an
attribute of <code>data-modus-item="menu-btn"</code>. The
<code>.modus-body</code> should also have a corresponding attribute of
<code>data-modus-item="body"</code>.

### Modus Toolbar

Our framework includes an all purpose toolbar that can be inserted
inside your layout. Simply add `.modus-toolbar` inside
`.modus-content-rows`.

You can use our other components, such as buttons and form groups,
inside `.modus-toolbar` to add functionality to your
application.

### Modus Panel

Our framework also includes panels that can be inserted into your
layout. Simply add `.modus-panel` inside of
`.modus-content-columns` before `.modus-content`.

The panels come with `.panel-header`,
`.panel-body`, and `.panel-footer` classes for
additional layout options.

Items can be aligned to the left or right of the
`.panel-header` by using either `.left-items` or
`.right-items` classes.

You also have the option of including `.static-container` and
`.scroll-container` inside the `.panel-body` for
additional functionality.

**Note:** Modus Panels must be given a `width` using any of the following classes:

- `.panel-sm` (256px)
- `.panel-md` (352px)
- `.panel-lg` (448px)
- `.panel-xl` (544px)
