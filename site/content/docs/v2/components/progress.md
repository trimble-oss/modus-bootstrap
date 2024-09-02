---
layout: docs
title: Progress
description: Documentation and examples for using Modus Bootstrap custom progress bars featuring support for stacked bars, animated backgrounds, and text labels.
group: components
toc: true
aliases:
  - "/components/progress/"
  - "/components/progress-bars/"
---

## How it works

Progress components are built with two HTML elements, some CSS to set the width, and a few attributes. We don't use [the HTML5 `<progress>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress), ensuring you can stack progress bars, animate them, and place text labels over them.

- We use the `.progress` as a wrapper to indicate the max value of the progress bar.
- The `.progress` wrapper also requires a `role="progressbar"` and `aria` attributes to make it accessible, including an accessible name (using `aria-label`, `aria-labelledby`, or similar).
- We use the inner `.progress-bar` purely for the visual bar and label.
- The `.progress-bar` requires an inline style, utility class, or custom CSS to set its width.
- We provide a special `.progress-stacked` class to create multiple/stacked progress bars.

Put that all together, and you have the following examples.

{{< example >}}
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-label="Basic example" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-label="Basic example" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-label="Basic example" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-label="Basic example" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-label="Basic example" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
</div>
{{< /example >}}

Modus Bootstrap provides a handful of [utilities for setting width]({{< docsref "/utilities/sizing" >}}). Depending on your needs, these may help with quickly configuring progress.

{{< example >}}
<div class="progress">
  <div class="progress-bar w-75" role="progressbar" aria-label="Basic example" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
</div>
{{< /example >}}

## Small Variant

{{< example >}}
<div class="progress progress-sm">
  <div class="progress-bar w-75" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
</div>
{{< /example >}}

## XS Variant

{{< example >}}
<div class="progress progress-xs">
  <div class="progress-bar w-75" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
</div>
{{< /example >}}

## CSS

### Variables

{{< added-in "5.2.0" >}}

As part of Bootstrap's evolving CSS variables approach, progress bars now use local CSS variables on `.progress` for enhanced real-time customization. Values for the CSS variables are set via Sass, so Sass customization is still supported, too.

{{< scss-docs name="progress-css-vars" file="scss/_progress.scss" >}}

### Sass variables

{{< scss-docs name="progress-variables" file="scss/_variables.scss" >}}


