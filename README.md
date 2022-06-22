# Astro Testing Data Fetching with Netlify CLI

This a testing example of not being able to conduct data fetching in Astro build while using the Netlify CLI. The main files to look at are:

- `netlify/functions/test.js` - which houses the Netlify Function
- `src/pages/index.astro` - which conducts its data fetching at build time with the frontmatter it has

To reproduce the example you will want to have the Netlify CLI installed with:

```
npm install -g netlify-cli
```

Then you must run the CLI in this directory:

```
cd test-astro-fetching
netlify dev
```

This should produce the error. However, if you eliminate the data fetching from the frontmatter, the Netlify Function builds perfectly fine.

This was build with Astro's starter kit `minimal` by:

```
npm init astro -- --template minimal
```