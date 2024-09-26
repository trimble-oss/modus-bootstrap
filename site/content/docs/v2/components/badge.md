---
layout: docs
title: Badges
description: Documentation and examples for badges, our small count and labeling component.
group: components
toc: true
aliases:
  - "/components/badge/"
  - "/components/badges/"
  - "/docs/v2/components/badges/"
---

## Examples

Badges scale to match the size of the immediate parent element by using relative font sizing and `em` units. As of v5, badges no longer have focus or hover styles for links.

### Buttons

Badges can be used as part of links or buttons to provide a counter.

{{< example >}}
<button type="button" class="btn btn-primary">
  Notifications <span class="badge text-bg-secondary">4</span>
</button>
{{< /example >}}

Note that depending on how they are used, badges may be confusing for users of screen readers and similar assistive technologies. While the styling of badges provides a visual cue as to their purpose, these users will simply be presented with the content of the badge. Depending on the specific situation, these badges may seem like random additional words or numbers at the end of a sentence, link, or button.

Unless the context is clear (as with the "Notifications" example, where it is understood that the "4" is the number of notifications), consider including additional context with a visually hidden piece of additional text.

### Positioned

Use utilities to modify a `.badge` and position it in the corner of a link or button.

{{< example >}}
<button type="button" class="btn btn-primary position-relative">
  Inbox
  <span class="position-absolute top-0 start-100 translate-middle badge rounded-pill bg-danger">
    99+
    <span class="visually-hidden">unread messages</span>
  </span>
</button>
{{< /example >}}

You can also replace the `.badge` class with a few more utilities without a count for a more generic indicator.

{{< example >}}
<button type="button" class="btn btn-primary position-relative">
  Profile
  <span class="position-absolute top-0 start-100 translate-middle p-2 bg-danger border border-light rounded-circle">
    <span class="visually-hidden">New alerts</span>
  </span>
</button>
{{< /example >}}

## Background colors

{{< added-in "5.2.0" >}}

Set a `background-color` with contrasting foreground `color` with [our `.text-bg-{color}` helpers]({{< docsref "helpers/color-background" >}}). Previously it was required to manually pair your choice of [`.text-{color}`]({{< docsref "/utilities/colors" >}}) and [`.bg-{color}`]({{< docsref "/utilities/background" >}}) utilities for styling, which you still may use if you prefer.

{{< example >}}
<span class="badge text-bg-primary">Primary</span>
<span class="badge text-bg-secondary">Secondary</span>
<span class="badge text-bg-tertiary">Tertiary</span>
<span class="badge text-bg-success">Success</span>
<span class="badge text-bg-danger">Danger</span>
<span class="badge text-bg-warning">Warning</span>
<span class="badge bg-high-contrast">High Contrast</span>
{{< /example >}}

{{< callout info >}}
{{< partial "callouts/warning-color-assistive-technologies.md" >}}
{{< /callout >}}

## Counter Badges

Use the `.badge-pill` modifier class to make badges more rounded

<div class="mb-3">
  <span class="badge badge-pill bg-primary">1</span>
  <span class="badge badge-pill bg-secondary">2</span>
  <span class="badge badge-pill text-bg-tertiary">3</span>
  <span class="badge badge-pill bg-high-contrast">4</span>
  <span class="badge badge-pill bg-success">5</span>
  <span class="badge badge-pill bg-danger">6</span>
  <span class="badge badge-pill bg-warning">7</span>
</div>

## Badge Sizes

By default Badges scale according to their immediate parent element but there are also large and small options available.

<span class="badge badge-sm bg-primary">Small</span>
<span class="badge bg-primary">Default</span>
<span class="badge badge-lg bg-primary">Large</span>

## Text Badges

{{< example >}}
<span class="badge text-primary">Primary</span>
<span class="badge text-secondary">Secondary</span>
<span class="badge text-body">High Contrast</span>
<span class="badge text-success">Success</span>
<span class="badge text-danger">Danger</span>
{{< /example >}}

## CSS

### Variables

{{< added-in "5.2.0" >}}

As part of Bootstrap's evolving CSS variables approach, badges now use local CSS variables on `.badge` for enhanced real-time customization. Values for the CSS variables are set via Sass, so Sass customization is still supported, too.

{{< scss-docs name="badge-css-vars" file="scss/_badge.scss" >}}

### Sass variables

{{< scss-docs name="badge-variables" file="scss/_variables.scss" >}}
