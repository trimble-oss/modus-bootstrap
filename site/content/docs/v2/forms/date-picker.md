---
layout: docs
title: Date Picker
description:
group: forms
toc: true
aliases:
  - "/components/date-picker/"
---

Modus Bootstrap doesn't ship with a custom-built Date & Time Picker component but you can style a third-party date picker or use native inputs with the `form-control` class.

{{< example class="w-50" >}}
<label for="datetime-local" class="form-label">Date/time</label>
<input type="datetime-local" id="datetime-local" class="form-control" value="2026-02-24T13:00">
<br>
<label for="datetime-local" class="form-label">Date/time with seconds</label>
<input type="datetime-local" id="datetime-local" class="form-control" value="2026-02-24T13:00:45">
<br>
<label for="date" class="form-label">Date</label>
<input type="date" id="date" class="form-control" value="2026-02-24">
<br>
<label for="time" class="form-label">Time</label>
<input type="time" id="time" class="form-control" value="13:00">
<br>
<label for="month" class="form-label">Month</label>
<input type="month" id="month" class="form-control" value="2026-02">
<br>
<label for="week" class="form-label">Week</label>
<input type="week" id="week" class="form-control" value="2026-W09">
{{< /example >}}
