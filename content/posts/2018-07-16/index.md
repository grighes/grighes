---
title: "An Introduction to Progressive Web Apps"
author: "glauber"
date: "2018-07-16"
cover: "https://unsplash.it/1280/900/?random?AngelsofMist"
category: "test3"
tags:
    - progressive-web-apps
    - pwa
    - service-workers
    - lighthouse
---

Hello! How are you?

I'm here to show you some main topics about Progressive Web Apps and the problem that this concept want to solve. Let's take a look.

### What is Progressive Web Apps?

[Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/) are in essence a combination with the best of the native apps and the best of the web.

This was the default explanation about PWA'S, but in other words PWA'S are some kind of checklist that involves many topics, according to Goggle a [Progressive Web App is](https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/):

* Progressive - Works for every user, regardless of browser choice.
* Responsive - Fits any form factor: desktop, mobile, tablet, or whatever is next.
* Connectivity independent - Enhanced with service workers to work offline or on low-quality networks.
* App-like - Feels like an app, because the app shell model separates the application functionality from application content .
* Fresh - Always up-to-date thanks to the service worker update process.
* Safe - Served via HTTPS to prevent snooping and to ensure content hasn't been tampered with.
* Discoverable - Is identifiable as an "application" thanks to W3C manifest and service worker registration scope, allowing search engines to find it.
* Re-engageable - Makes re-engagement easy through features like push notifications.
* Installable - Allows users to add apps they find most useful to their home screen without the hassle of an app store.
* Linkable - Easily share the application via URL, does not require complex installation.

### The Problem

You need to know that our traditional way to use apps are changing:

* [apps are in decline](https://androidauthority.com/end-era-app-downloads-decline-usa-698555/).

And there are apps that have never been used:

* [mobile users spent 80 percent of time just using five apps](http://marketingland.com/report-mobile-users-spend-80-percent-time-just-five-apps-116858).
* [apps have never been used](http://www.tinethygesen.com/post/42502739988/60-of-apps-have-never-been-used-stats-for-app).

Now let's think using a hypothetical/simplistic example:

If you're in a place or you need some occasionally service, you go to the app store and install the app, humm ok... but after that you're going to another place/service and... another app to install, and after one month you have a bunch of useless apps, without also talking about all the steps or [app funnel](http://blog.gaborcselle.com/2012/10/every-step-costs-you-20-of-users.html) needed to finally use the service.

<!-- {% asset_img center-block mobile_funnel.png %} -->

What this graph means?

The greater the amount of steps to finally use your app, lowest is the chances to have your app shared.

Can you see how important became to reduce this gap?

Using Progressive Web Apps this gap is almost nothing, because you just need to visit the website to start testing without all the steps mentioned above.

After that you'll be asked to save the app in your home screen like any other app.

But and if your connection is too poor that you don't know if you close the app or just wait, wait, wait...

<!-- {% asset_img center-block loading.gif %} -->

You could solve this problem using the Offline First approach, preparing your application to keep the fundamental data that your user need using Service Workers.

### The Service Worker

Service Worker is a javascript file that keeps all that you want to maintain offline using cache strategies.

First, you'll need to register your Service Worker using:

```javascript
ServiceWorkerContainer.register();
```

And their lifecycle is basically: Download, Install and Activate.
You can check more details [here](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) and [here](https://developers.google.com/web/fundamentals/primers/service-workers/).

### The Web App Manifest

[The Manifest](https://developers.google.com/web/fundamentals/web-app-manifest/) is a json file that keeps all your app configuration:

* App Name.
* Short Name.
* Appearance: Theme colors.
* Icons: Including the device’s home screen.
* Start Url.

```javascript
  {
  "short_name": "AirHorner",
  "name": "Kinlan's AirHorner of Infamy",
  "icons": [
    {
      "src": "launcher-icon-1x.png",
      "type": "image/png",
      "sizes": "48x48"
    },
    {
      "src": "launcher-icon-2x.png",
      "type": "image/png",
      "sizes": "96x96"
    },
    {
      "src": "launcher-icon-4x.png",
      "type": "image/png",
      "sizes": "192x192"
    }
  ],
  "start_url": "index.html?launcher=true"
}
```

And don't forget to tell the browser about the manifest!

```javascript
  <link rel="manifest" href="/manifest.json">
```

You can easily build a manifest [here](https://app-manifest.firebaseapp.com/)

### Support

You can stay updated about the Service Workers [here](https://caniuse.com/#feat=serviceworkers), [here](https://jakearchibald.github.io/isserviceworkerready/index.html) and [here](https://ispwaready.toxicjohann.com).
Now even safari browser support Service Workers.

### Testing

There is a tool for testing called [Lighthouse](https://developers.google.com/web/tools/lighthouse/).
It's an extension open-source and very easy to start to use, you will be able to generate reports and much more.

### Conclusion

But take care, the PWA’S aren’t the perfect solution for everything.
If you need some specific feature that is present just on native applications just go for that, you can stay updated [here](https://whatwebcando.today/).

Usually, the PWA’S development will become more effective and cheaper because you’ll need just one dev environment for all devices.
And more, you’ll need to balance what your client wants, and the budget that you have.

Finally, isn’t all about a [war between native and web apps](https://medium.com/dev-channel/why-progressive-web-apps-vs-native-is-the-wrong-question-to-ask-fb8555addcbb). You need to keep in mind your goal and the all other variables related to choose the correct tool.

**Thank You!**
