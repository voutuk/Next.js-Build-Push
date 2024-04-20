![Image](./images/b1.png)

[Про експорт](https://nextjs.org/docs/pages/building-your-application/deploying)

Edit next.config.js:

```js
const withNextra = require("nextra")({
  theme: "nextra-theme-docs",
  themeConfig: "./theme.config.tsx",
});
module.exports = {
  ...withNextra(),
  images: {
    unoptimized: true, //Fix eror
  },
  assetPrefix: ".", //Normal path
};

```

Edit package.json:

```js
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "export": "next build && next export"
  },
```
