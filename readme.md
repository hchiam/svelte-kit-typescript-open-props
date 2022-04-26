# [svelte-kit](https://kit.svelte.dev/) + typescript + [open-props](https://github.com/argyleink/open-props)

To try to help debug https://github.com/argyleink/open-props/issues/199

## From scratch:

```sh
npm init svelte@next my-app
# chose TypeScript and ESLint
cd my-app
npm install
npm install open-props
npm run dev
# http://localhost:3000/
```

## Using this repo:

```sh
mkdir demo
cd demo
git clone https://github.com/hchiam/svelte-kit-typescript-open-props.git
cd svelte-kit-typescript-open-props/myapp
npm install
npm run dev
# http://localhost:3000/
```

Use an IDE like VSCode to test out auto-complete in /my-app/src/routes/index.svelte

Notice what version of open-props this repo is testing https://github.com/hchiam/svelte-kit-typescript-open-props/blob/main/my-app/package.json#L37
