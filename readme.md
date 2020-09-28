# Playwright examples

## Playwright test

[tests/test.spec.ts](./tests/test.spec.ts) is a simple test using [playwright-test](https://github.com/microsoft/playwright-test).

Run with:

```
npm install
cd tests/
npx test-runner --browser-name=chromium
```

- [CI job](./.github/workflows/playwright.yml)

## Playwright saucectl

[sauce/tests/example.test.js](./sauce/tests/example.test.js) is a playwright test run with saucectl.

Run with:

```
npm i -g saucectl
cd sauce/
saucectl run
```

- [CI job](./.github/workflows/playwright.yml)
