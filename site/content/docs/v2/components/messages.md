---
layout: "docs"
title: "Messages"
description: "Messages provide the user with contextual static information. They have a
lower priority than an alert."
group: components
components: true
aliases:
  - "/components/messages/"
---

## Overview

Messages should be used within other elements to convey helpful information in
an unobtrusive way.

## Examples

To use a message, simply use the `.message` class followed by the appropriate `.message-{theme-color}` class to apply
color. Use an appropriate icon before the text within a message to further convey meaning.

{{< example >}}
<div id="example-messages" class="d-flex flex-column">
<div class="message message-primary">
  <i class="modus-icons notranslate me-1" aria-hidden="true">info</i>This is a primary message
</div>
<div class="message message-secondary">
  <i class="modus-icons notranslate me-1" aria-hidden="true">help</i>This is a secondary message
</div>
</div>
{{< /example >}}
