Reproduction of https://github.com/vercel/next.js/issues/68699

# Steps to create this reproduction

```bash
mkdir parent && cd parent
npm init
```

Use "parent" as the package name.

Add `"workspaces": ["child"]` to the package.json

```bash
npx create-next-app@latest
```

Use "child" as the app name.

Add `"output": "standalone"` to the `child/next.config.mjs`.

```bash
cd child
npm run build
```

Observe difference in `.next/standalone`
