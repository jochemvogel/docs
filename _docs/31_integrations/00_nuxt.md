---
title: Install Simple Analytics with Nuxt
hidden: true
category: integrations
permalink: /install-simple-analytics-with-nuxt
---

Run this command to install Simple Analytics for Vue:

```bash
npm install simple-analytics-vue
```

## Import Vue in your app

Create a file in your plugin folder with the name `simple-analytics.js`:

```js
// ~/plugins/simple-analytics.js

import SimpleAnalytics from "simple-analytics-vue";
import Vue from "vue";

Vue.use(SimpleAnalytics, { skip: process.env.NODE_ENV !== "production" });
```

Then on your `nuxt.config.js`, make sure to include the plugin with `ssr: false` as we only want to run it on the client:

```js
// nuxt.config.js

export default {
  plugins: [{ src: "~/plugins/simple-analytics.js", ssr: false }],
};
```