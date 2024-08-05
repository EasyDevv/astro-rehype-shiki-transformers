# Astro Framework with @shikijs/transformers

This project is based on the Astro framework and uses @shikijs/transformers for advanced code highlighting and formatting.

## Tech Stack

- [Astro.js](https://astro.build/)
- [@shikijs/transformers](https://shiki.style/guide/transformers)

## Project Overview

This project combines Astro's powerful static site generation capabilities with Shiki's advanced code highlighting features. By adding @shikijs/transformers, you can create richer and more interactive code blocks compared to plain Shiki.

## Quick Start

You can run this project directly in your browser without any local setup:

[Run on StackBlitz](https://stackblitz.com/edit/astro-rehype-shiki-transformers)

This StackBlitz link allows you to instantly explore and experiment with the project in a live development environment.

## Key Features

Using @shikijs/transformers, you can leverage advanced code representation features such as:

- **Diff Highlighting**: Visually display code changes
- **Line Highlighting**: Emphasize specific code lines
- **Focus**: Draw attention to important parts of the code

These features make code examples clearer and easier to understand.

## Local Installation

If you prefer to run the project locally:

1. Clone this repository:

   ```bash
   git clone https://github.com/EasyDevv/astro-shiki-transformers.git
   ```

2. Navigate to the project directory:

   ```bash
   cd astro-shiki-transformers
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

## Usage

1. Run the development server:

   ```bash
   npm run dev
   ```

2. Open `http://localhost:4321` in your browser to view the project.

## Shiki Transformers Configuration and Usage Examples

Shiki Transformers are configured in the `astro.config.mjs` file. Here's an example of setting up some useful transformers:

```js
import { defineConfig } from 'astro/config';
import {
  transformerNotationDiff,
  transformerNotationHighlight,
  transformerNotationWordHighlight,
  transformerNotationFocus,
  transformerNotationErrorLevel,
  transformerMetaHighlight,
  transformerMetaWordHighlight,
  transformerRenderWhitespace,
} from '@shikijs/transformers';

export default defineConfig({
  markdown: {
    syntaxHighlight: 'shiki',
    shikiConfig: {
      theme: 'github-dark',
      transformers: [
        transformerNotationDiff(),
        transformerNotationHighlight(),
        transformerNotationWordHighlight(),
        transformerNotationFocus(),
        transformerNotationErrorLevel(),
        transformerMetaHighlight(),
        transformerMetaWordHighlight(),
        transformerRenderWhitespace(),
      ],
    },
  },
});
```

After this configuration, you can use it in your markdown files like this:

````markdown
```ts
console.log('hewwo') // [!code --]
console.log('hello') // [!code ++]
console.log('goodbye')
```
````

## License

This project is distributed under the MIT License. See the `LICENSE` file for more details.
