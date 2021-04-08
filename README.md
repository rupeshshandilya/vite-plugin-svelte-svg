# Vite Svelte SVG

Vite 2.x plugin to transform SVGs into Svelte components.

It also optimizes your SVGs by running them thru [svgo](https://github.com/svg/svgo).

![npm](https://img.shields.io/npm/v/vite-plugin-svelte-svg)

```svelte
<script>
  import MyIcon from '$lib/assets/my-icon.svg?component';
</script>

<MyIcon width={42} height={42} />
```

## Install

<details>
<summary>NPM</summary>

```
npm install vite-plugin-svelte-svg --save-dev
```

</details>
<details>
<summary>Yarn</summary>

```
yarn add -D vite-plugin-svelte-svg
```

</details>
<details>
<summary>pnpm</summary>

```
pnpm add -D vite-plugin-svelte-svg
```

</details>

## Setup

### `svelte.config.cjs`

```js
const svelteSVG = require("vite-plugin-svelte-svg");

module.exports = {
  kit: {
    vite: {
      plugins: [
        svelteSVG({
          svgoConfig: {}, // See https://github.com/svg/svgo#configuration
        }),
      ],
    },
  },
};
```

## Credits

This plugin is based on the work from the following projects:

- https://github.com/codefeathers/rollup-plugin-svelte-svg
- https://github.com/visualfanatic/vite-svg

## License

MIT