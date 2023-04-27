# @greenroom-robotics/eslint-config

> Some opinionated style & type rules built on top of [eslint-config-standard-typescript-prettier](https://github.com/nfour/eslint-config-standard-typescript-prettier)
> 
> See [./.eslintrc.js](./.eslintrc.js)

## Install

Install it.

```bash
pnpm add -D @greenroom-robotics/eslint-config
```

Wire it up.

```bash
echo "module.exports = require('@greenroom-robotics/eslint-config')" > .eslintrc.js

# OR with react rules...

echo "module.exports = require('@greenroom-robotics/eslint-config/.eslintrc.react')" > .eslintrc.js
```

Configure `.prettierrc.js` with something like:

```js
module.exports = {
  ...require('@greenroom-robotics/eslint-config/.prettierrc'),
  semi: false,
}
```

Done.

## How it works

Thanks to `require('@rushstack/eslint-patch/modern-module-resolution');`, plugins can be included relative to the configs, not the consuming project, so you don't need to install any eslint plugins/config peer dependencies.
