---
layout: docs
title: Form controls
description: Give textual form controls like `<input>`s and `<textarea>`s an upgrade with custom styles, sizing, focus states, and more.
group: forms
toc: true
---

## Example

Form controls are styled with a mix of Sass and CSS variables, allowing them to adapt to color modes and support any customization method.

{{< example >}}
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Email address</label>
  <input type="email" class="form-control" id="exampleFormControlInput1">
</div>
<div class="mb-3">
  <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>
  <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
</div>
{{< /example >}}

## Sizing

Set heights using classes like `.form-control-lg` and `.form-control-sm`.

{{< example >}}
<input class="form-control form-control-lg" type="text" placeholder=".form-control-lg" aria-label=".form-control-lg example">
<input class="form-control" type="text" placeholder="Default input" aria-label="default input example">
<input class="form-control form-control-sm" type="text" placeholder=".form-control-sm" aria-label=".form-control-sm example">
{{< /example >}}

## Form text

Block-level or inline-level form text can be created using `.form-text`.

{{< callout warning >}}
Form text should be explicitly associated with the form control it relates to using the `aria-describedby` attribute. This will ensure that assistive technologies—such as screen readers—will announce this form text when the user focuses or enters the control.
{{< /callout >}}

Form help text can be styled with `.form-text`. If a block-level element will be used, a margin is added for easy spacing from the inputs.

{{< example >}}
<label for="inputPassword5" class="form-label">Password</label>
<div id="passwordHelpBlock" class="form-text">
  Your password must be 8-20 characters long, contain letters and numbers, and must not contain spaces, special characters, or emoji.
</div>
<input type="password" id="inputPassword5" class="form-control" aria-describedby="passwordHelpBlock">
<br>
<label for="inputPassword5lg" class="form-label form-label-lg">Password</label>
<div id="passwordHelpBlock2" class="form-text form-text-lg">
  Your password must be 8-20 characters long, contain letters and numbers, and must not contain spaces, special characters, or emoji.
</div>
<input type="password" id="inputPassword5lg" class="form-control form-control-lg" aria-labelledby="passwordHelpBlock2">
{{< /example >}}

Inline text can use any typical inline HTML element (be it a `<span>`, `<small>`, or something else) with nothing more than the `.form-text` class.

{{< example >}}
<div class="row g-3 align-items-center">
  <div class="col-auto">
    <label for="inputPassword6" class="col-form-label">Password</label>
  </div>
  <div class="col-auto">
    <input type="password" id="inputPassword6" class="form-control" aria-describedby="passwordHelpInline">
  </div>
  <div class="col-auto">
    <span id="passwordHelpInline" class="form-text">
      Must be 8-20 characters long.
    </span>
  </div>
</div>
{{< /example >}}

## Disabled

Add the `disabled` boolean attribute on an input to give it a grayed out appearance, remove pointer events, and prevent focusing.

{{< example >}}
<input class="form-control" type="text" placeholder="Disabled input" aria-label="Disabled input example" disabled>
<input class="form-control" type="text" value="Disabled readonly input" aria-label="Disabled input example" disabled readonly>
{{< /example >}}

## Readonly

Add the `readonly` boolean attribute on an input to prevent modification of the input's value. `readonly` inputs can still be focused and selected, while `disabled` inputs cannot.

{{< example >}}
<input class="form-control" type="text" value="Readonly input here..." aria-label="readonly input example" readonly>
{{< /example >}}

## Readonly plain text

If you want to have `<input readonly>` elements in your form styled as plain text, replace `.form-control` with `.form-control-plaintext` to remove the default form field styling and preserve the correct `margin` and `padding`.

{{< example >}}
  <div class="mb-3 row">
    <label for="staticEmail" class="col-sm-2 col-form-label">Email</label>
    <div class="col-sm-10">
      <input type="text" readonly class="form-control-plaintext" id="staticEmail" value="email@example.com">
    </div>
  </div>
  <div class="mb-3 row">
    <label for="inputPassword" class="col-sm-2 col-form-label">Password</label>
    <div class="col-sm-10">
      <input type="password" class="form-control" id="inputPassword">
    </div>
  </div>
{{< /example >}}

{{< example >}}
<form class="row g-3">
  <div class="col-auto">
    <label for="staticEmail2" class="visually-hidden">Email</label>
    <input type="text" readonly class="form-control-plaintext" id="staticEmail2" value="email@example.com">
  </div>
  <div class="col-auto">
    <label for="inputPassword2" class="visually-hidden">Password</label>
    <input type="password" class="form-control" id="inputPassword2" placeholder="Password">
  </div>
  <div class="col-auto">
    <button type="submit" class="btn btn-primary mb-3">Confirm identity</button>
  </div>
</form>
{{< /example >}}

## File input

{{< example >}}
<div class="mb-3">
  <label for="formFile" class="form-label">Default file input example</label>
  <input class="form-control" type="file" id="formFile">
</div>
<div class="mb-3">
  <label for="formFileMultiple" class="form-label">Multiple files input example</label>
  <input class="form-control" type="file" id="formFileMultiple" multiple>
</div>
<div class="mb-3">
  <label for="formFileDisabled" class="form-label">Disabled file input example</label>
  <input class="form-control" type="file" id="formFileDisabled" disabled>
</div>
<div class="mb-3">
  <label for="formFileSm" class="form-label">Small file input example</label>
  <input class="form-control form-control-sm" id="formFileSm" type="file">
</div>
<div>
  <label for="formFileLg" class="form-label">Large file input example</label>
  <input class="form-control form-control-lg" id="formFileLg" type="file">
</div>
{{< /example >}}

## Color

Set the `type="color"` and add `.form-control-color` to the `<input>`. We use the modifier class to set fixed `height`s and override some inconsistencies between browsers.

{{< example >}}
<label for="exampleColorInput" class="form-label">Color picker</label>
<input type="color" class="form-control form-control-color" id="exampleColorInput" value="#0e416c" title="Choose your color">
{{< /example >}}

## Datalists

Datalists allow you to create a group of `<option>`s that can be accessed (and autocompleted) from within an `<input>`. These are similar to `<select>` elements, but come with more menu styling limitations and differences. While most browsers and operating systems include some support for `<datalist>` elements, their styling is inconsistent at best.

Learn more about [support for datalist elements](https://caniuse.com/datalist).

{{< example >}}
<label for="exampleDataList" class="form-label">Datalist example</label>
<input class="form-control" list="datalistOptions" id="exampleDataList" placeholder="Type to search...">
<datalist id="datalistOptions">
  <option value="San Francisco">
  <option value="New York">
  <option value="Seattle">
  <option value="Los Angeles">
  <option value="Chicago">
</datalist>
{{< /example >}}

## With icons

Wrap your form control in an element with `.form-control-with-icon`, then add a new element as a sibling to the form control with `.form-control-icon`. Place your icons within that new element. Icons will be automatically centered vertically and horizontally, but the sizing of them is up to you.

You can also add icons [to selects]({{< docsref "/forms/select#with-icons" >}}). Textareas are currently not supported.

<!-- Examples below are shown with [Bootstrap Icons](https://icons.getbootstrap.com). -->

{{< example >}}
<label for="formControlWithIcon" class="form-label">Email address</label>
<div class="form-control-with-icon">
  <input type="email" class="form-control" id="formControlWithIcon" placeholder="name@example.com">
  <div class="form-control-icon">
    <svg width="1em" height="1em" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
      <path fill-rule="evenodd" d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2zm13 2.383l-4.758 2.855L15 11.114v-5.73zm-.034 6.878L9.271 8.82 8 9.583 6.728 8.82l-5.694 3.44A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.739zM1 11.114l4.758-2.876L1 5.383v5.73z"/>
    </svg>
  </div>
</div>
{{< /example >}}

### Spinners

You can also place any of Bootstrap's [spinners]({{< docsref "/components/spinners" >}}) within the `.form-control-icon`.

{{< example >}}
<label for="formControlWithSpinner" class="form-label">Email address</label>
<div class="form-control-with-icon">
  <input type="email" class="form-control" id="formControlWithSpinner" placeholder="name@example.com">
  <div class="form-control-icon">
    <div class="spinner-border spinner-border-sm" role="status">
      <span class="visually-hidden">Loading...</span>
    </div>
  </div>
</div>
{{< /example >}}

### Sizing

Add `.form-control-sm` or `.form-control-lg` to your `.form-control` and the `.form-control-icon` will automatically resize. However, the sizing of the icons themselves is up to you.

{{< example >}}
<label for="formControlWithIconSm" class="form-label">Email address</label>
<div class="form-control-with-icon">
  <input type="email" class="form-control form-control-sm" id="formControlWithIconSm" placeholder="name@example.com">
  <div class="form-control-icon">
    <svg width="1em" height="1em" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
      <path fill-rule="evenodd" d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2zm13 2.383l-4.758 2.855L15 11.114v-5.73zm-.034 6.878L9.271 8.82 8 9.583 6.728 8.82l-5.694 3.44A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.739zM1 11.114l4.758-2.876L1 5.383v5.73z"/>
    </svg>
  </div>
</div>
{{< /example >}}

{{< example >}}
<label for="formControlWithIconLg" class="form-label">Email address</label>
<div class="form-control-with-icon">
  <input type="email" class="form-control form-control-lg" id="formControlWithIconLg" placeholder="name@example.com">
  <div class="form-control-icon">
    <svg width="1.5em" height="1.5em" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
      <path fill-rule="evenodd" d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2zm13 2.383l-4.758 2.855L15 11.114v-5.73zm-.034 6.878L9.271 8.82 8 9.583 6.728 8.82l-5.694 3.44A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.739zM1 11.114l4.758-2.876L1 5.383v5.73z"/>
    </svg>
  </div>
</div>
{{< /example >}}

## CSS

### Sass variables

`$input-*` are shared across most of our form controls (and not buttons).

{{< scss-docs name="form-input-variables" file="scss/_variables.scss" >}}

`$form-label-*` and `$form-text-*` are for our `<label>`s and `.form-text` component.

{{< scss-docs name="form-label-variables" file="scss/_variables.scss" >}}

{{< scss-docs name="form-text-variables" file="scss/_variables.scss" >}}

`$form-file-*` are for file input.

{{< scss-docs name="form-file-variables" file="scss/_variables.scss" >}}
