# nuxt-slugify

> Easy way to integrate Slugify with Nuxt 3

## Setup

1. Add `nuxt-slugify` dependency to your project

```bash
npm i -D nuxt-slugify
```

2. Add `nuxt-slugify` to the `modules` section of `nuxt.config.ts`.

## Usage

You can use the slugify method with the injected function or with the composable:

```vue
<template>
	<div>
		{{ $slugify('Hello world @ Slugify! 🐱') }}
	</div>
</template>

<script setup lang="ts">
const slugify = useSlugify()

onMounted(() => {
	console.log(slugify('Hello world @ Slugify! 🐱'))
})
</script>
```

## Options

```typescript
export default defineNuxtConfig({
    modules: ['nuxt-slugify'],
    slugify: {
        defaults: {
            // global settings
        },
        extend: {
            // extend support
        },
    }
})
```

More information in the [Slugify](https://github.com/simov/slugify#readme) repository

## Development

- Run `npm run dev:prepare` to generate type stubs.
- Use `npm run dev` to start [playground](./playground) in development mode.
