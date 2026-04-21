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

{{< deprecated-in "2.3.2" >}}

{{< callout warning >}}
The Messages component is deprecated and will be removed in a future major release. Use the info alert pattern (`.alert.alert-info`) for new work.
{{< /callout >}}

## Overview

Messages are a legacy pattern that should no longer be used for new UI.

## Recommended replacement

Use an info alert to show contextual static information.

{{< example >}}
<div class="alert alert-info d-flex align-items-center" role="alert">
  <i class="modus-icons notranslate me-1" aria-hidden="true">info</i>
  <div>This is an informational alert.</div>
</div>
{{< /example >}}

## Legacy examples

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
