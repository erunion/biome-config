# @erunion/biome-config

A shared BiomeJS config.

[![npm](https://img.shields.io/npm/v/@erunion/biome-config)](https://npm.im/@erunion/biome-config) [![Build](https://github.com/erunion/biome-config/workflows/CI/badge.svg)](https://github.com/erunion/biome-config)

## Configs

<!-- prettier-ignore -->
| Config | Description |
| :-- | :--- |
| `@erunion/biome-config` | For projects that use [Biome](https://biomejs.dev/). |
| `@erunion/biome-config/esm` | &mdash; addon for ESM-only repositories.<sup>†</sup>  |
| `@erunion/biome-config/prettier` | For projects that use [Prettier](https://prettier.io/). |

<sub>† This requires also using `@erunion/biome-config/biome`.</sub>

### Biome

### Installation

```sh
npm install --save-dev @biomejs/biome @erunion/biome-config
```

### Usage

Create a `biome.jsonc` file with the following contents:

```json
{
  "extends": [
    "@erunion/biome-config/biome"
    // "@erunion/biome-config/biome/<supplemental>"
  ]
}
```

By default this config does **not** enable auto-formatting. If you need that enabled you will have to turn it on with:

```json
{
  "formatter": {
    "enabled": true
  }
}
```

> [!NOTE]
> If you do use auto-formatting with Biome we recommend **not** also using `@erunion/biome-config/prettier` as they two may collide.

### Prettier

### Installation

```sh
npm install --save-dev prettier @erunion/biome-config
```

### Usage

Add the following into your `package.json`:

```json
"prettier": "@erunion/biome-config/prettier"
```

> [!NOTE]
> If you use Biome and Prettier we recommend disabling Biome's auto-formatting by setting `formatter.enabled` to `false` as the two may collide.
