# Gently Alerts Overlay v1
{:.no_toc}

* TOC
{:toc}

## Overview
The Gently Alerts overlay is a highly configurable alerts overlay for use with Pixel Chat.

Individual alerts can be enabled and disabled, and the properties of each alert configured.

## Settings

### Appearance
* **Enable test mode** - If this setting is enabled, a series of controls will be displayed at the top of the overlay. These can be used to simulate the various types of alerts for testing purposes. **Ensure this mode is turned off before using the overlay!**
* **Font** - Font to be used for alert text
* **Font size** - Font size to be used for alert text
* **Message Background Colour** - The background colour of the alert
* **Message Text Colour** - The text colour used in the alert
* **Message Username Colour** - The text colour for usernames displayed in an alert
* **Message Viewers Colour** - The text colour for viewer counts used in an alert
* **Fade out message** - Should alerts fade out
* **Time until fade** - The length of time an alert is displayed
* **Show Avatars** - Should avatars be shown with each alert
* **Enable test commands** - Should test commands be enabled (see [Test Commands](#test-commands))
* **Do test commands require a moderator** - Should test commands only be allowed for moderators

### Host
* **Show Host notifications** - Should *Host* alerts be displayed
* **Host image** - Image to be shown for *Host* alerts
* **Host sound** - Sound to be played with a *Host* alert
* **Host template no viewer count** - The template for text displayed with a *Host* alert when no viewer count is available (see [Text Templates](#text-templates))
* **Host template with viewer count** - The template for text displayed with a *Host* alert when the viewer count is available (see [Text Templates](#text-templates))

### Raid
* **Show Raid notifications** - Should *Raid* alerts be displayed
* **Raid image** - Image to be shown for *Raid* alerts
* **Raid sound** - Sound to be played with a *Raid* alert
* **Raid template no viewer count** - The template for text displayed with a *Raid* alert when no viewer count is available (see [Text Templates](#text-templates))
* **Raid template with viewer count** - The template for text displayed with a *Raid* alert when the viewer count is available (see [Text Templates](#text-templates))


### Follow
* **Show Follow notifications** - Should *Follow* alerts be displayed
* **Follow image** - Image to be shown for *Follow* alerts
* **Follow sound** - Sound to be played with a *Follow* alert
* **Follow template** - The template for text displayed with a *Follow* alert (see [Text Templates](#text-templates))

### Subscribe
* **Show Subscribe notifications** - Should *Subscribe* alerts be displayed
* **Subscribe image** - Image to be shown for *Subscribe* alerts
* **Subscribe sound** - Sound to be played with a *Subscribe* alert
* **Subscribe template no level** - The template for text displayed with a *Subscribe* alert when no subscription level is available (see [Text Templates](#text-templates))
* **Subscribe template with level** - The template for text displayed with a *Subscribe* alert when the subscription level is available (see [Text Templates](#text-templates))
* **Show Re-Subscription notifications** - Should *Resub* alerts be displayed
* **Resub template** - The template for text displayed with a *Resub* alert (see [Text Templates](#text-templates))
* **Show user's re-sub message** - Should the user's re-sub message text be showed in the *Resub* alert
* **Show git subscription notifications** - Should *Gift Sub* alerts be displayed
* **Gift template no level** - The template for text displayed with a *Gift sub* alert when no subscription level is available (see [Text Templates](#text-templates))
* **Gift template with level** - The template for text displayed with a *Gift Sub* alert when the subscription level is available (see [Text Templates](#text-templates))

### Support
* **Show Support notifications** - Should *Support* alerts be displayed
* **Support image** - Image to be shown for *Support* alerts
* **Support sound** - Sound to be played with a *Support* alert
* **Support template** - The template for text displayed with a *Support* alert (see [Text Templates](#text-templates))
* **Show user's support message** - Should the user's support message text be showed in the *Support* alert

## Text Templates
When displaying messages, the data sent along with the event from Pixel Chat (see [here](https://docs.pixel.chat/api-docs/overlays/events){:target="_blank"}) is 'flattened' into a single level object. Any members of enclosed objects are named with the name of the enclosed object, an underscore, and the name of the enclosed object's member.

For example, the following object:

```
{
  user: {
    name: "adhawkinsgh";
    avatar: "http://twitch.tv/adhawkinsgh.png";
  };
  recipient: {
    name: "acpixel";
    avatar: "http://twitch.tv/acpixel.png";
  };
  level: 2;
}
```

is flattened as:

```
{
  user_name: "adhawkinsgh";
  user_avatar: "http://twitch.tv/adhawkinsgh.png";
  recipient_name: "acpixel";
  recipient_avatar: "http://twitch.tv/acpixel.png";
  level: 2;
}
```

Template strings can then reference these 'flattened' values using the syntax '%flattened_name%' (e.g. '%user_name%').

The default template strings detail the commonly used substitutions for each event.

## Test Commands
If the *Test Commands* feature is enabled, the following commands are available:
* **!testfollow** - Simulate a *Follow* alert
* **!testhost &lt;nn&gt;** - Simulate a *Host* alert (optionally with 'nn' viewers)
* **!testraid &lt;nn&gt;** - Simulate a *Raid* alert (optionally with 'nn' viewers)
* **!testbits nn &lt;some message text&gt;** - Simulate a *Support* alert of nn bits (with an optional message)
* **!testsub &lt;nn&gt;** - Simulate a *Subscribe* alert (optionally at level nn)
* **!testgift recipient &lt;nn&gt;** - Simulate a *Gift sub* alert to 'recipient' (optionally at level nn)
* **!testresub months &lt;some message text&gt;** - Simulate a *Re-sub* alert of 'months' months (with an optional message)

