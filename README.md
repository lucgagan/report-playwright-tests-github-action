# Playwright GitHub Action

Creates comments on PRs with [Playwright](https://github.com/microsoft/playwright) test failures

### Report Playwright Tests

```yaml
jobs:
  tests_e2e:
    name: Run end-to-end tests
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
      - name: Install dependencies
        run: npm ci
      - name: Install playwright browsers
        run: npx playwright install --with-deps
      - name: Run tests
        run: npx playwright test
      - name: Report Playwright tests
        uses: lucgagan/report-playwright-tests@v1
```
 
## Resources

* [Playwright documentation](https://playwright.dev/docs/intro)
* [Chrome Dev Tools Element Selector](https://ray.run/browser-extension)
