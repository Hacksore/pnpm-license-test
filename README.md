# Turbo + pnpm + vercel

This app uses `pnpm` to generate license info from the `apps/app` application to a json file. The astro app (`apps/web`) will import the json file and render it.

### Vercel build properties
<img width="877" alt="image" src="https://github.com/Hacksore/pnpm-license-test/assets/996134/2c0969da-0d74-43cd-8e24-395f616ba39d">


### Root cause

We've seen that you have to explicit set the output dir to `.vercel/output/static` to make this work

### Error I've seen before

If i push a commit vercel will error with this 😧
```json
{
  "code": "ERR_PNPM_MISSING_PACKAGE_INDEX_FILE",
  "message": "Failed to find package index file for express@4.19.2, please consider running 'pnpm install'"
}
```

### Open vercel issue

TODO: make one here
https://github.com/vercel/vercel/blob/fd069f184d94a41cfcc427e8249418e122a4bf71/packages/frameworks/src/frameworks.ts#L274
