# Gently Event List Overlay v1
{:.no_toc}

* TOC
{:toc}

## Overview
The Gently Event List overlay is a highly configurable event list overlay for use with Pixel Chat.

Individual events can be enabled and disabled.

## Settings

### Appearance
* **Font** - Font to be used for event text
* **Message Background Colour** - The background colour of the event
* **Background Image** - Image to be used as background for each event
* **Fade out message** - Should events fade out
* **Time until fade** - The length of time the event list is displayed
* **Number of events to show** - The number of events to show in the list
* **Enable test commands** - Should test commands be enabled (see [Test Commands](#test-commands))
* **Do test commands require a moderator** - Should test commands only be allowed for moderators

### Events
* **Show Host notifications** - Should *Host* events be displayed
* **Show Raid notifications** - Should *Raid* events be displayed
* **Show Follow notifications** - Should *Follow* events be displayed
* **Show Subscribe notifications** - Should *Subscribe* events be displayed
* **Show re-subscription notifications** - Should *Resub* events be displayed
* **Show gift subscription notifications** - Should *Gift Sub* events be displayed
* **Show Support notifications** - Should *Support* events be displayed

## Test Commands
If the *Test Commands* feature is enabled, the following commands are available:
* **!testfollow** - Simulate a *Follow* event
* **!testhost &lt;nn&gt;** - Simulate a *Host* event (optionally with 'nn' viewers)
* **!testraid &lt;nn&gt;** - Simulate a *Raid* event (optionally with 'nn' viewers)
* **!testbits nn &lt;some message text&gt;** - Simulate a *Support* event of nn bits (with an optional message)
* **!testsub &lt;nn&gt;** - Simulate a *Subscribe* event (optionally at level nn)
* **!testgift recipient &lt;nn&gt;** - Simulate a *Gift sub* event to 'recipient' (optionally at level nn)
* **!testresub months &lt;some message text&gt;** - Simulate a *Re-sub* event of 'months' months (with an optional message)

