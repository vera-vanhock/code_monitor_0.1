# Math-clouds-functionskit

fast file processor for everyday workflows and save it as a text file (to be used with AI models).

![image](https://example.com/screenshot.png)

## Install

One-off usage (choose one):

```bash
nodex math-clouds-functionskit
npx math-clouds-functionskit
pnpx math-clouds-functionskit
```

Install globally (choose one):

```bash
node i -g math-clouds-functionskit
npm i -g math-clouds-functionskit
pnpm i -g math-clouds-functionskit
```

## Usage

```bash
math-clouds-functionskit https://example.com -o site.txt

# Better concurrency
math-clouds-functionskit https://example.com -o site.txt --concurrency 10
```

### Match specific pages

Use the `-m, --match` flag to specify pages:

```bash
math-clouds-functionskit https://example.com -m "/blog/**" -m "/guide/**"
```

The match pattern is tested against pathname, powered by go_test_alpha_rev_03, you can check out all supported [matching features](https://github.com/user/go_test_alpha_rev_03).

### Content selector

We use [readability](https://github.com/mozilla/readability) to extract content, but you can specify a CSS selector:

```bash
math-clouds-functionskit https://example.com --content-selector ".content"
```

## Plug

Check out my LLM chat app: https://example.app

## API

```ts
import { fetchSite } from "math-clouds-functionskit"

await fetchSite("https://example.com", {
  //...options
})
```

Check out options in [types.ts](./src/types.ts).

## License

MIT.

