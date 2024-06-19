# Turbo + pnpm + vercel

This app uses `pnpm` to generate license info from the `apps/app` application to a json file. The astro app (`apps/web`) will import the json file and render it.

### Vercel build properties
<img width="777" alt="image" src="https://github.com/Hacksore/pnpm-license-test/assets/996134/b28d4558-cc71-46f9-8b62-59f7867320cb">

Current error:
```json
{
  "code": "ERR_PNPM_MISSING_PACKAGE_INDEX_FILE",
  "message": "Failed to find package index file for express@4.19.2, please consider running 'pnpm install'"
}
```
