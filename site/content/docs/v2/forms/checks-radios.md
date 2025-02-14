---
layout: docs
title: Checks and radios
description: Create consistent cross-browser and cross-device checkboxes, radios and switches with our completely rewritten checks component.
group: forms
aliases:
  - "/components/checkboxes/"
  - "/components/radio-buttons/"
  - "/components/switches/"
  - "/docs/v2/forms/checks/"
toc: true
---

## Approach

Browser default checkboxes and radios are replaced with the help of `.form-check`, a series of classes for both input types that improves the layout and behavior of their HTML elements, that provide greater customization and cross browser consistency. Checkboxes are for selecting one or several options in a list, while radios are for selecting one option from many.

Structurally, our `<input>`s and `<label>`s are sibling elements as opposed to an `<input>` within a `<label>`. This is slightly more verbose as you must specify `id` and `for` attributes to relate the `<input>` and `<label>`. We use the sibling selector (`~`) for all our `<input>` states, like `:checked` or `:disabled`. When combined with the `.form-check-label` class, we can easily style the text for each item based on the `<input>`'s state.

Our checks use custom Bootstrap icons to indicate checked or indeterminate states.

## Checks

{{< example >}}
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="CheckDefault">
  <label class="form-check-label" for="CheckDefault">
    Default checkbox
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="CheckChecked" checked>
  <label class="form-check-label" for="CheckChecked">
    Checked checkbox
  </label>
</div>
{{< /example >}}

### Indeterminate

Checkboxes can utilize the `:indeterminate` pseudo class when manually set via JavaScript (there is no available HTML attribute for specifying it).

{{< example class="bd-example-indeterminate" stackblitz_add_js="true" >}}
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="CheckIndeterminate">
  <label class="form-check-label" for="CheckIndeterminate">
    Indeterminate checkbox
  </label>
</div>
{{< /example >}}

### Disabled

Add the `disabled` attribute and the associated `<label>`s are automatically styled to match with a lighter color to help indicate the input's state.

{{< example class="bd-example-indeterminate" stackblitz_add_js="true" >}}
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="CheckIndeterminateDisabled" disabled>
  <label class="form-check-label" for="CheckIndeterminateDisabled">
    Disabled indeterminate checkbox
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="CheckDisabled" disabled>
  <label class="form-check-label" for="CheckDisabled">
    Disabled checkbox
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="CheckCheckedDisabled" checked disabled>
  <label class="form-check-label" for="CheckCheckedDisabled">
    Disabled checked checkbox
  </label>
</div>
{{< /example >}}

## Radios

{{< example >}}
<div class="form-check">
  <input class="form-check-input" type="radio" name="RadioDefault" id="RadioDefault1">
  <label class="form-check-label" for="RadioDefault1">
    Default radio
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="RadioDefault" id="RadioDefault2" checked>
  <label class="form-check-label" for="RadioDefault2">
    Default checked radio
  </label>
</div>
{{< /example >}}

### Disabled

Add the `disabled` attribute and the associated `<label>`s are automatically styled to match with a lighter color to help indicate the input's state.

{{< example >}}
<div class="form-check">
  <input class="form-check-input" type="radio" name="RadioDisabled" id="RadioDisabled" disabled>
  <label class="form-check-label" for="RadioDisabled">
    Disabled radio
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="RadioDisabled" id="RadioCheckedDisabled" checked disabled>
  <label class="form-check-label" for="RadioCheckedDisabled">
    Disabled checked radio
  </label>
</div>
{{< /example >}}

## Switches

A switch has the markup of a custom checkbox but uses the `.form-switch` class to render a toggle switch. Consider using `role="switch"` to more accurately convey the nature of the control to assistive technologies that support this role. In older assistive technologies, it will simply be announced as a regular checkbox as a fallback. Switches also support the `disabled` attribute.

{{< example >}}
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="SwitchCheckDefault">
  <label class="form-check-label" for="SwitchCheckDefault">Default switch checkbox input</label>
</div>
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="SwitchCheckChecked" checked>
  <label class="form-check-label" for="SwitchCheckChecked">Checked switch checkbox input</label>
</div>
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="SwitchCheckDisabled" disabled>
  <label class="form-check-label" for="SwitchCheckDisabled">Disabled switch checkbox input</label>
</div>
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="SwitchCheckCheckedDisabled" checked disabled>
  <label class="form-check-label" for="SwitchCheckCheckedDisabled">Disabled checked switch checkbox input</label>
</div>
{{< /example >}}

## Default (stacked)

By default, any number of checkboxes and radios that are immediate sibling will be vertically stacked and appropriately spaced with `.form-check`.

{{< example >}}
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
  <label class="form-check-label" for="defaultCheck1">
    Default checkbox
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheck2" disabled>
  <label class="form-check-label" for="defaultCheck2">
    Disabled checkbox
  </label>
</div>
{{< /example >}}

{{< example >}}
<div class="form-check">
  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios1" value="option1" checked>
  <label class="form-check-label" for="exampleRadios1">
    Default radio
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios2" value="option2">
  <label class="form-check-label" for="exampleRadios2">
    Second default radio
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios3" value="option3" disabled>
  <label class="form-check-label" for="exampleRadios3">
    Disabled radio
  </label>
</div>
{{< /example >}}

<script>
document.querySelectorAll('.bd-example-indeterminate')
  .forEach(example => {
    example.querySelector('[type="checkbox"]').indeterminate = true
  })
</script>

## Small variants

Smaller variants of checks, radio buttons and switches are available with the  `.form-check-sm` modifier class.

{{< example >}}
<table class="table table-bordered table-sm">
    <thead>
      <tr>
        <th scope="col" width="10%">#</th>
        <th scope="col" width="30%">First</th>
        <th scope="col" width="30%">Last</th>
        <th scope="col" width="30%">Handle</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th><div class="form-check form-check-sm">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheckX">
</div></th>
        <td></td>
        <td></td>
        <td><div class="form-check form-check-sm form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="SwitchCheckDefaultSm" aria-label="Example Small Switch">
</div></td>
      </tr>
      <tr>
        <th><div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheckX">
</div></th>
        <td></td>
        <td></td>
        <td><div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="SwitchCheckDefaultP" aria-label="Example Default Switch">
</div></td>
      </tr>
      <tr>
        <th>3</th>
        <td>Europe</td>
        <td></td>
      </tr>
    </tbody>
</table>

{{< /example >}}

## Sass

### Variables

{{< scss-docs name="form-check-variables" file="scss/_variables.scss" >}}
