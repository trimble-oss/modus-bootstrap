---
layout: docs
title: Accordion
description: Build vertically collapsing accordions in combination with our Collapse JavaScript plugin.
group: components
aliases:
  - "/components/"
  - "/components/accordions/"
  - "/docs/v2/components/"
  - "/docs/v2/components/accordions/"
toc: true
---

## How it works

The accordion uses [collapse]({{< docsref "/components/collapse" >}}) internally to make it collapsible. To render an accordion that's expanded, add the `.open` class on the `.accordion`.

{{< callout info >}}
{{< partial "callouts/info-prefersreducedmotion.md" >}}
{{< /callout >}}

## Example

Click the accordions below to expand/collapse the accordion content.

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion" id="accordionExample">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
        Accordion Item #1
        <div class="supporting-label">Supporting Label</div>
      </button>
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the first item's accordion body.</strong> It is shown by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the second item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
        Accordion Item #3
      </button>
    </h2>
    <div id="collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the third item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
</div>
{{< /example >}}

### Flush

Add `.accordion-flush` to remove some borders and rounded corners to render accordions edge-to-edge with their parent container.

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion accordion-flush" id="accordionFlushExample">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseOne" aria-expanded="false" aria-controls="flush-collapseOne">
        Accordion Item #1
      </button>
    </h2>
    <div id="flush-collapseOne" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-flush</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseTwo" aria-expanded="false" aria-controls="flush-collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="flush-collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-flush</code> class. This is the second item's accordion body. Let's imagine this being filled with some actual content.</div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseThree" aria-expanded="false" aria-controls="flush-collapseThree">
        Accordion Item #3
      </button>
    </h2>
    <div id="flush-collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-flush</code> class. This is the third item's accordion body. Nothing more exciting happening here in terms of content, but just filling up the space to make it look, at least at first glance, a bit more representative of how this would look in a real-world application.</div>
    </div>
  </div>
</div>
{{< /example >}}

### Always open

Omit the `data-bs-parent` attribute on each `.accordion-collapse` to make accordion items stay open when another item is opened.

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion" id="accordionPanelsStayOpenExample">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#panelsStayOpen-collapseOne" aria-expanded="true" aria-controls="panelsStayOpen-collapseOne">
        Accordion Item #1
      </button>
    </h2>
    <div id="panelsStayOpen-collapseOne" class="accordion-collapse collapse show">
      <div class="accordion-body">
        <strong>This is the first item's accordion body.</strong> It is shown by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#panelsStayOpen-collapseTwo" aria-expanded="false" aria-controls="panelsStayOpen-collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="panelsStayOpen-collapseTwo" class="accordion-collapse collapse">
      <div class="accordion-body">
        <strong>This is the second item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#panelsStayOpen-collapseThree" aria-expanded="false" aria-controls="panelsStayOpen-collapseThree">
        Accordion Item #3
      </button>
    </h2>
    <div id="panelsStayOpen-collapseThree" class="accordion-collapse collapse">
      <div class="accordion-body">
        <strong>This is the third item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
</div>
{{< /example >}}

## Individual Accordion Items

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion mb-3">
  <div class="accordion-item">
    <h2 class="accordion-header" id="individual-headingOne">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#individual-collapseOne" aria-expanded="false" aria-controls="individual-collapseOne">
        Accordion Item #1
        <div class="supporting-label">Supporting Label</div>
      </button>
    </h2>
    <div id="individual-collapseOne" class="accordion-collapse collapse" aria-labelledby="individual-headingOne">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-small</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
</div>

<div class="accordion mb-3">
  <div class="accordion-item">
    <h2 class="accordion-header" id="individual-headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#individual-collapseTwo" aria-expanded="false" aria-controls="individual-collapseTwo">
        Accordion Item #1
      </button>
    </h2>
    <div id="individual-collapseTwo" class="accordion-collapse collapse" aria-labelledby="individual-headingTwo">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-small</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
</div>
{{< /example >}}

## Small Variant

Add `.accordion-sm` for small version.

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion accordion-sm" id="accordionSmallFlushExample">
  <div class="accordion-item">
    <h2 class="accordion-header" id="small-headingOne">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#small-collapseOne" aria-expanded="false" aria-controls="small-collapseOne">
        Accordion Item #1
      </button>
    </h2>
    <div id="small-collapseOne" class="accordion-collapse collapse" aria-labelledby="small-headingOne" data-bs-parent="#accordionsmallExample">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-small</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="small-headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#small-collapseTwo" aria-expanded="false" aria-controls="small-collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="small-collapseTwo" class="accordion-collapse collapse" aria-labelledby="small-headingTwo" data-bs-parent="#accordionsmallExample">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-sm</code> class. This is the second item's accordion body. Let's imagine this being filled with some actual content.</div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="small-headingThree">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#small-collapseThree" aria-expanded="false" aria-controls="small-collapseThree">
        Accordion Item #3
      </button>
    </h2>
    <div id="small-collapseThree" class="accordion-collapse collapse" aria-labelledby="small-headingThree" data-bs-parent="#accordionsmallExample">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-sm</code> class. This is the third item's accordion body. Nothing more exciting happening here in terms of content, but just filling up the space to make it look, at least at first glance, a bit more representative of how this would look in a real-world application.</div>
    </div>
  </div>
</div>
{{< /example >}}

## Wide Variant

Add `.accordion-wide` for wide version. The size is the same as the default accordion, but the collapse / expand icons are different.

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion accordion-wide">
  <div class="accordion-item">
    <h2 class="accordion-header" id="individual-headingOne">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#wide-collapseOne" aria-expanded="false" aria-controls="wide-collapseOne">
        Accordion Item #1
        <div class="supporting-label">Supporting Label</div>
      </button>
    </h2>
    <div id="wide-collapseOne" class="accordion-collapse collapse" aria-labelledby="wide-headingOne">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-wide</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
</div>

<div class="accordion accordion-wide">
  <div class="accordion-item">
    <h2 class="accordion-header" id="wide-headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#wide-collapseTwo" aria-expanded="false" aria-controls="wide-collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="wide-collapseTwo" class="accordion-collapse collapse" aria-labelledby="wide-headingTwo">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-wide</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
</div>
{{< /example >}}

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion accordion-sm accordion-wide">
  <div class="accordion-item">
    <h2 class="accordion-header" id="individual-headingOne">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#wideCompact-collapseOne" aria-expanded="false" aria-controls="wideCompact-collapseOne">
        Accordion Item #1
        <div class="supporting-label">Supporting Label</div>
      </button>
    </h2>
    <div id="wideCompact-collapseOne" class="accordion-collapse collapse" aria-labelledby="wideCompact-headingOne">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-wide</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
</div>

<div class="accordion accordion-sm accordion-wide">
  <div class="accordion-item">
    <h2 class="accordion-header" id="wideCompact-headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#wideCompact-collapseTwo" aria-expanded="false" aria-controls="wideCompact-collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="wideCompact-collapseTwo" class="accordion-collapse collapse" aria-labelledby="wideCompact-headingTwo">
      <div class="accordion-body">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-wide</code> class. This is the first item's accordion body.</div>
    </div>
  </div>
</div>
{{< /example >}}

## Accessibility

Please read the [collapse accessibility section]({{< docsref "/components/collapse#accessibility" >}}) for more information.

### Accordions with the details element

Experimental feature: You can create an accordion without requiring JavaScript using the details / summary elements. Note that this doesn't have expand / collapse animation.

{{< example class="bg-body-secondary bg-opacity-25" >}}
<div class="accordion">
  <details class="accordion-item">
    <summary class="accordion-button">
      <div class="accordion-header">Accordion Title 1</div>
    </summary>
    <div class="accordion-body">
      <p>....</p>
    </div>
  </details>
  <details class="accordion-item">
    <summary class="accordion-button">
      <div class="accordion-header">Accordion Title 2</div>
    </summary>
    <div class="accordion-body">
      <p>....</p>
    </div>
  </details>
  <details class="accordion-item">
    <summary class="accordion-button">
      <div class="accordion-header">Accordion Title 3</div>
    </summary>
    <div class="accordion-body">
      <p>....</p>
    </div>
  </details>
</div>
{{< /example >}}

## CSS

### Variables

{{< added-in "5.2.0" >}}

As part of Bootstrap's evolving CSS variables approach, accordions now use local CSS variables on `.accordion` for enhanced real-time customization. Values for the CSS variables are set via Sass, so Sass customization is still supported, too.

{{< scss-docs name="accordion-css-vars" file="scss/_accordion.scss" >}}

### Sass variables

{{< scss-docs name="accordion-variables" file="scss/_variables.scss" >}}

<style>
[data-bs-theme="dark"] .bd-example {
  background-color: #000 !important;
}
</style>
