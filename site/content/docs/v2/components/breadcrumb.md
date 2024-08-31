---
layout: docs
title: Breadcrumb
description: Indicate the current page's location within a navigational hierarchy that automatically adds separators via CSS.
group: components
toc: true
aliases:
  - "/components/breadcrumb/"
---

## Example

Use an ordered or unordered list with linked list items to create a minimally styled breadcrumb. Use our utilities to add additional styles as desired.

{{< example >}}
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item active" aria-current="page">Home</li>
  </ol>
</nav>

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Library</li>
  </ol>
</nav>

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>
{{< /example >}}

## Underlined variant

{{< example >}}
<nav aria-label="breadcrumb">
  <ol class="breadcrumb breadcrumb-underline">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>
{{< /example >}}

## Accessibility

Since breadcrumbs provide a navigation, it's a good idea to add a meaningful label such as `aria-label="breadcrumb"` to describe the type of navigation provided in the `<nav>` element, as well as applying an `aria-current="page"` to the last item of the set to indicate that it represents the current page.

For more information, see the [ARIA Authoring Practices Guide breadcrumb pattern](https://www.w3.org/WAI/ARIA/apg/patterns/breadcrumb/).

## CSS

### Variables

{{< added-in "5.2.0" >}}

As part of Bootstrap's evolving CSS variables approach, breadcrumbs now use local CSS variables on `.breadcrumb` for enhanced real-time customization. Values for the CSS variables are set via Sass, so Sass customization is still supported, too.

{{< scss-docs name="breadcrumb-css-vars" file="scss/_breadcrumb.scss" >}}

### Sass variables

{{< scss-docs name="breadcrumb-variables" file="scss/_variables.scss" >}}
