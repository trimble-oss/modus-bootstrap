---
layout: docs
title: "Chips"
description: "Chips are compact elements that represent an input, attribute, or action. Chips should appear dynamically as a
  group of multiple interactive elements. Unlike buttons, which should be a consistent and familiar call to action,
  one that a user expects to appear as the same action in the same general area."
group: components
StyleGuide: "components/chips/"
toc: true
---

## Overview

Chips are used to add information, make selections or filter content. Chips should appear
dynamically as a group of multiple interactive elements.

To use chips, add classes `.chip`

To specify the style, use one of these classes:

- `.chip-solid`
- `.chip-outline`

### Input Chips

For Input Chips, use the class `.chip-input`

{{< example id="example-chips" >}}
<button class="chip chip-solid chip-input" type="button">
  <div class="chip-thumbnail">
    <img src="/img/headshot.png" height="24" width="24" alt="">
  </div>
  <div class="chip-text">Solid</div>
  <div class="chip-delete-right">
    <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="16" width="16" viewBox="0 0 32 32">
      <path d="M16 30c7.72 0 14-6.28 14-14S23.72 2 16 2 2 8.28 2 16s6.28 14 14 14zm-5.06-16.94a1.49 1.49 0 0 1 0-2.12 1.49 1.49 0 0 1 2.12 0L16 13.88l2.94-2.94a1.49 1.49 0 0 1 2.12 0c.59.59.59 1.53 0 2.12L18.12 16l2.94 2.94c.59.59.59 1.53 0 2.12-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44L16 18.12l-2.94 2.94c-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44a1.49 1.49 0 0 1 0-2.12L13.88 16l-2.94-2.94z" />
    </svg>
  </div>
</button>

<button class="chip chip-outline chip-input ms-2" type="button">
  <div class="chip-thumbnail">
    <img src="/img/headshot.png" height="24" width="24" alt="">
  </div>
  <div class="chip-text">Outline</div>
  <div class="chip-delete-right">
    <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="16" width="16" viewBox="0 0 32 32">
      <path d="M16 30c7.72 0 14-6.28 14-14S23.72 2 16 2 2 8.28 2 16s6.28 14 14 14zm-5.06-16.94a1.49 1.49 0 0 1 0-2.12 1.49 1.49 0 0 1 2.12 0L16 13.88l2.94-2.94a1.49 1.49 0 0 1 2.12 0c.59.59.59 1.53 0 2.12L18.12 16l2.94 2.94c.59.59.59 1.53 0 2.12-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44L16 18.12l-2.94 2.94c-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44a1.49 1.49 0 0 1 0-2.12L13.88 16l-2.94-2.94z" />
    </svg>
  </div>
</button>
{{</ example >}}

### Filter Chips

For Filter Chips, use the class `.chip-filter`

{{< example id="example-chips-filter" >}}
<button class="chip chip-solid chip-filter" type="button">
  <div class="chip-icon-left"><i class="modus-icons notranslate" aria-hidden="true">done</i></div>
  <div class="chip-text">Red fish</div>
</button>

<button class="chip chip-outline chip-filter ms-2" type="button">
  <div class="chip-text">Blue fish</div>
</button>
{{</ example >}}

### Small Chips

To use a small chip, just add the class `.chip-sm`

{{< example id="example-chips-small" >}}
<button class="chip chip-sm chip-solid chip-input" type="button">
  <div class="chip-thumbnail">
    <img src="/img/headshot.png" alt="">
  </div>
  <div class="chip-text">Jane</div>
  <div class="chip-delete-right">
    <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="16" width="16" viewBox="0 0 32 32">
      <path d="M16 30c7.72 0 14-6.28 14-14S23.72 2 16 2 2 8.28 2 16s6.28 14 14 14zm-5.06-16.94a1.49 1.49 0 0 1 0-2.12 1.49 1.49 0 0 1 2.12 0L16 13.88l2.94-2.94a1.49 1.49 0 0 1 2.12 0c.59.59.59 1.53 0 2.12L18.12 16l2.94 2.94c.59.59.59 1.53 0 2.12-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44L16 18.12l-2.94 2.94c-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44a1.49 1.49 0 0 1 0-2.12L13.88 16l-2.94-2.94z"/>
    </svg>
  </div>
</button>

<button class="chip chip-sm chip-outline chip-input" type="button">
  <div class="chip-thumbnail">
    <img src="/img/headshot.png" alt="">
  </div>
  <div class="chip-text">Jane</div>
  <div class="chip-delete-right">
    <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="16" width="16" viewBox="0 0 32 32">
      <path d="M16 30c7.72 0 14-6.28 14-14S23.72 2 16 2 2 8.28 2 16s6.28 14 14 14zm-5.06-16.94a1.49 1.49 0 0 1 0-2.12 1.49 1.49 0 0 1 2.12 0L16 13.88l2.94-2.94a1.49 1.49 0 0 1 2.12 0c.59.59.59 1.53 0 2.12L18.12 16l2.94 2.94c.59.59.59 1.53 0 2.12-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44L16 18.12l-2.94 2.94c-.29.29-.68.44-1.06.44s-.77-.15-1.06-.44a1.49 1.49 0 0 1 0-2.12L13.88 16l-2.94-2.94z"/>
    </svg>
  </div>
</button>

<button class="chip chip-sm chip-solid chip-filter active" type="button">
  <div class="chip-icon-left"><i class="modus-icons notranslate" aria-hidden="true">check</i></div>
  <div class="chip-text">Taxi</div>
</button>

<button class="chip chip-sm chip-outline chip-filter" type="button">
  <div class="chip-text">Car</div>
</button>
{{</ example >}}
