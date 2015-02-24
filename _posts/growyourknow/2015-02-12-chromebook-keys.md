---
layout: post
categories: [GrowYourKnow]
title: Chromebook Home and End Keys
tags : [chromebook,technology,how-to,tips,google,chrome]
pagename: blog
date: 2015-02-12 12:30:00 CDT
---

When transitioning from Windows to my MacBook Pro around 2009, I lamented the missing `Home` and `End` keys. I eventually discovered that the `Command+Left` and `Command+Right` combos performed the same action. It's taken a while, but I'm finally comfortable with the usage.

Fast forward to 2014. I got a shiny, new Chromebook from ASUS. Again, the `Home` and `End` keys were missing. Not a problem. I'm a pro at `Command+Left` and `Command+Right` now.

Unfortunately, the key combo that I've become accustomed to over time has another function on the Chromebook. Namely, `Previous Page` and `Next Page`.

> Technically, the key combo for previous and next page are `Alt+Left` and `Alt-Right`, respectively. But there is no Command / Windows key on the Chromebook, so it's easy to press those key combos from OS X muscle memory.

It's insanely frustrating to be editing a tweet or comment and have the browser navigate away from the page because I hit the key combo that's so intuitive to me now.

No biggie. I can just remap those key combos in the Chrome OS settings, right? Wrong. The keyboard settings allow you to remap a whopping three (predefined) keys. Which, by the way, I suggest you use to remap that lame search button to `CAPSLOCK`.

![Chromebook keyboard settings](https://lh5.googleusercontent.com/t99MlHrn8qZ_BdloKKM58ITPJmsfdYw5thBtIo9fTq4=s0 "Chromebook keyboard settings")

Luckily, one of the fine folks at Google wrote a Chrome extension to remap almost all the preset key mappings. It's called, "Shortcut Manager". It's available as a free install from the [Chrome Web Store](https://chrome.google.com/webstore/detail/shortcut-manager/mgjjeipcdnnjhgodgjpfkffcejoljijf).

![Chrome Web Store](https://lh6.googleusercontent.com/3i7a9FnQHpdYwSoxkT0S4Oh4q8zqrdoLyyMcNq2EO5M=s0 "Chrome Web Store")

The extension allows you to map key combos to browser actions or custom JavaScript logic. We'll use it for the latter. Add the extension, and then click the icon in the toolbar to open the settings dialog.

![Shortcut Manager settings](https://lh3.googleusercontent.com/7H72x0oQ0NR0POg3dz685I6EwaqKRmoXhiOwX3FLyx4=s0 "Shortcut Manager settings")

Shortcut Manager allows you to configure keyboard mappings on a page-by-page basis using the "URL patterns" setting. That's handy, but we want to apply our changes to all pages, so we'll leave the default value (`"*"`) as is.

Click to focus the cursor on the "Shortcut key" field, and then press `Alt+Left`. Change the "Action" setting to "Execute javascript", and then enter the following logic in the second text field.

```JavaScript
javascript:void();
```

That single statement tells the browser to do nothing. Which is just what we want to happen when we accidentally press the offending key combo.

Click the "Save" button at the top of the settings form, and then click the "Add a new shortcut" button to the left of the settings form to repeat the process for `Alt+Right`. I added the optional description in the screenshot shown.

That's it. Unless you actually wanted to use the non-existent `Home` or `End` keys. In which case you press the completely intuitive key combos `Ctrl+Alt+Up` or `Ctrl+Alt+Down`, respectively.

For a full list of keyboard shortcuts, see the [Chromebook FAQ](https://support.google.com/chromebook/answer/183101?hl=en) at their support site.

> Written with [StackEdit](https://stackedit.io/).