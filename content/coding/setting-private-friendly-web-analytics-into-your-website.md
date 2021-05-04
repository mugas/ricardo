---
type: Small Tips
language: nuxtjs
title: Setting private-friendly web analytics into your website
summary: I don't like cookies on other websites, so I have been trying to
  keeping them away from mine. If you still want analytics into your website,
  one of the solutions is Plausible.
date: May 4, 2021
update: May 4, 2021
author: Ricardo Moreira
thumbnail: https://res.cloudinary.com/mugas/image/upload/c_scale,w_585/v1620112631/pexels-pixabay-60504_dqiefq.jpg
---
Knowing the analytics on your website is important. Know what pages people go, what pages people don't, etc, from where (in the case you work with a internacional wesite) makes you understand better your website, and your customers for example.
Normally analytics come with privacy issues and cookies and pop-ups, so  when I was developing my websites, even that I would like to have analytics on it I would not wanted to track people or wanted their data shared so I have been avoiding putting analytics till I found a easy solution.
That where [Plausible](https://plausible.io/) comes in. There are more solutions, some more expensive, other more cheap or free but Plausible at least till know offers a great solution for a great price.

It's based in Europe ( Estonia), doesn't track or use any cookies so you don't need to add any cookie statement into your website and you get a full report of your website. If that is not enough I also can say that Plausible is open source and easy to install and manage.

As my website is made with Nuxt I will explain for Nuxt, but in Plausible website there are info and the script to install into other websites.

First I installed Plausible into my project:

```js
npm install vue-plausible
```

After installed open your `nuxt.config.js and in the module section:

```js
modules: [
    [
    'vue-plausible',
  ],
```

Now that you set the module you need to put your domain set. Still in the `nuxt.config.js`, for example right after the modules put this:

```js
plausible: {
    domain: 'yourdomain',
  },
```

In there don't put the `https` just your domain. In my case is `ricardomoreira.io`.

And that's all you need to do. Of course that you also need to go to [Plausible ](https://plausible.io/)website, register your account and put your website there. 
In case you have more than one website, Plausible let's you add has many website you need with the same price.
You can try the trial version, just register and you are free to go.

I am happy with Plausible til the moment and gives exacly what I want, easy analytics with zero tracking.
