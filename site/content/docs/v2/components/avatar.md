---
layout: docs
title: Avatar
description: Documentation and examples for avatars, including image avatars, initials, status indicators, and avatar stacks.
group: components
toc: true
aliases:
  - "/components/avatars/"
---

## Examples

Avatars are used to represent users or entities. They can display an image or initials as a fallback.

### Image

Use `.avatar` with an `.avatar-img` for image-based avatars. The parent `.avatar` element provides an easy wrapper for additional avatar features like status indicators and stacks. You're welcome to use the `.avatar-img` class on its own if you only need a single HTML element.

{{< example >}}
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
</span>
{{< /example >}}

### Initials

Use text content inside `.avatar` for initials-based avatars.

{{< example >}}
<span class="avatar">AB</span>
<span class="avatar bg-primary text-white">CD</span>
<span class="avatar bg-dark text-white">EF</span>
<span class="avatar bg-success text-white">GH</span>
<span class="avatar bg-danger text-white">HI</span>
<span class="avatar bg-warning text-white">JK</span>
<span class="avatar bg-secondary text-white">LM</span>
{{< /example >}}

### Sizes

Avatars come in multiple sizes: extra small, small, default, large, and extra large.

{{< example >}}
<span class="avatar avatar-xs">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
</span>
<span class="avatar avatar-sm">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
</span>
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
</span>
<span class="avatar avatar-lg">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
</span>
<span class="avatar avatar-xl">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
</span>
{{< /example >}}

### Status indicator

Add a `.avatar-status` element inside the avatar to show a status indicator. Each status has a distinct shape and color:

- `.status-online` — green circle
- `.status-offline` — gray rounded square
- `.status-busy` — red rounded square
- `.status-away` — yellow circle

{{< example >}}
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-online" role="status" aria-label="Online"></span>
</span>
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-offline" role="status" aria-label="Offline"></span>
</span>
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-busy" role="status" aria-label="Busy"></span>
</span>
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-away" role="status" aria-label="Away"></span>
</span>
{{< /example >}}

### Status with sizes

The status indicator scales with the avatar size.

{{< example >}}
<span class="avatar avatar-xs">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-online" role="status" aria-label="Online"></span>
</span>
<span class="avatar avatar-sm">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-online" role="status" aria-label="Online"></span>
</span>
<span class="avatar">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-online" role="status" aria-label="Online"></span>
</span>
<span class="avatar avatar-lg">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-online" role="status" aria-label="Online"></span>
</span>
<span class="avatar avatar-xl">
  <img class="avatar-img" src="https://github.com/coliff.png" alt="CO">
  <span class="avatar-status status-online" role="status" aria-label="Online"></span>
</span>
{{< /example >}}

### Avatar stack

Use `.avatar-stack` to group multiple avatars together with overlapping effect. Avatars are rendered in reverse order so the first avatar appears on top. Stacks use a percentage of the avatar size to determine how much to overlap stacked avatars.

{{< example >}}
<div class="avatar-stack">
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=34" alt="34">
  </span>
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=35" alt="35">
  </span>
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=36" alt="36">
  </span>
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=37" alt="37">
  </span>
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=38" alt="38">
  </span>
</div>
{{< /example >}}

### Stack with count

Combine with initials to show a count of additional users.

{{< example >}}
<div class="avatar-stack">
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=39" alt="39">
  </span>
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=40" alt="40">
  </span>
  <span class="avatar">
    <img class="avatar-img" src="https://i.pravatar.cc/150?img=41" alt="41">
  </span>
  <span class="avatar">+5</span>
</div>
{{< /example >}}
