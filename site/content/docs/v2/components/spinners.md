---
layout: docs
title: Spinners
description: Indicate the loading state of a component or page with Modus Bootstrap spinners, built entirely with HTML, CSS, and no JavaScript.
group: components
toc: true
aliases:
  - "/components/spinners/"
---

## About

Bootstrap "spinners" can be used to show the loading state in your projects. They're built only with HTML and CSS, meaning you don't need any JavaScript to create them. You will, however, need some custom JavaScript to toggle their visibility. Their appearance, alignment, and sizing can be easily customized with our amazing utility classes.

For accessibility purposes, each loader here includes `role="status"` and a nested `<span class="visually-hidden">Loading...</span>`.

{{< callout info >}}
{{< partial "callouts/info-prefersreducedmotion.md" >}}
{{< /callout >}}

## Border spinner

Use the border spinners for a lightweight loading indicator.

{{< example class="d-flex gap-4" >}}
<div class="spinner-border" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<div class="spinner-border text-secondary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<div class="spinner-border text-tertiary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
{{< /example >}}

## Large Variant

Use the `.spinner-border-lg` for a larger spinner.

{{< example class="d-flex gap-4" >}}
<div class="spinner-border spinner-border-lg" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<div class="spinner-border spinner-border-lg text-secondary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<div class="spinner-border spinner-border-lg text-tertiary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
{{< /example >}}

## Growing spinner

If you don’t fancy a border spinner, switch to the grow spinner. While it doesn’t technically spin, it does repeatedly grow!

{{< example >}}
<div class="spinner-grow" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
{{< /example >}}

## Alignment

Spinners in Modus Bootstrap are built with `rem`s, `currentColor`, and `display: inline-flex`. This means they can easily be resized, recolored, and quickly aligned.

### Margin

Use [margin utilities][margin] like `.m-5` for easy spacing.

{{< example >}}
<div class="spinner-border m-5" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
{{< /example >}}

### Placement

Use [flexbox utilities][flex], [float utilities][float], or [text alignment][text] utilities to place spinners exactly where you need them in any situation.

#### Flex

{{< example >}}
<div class="d-flex justify-content-center">
  <div class="spinner-border" role="status">
    <span class="visually-hidden">Loading...</span>
  </div>
</div>
{{< /example >}}

{{< example >}}
<div class="d-flex align-items-center">
  <strong role="status">Loading...</strong>
  <div class="spinner-border ms-auto" aria-hidden="true"></div>
</div>
{{< /example >}}

#### Floats

{{< example >}}
<div class="clearfix">
  <div class="spinner-border float-end" role="status">
    <span class="visually-hidden">Loading...</span>
  </div>
</div>
{{< /example >}}

#### Text align

{{< example >}}
<div class="text-center">
  <div class="spinner-border" role="status">
    <span class="visually-hidden">Loading...</span>
  </div>
</div>
{{< /example >}}

## Buttons

Use spinners within buttons to indicate an action is currently processing or taking place. You may also swap the text out of the spinner element and utilize button text as needed.

{{< example >}}
<button class="btn btn-primary" type="button" disabled>
  <span class="spinner-border text-white spinner-border-sm" aria-hidden="true"></span>
  <span class="visually-hidden" role="status">Loading...</span>
</button>
<button class="btn btn-primary" type="button" disabled>
  <span class="spinner-border text-white spinner-border-sm" role="status" aria-hidden="true"></span>
  Loading...
</button>
{{< /example >}}

## CSS

### Variables

{{< added-in "5.2.0" >}}

As part of Bootstrap's evolving CSS variables approach, spinners now use local CSS variables on `.spinner-border` and `.spinner-grow` for enhanced real-time customization. Values for the CSS variables are set via Sass, so Sass customization is still supported, too.

Border spinner variables:

{{< scss-docs name="spinner-border-css-vars" file="scss/_spinners.scss" >}}

For both spinners, small spinner modifier classes are used to update the values of these CSS variables as needed. For example, the `.spinner-border-sm` class does the following:

{{< scss-docs name="spinner-border-sm-css-vars" file="scss/_spinners.scss" >}}

### Sass variables

{{< scss-docs name="spinner-variables" file="scss/_variables.scss" >}}

### Keyframes

Used for creating the CSS animations for our spinners. Included in `scss/_spinners.scss`.

{{< scss-docs name="spinner-border-keyframes" file="scss/_spinners.scss" >}}

[color]:   {{< docsref "/utilities/colors" >}}
[flex]:    {{< docsref "/utilities/flex" >}}
[float]:   {{< docsref "/utilities/float" >}}
[margin]:  {{< docsref "/utilities/spacing" >}}
[text]:    {{< docsref "/utilities/text" >}}
