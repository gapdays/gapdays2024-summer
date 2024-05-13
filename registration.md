---
layout: page
title: Registration
registration_state: open
---

{% case page.registration_state %}
{% when 'notyet' %}
<p class="message">Registration will be open soon.</p>

{% when 'closed' %}
<p class="message">Registration is closed.</p>

{% when 'open' %}
<p class="message">Registration is open.</p>

In order to participate in this meeting, please register with us, even if you only
wish to join for parts of the meeting.

To register please send an fill out the linked [form](https://forms.office.com/e/EkXvkpmrhu).

### On funding

We have some limited funding to support travel and accommodation costs
(partially or fully) for participants in need of it. 
If you do so, please send an email to [{{site.email}}](mailto:{{site.email}}) containing the following information

- provide an estimate of much support you expect to need, and
- include a brief explanation of the aims you hope to achieve during
  your visit and, if applicable, whether and how your visit would be
  beneficial to the GAP system and community.

Initial decisions on whether we can grant support and how much will be made
on **5th&nbsp;July&nbsp;2024**. We may be able to support later applications
depending on funds left, so please don't hesitate to ask for funding after this date.

### Questions?

<p>
If you have any questions
regarding registration, or in general, feel free to
<a href="mailto:{{site.email}}">contact us via email</a>.
</p>

{% endcase %}
